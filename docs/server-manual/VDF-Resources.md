# VDF Resources

VDF resources let a server distribute ordinary Gothic assets that cannot be delivered as Lua resource packages. This includes meshes, textures, sounds, animations, worlds, and an optional `GOTHIC.DAT`. Use [Lua Resources](Resources.md) for server, shared, and client Lua code; use VDF resources when the game itself must see the asset through its virtual file system.

## Configuration

Add an ordered list to the server's `config.toml`:

```toml
addon_vdfs = [
  "addons/base.vdf",
  "addons/overrides.vdf"
]
```

Paths are resolved relative to the server's working directory. They must name regular files below that directory, use a `.vdf` extension, and contain no absolute path or `..` segment. The file basename is the logical name used for the client bundle, so two configured files cannot have the same basename, even with different letter casing.

The server validates every entry before it starts accepting connections. A missing file, unsafe or non-portable basename, oversized archive, unsupported VDF format, or invalid catalog prevents startup. Each VDF must be between 1 byte and 2 GiB. GMPC accepts the standard VDF format and the Union ZippedStream variant; other archive flags are rejected.

The list order is significant. When archives provide the same virtual path, the later archive wins. Put a base archive first and patches or overrides after it.

## Gothic Data

At most one configured archive may contain `GOTHIC.DAT`. When one is present, the server parses its item definitions and compares them with `data/instances/items.json`. The registry must describe the items from the archive consistently, including their flags, visuals, optional state, damage, ammunition references, protections, and requirements. This prevents the server's item model from silently disagreeing with the client-side Gothic data.

An addon set without `GOTHIC.DAT` is valid and skips that item comparison. The VDF archives themselves are still checked and hashed.

## Distribution And Cache

On successful validation, GMPC creates `data/public/addons.bin` and `data/public/addons.zip`. The binary manifest identifies the ordered VDF set; the ZIP contains the VDF files. The server reuses these generated files only when their identities and checksums still match the current configuration. An empty `addon_vdfs` list removes the generated addon bundle.

The bundle is served by the built-in content endpoint on the same port as the game server. It is not copied into the player's Gothic `Data` directory. The client extracts the VDFs into its GMPC store and mounts them as an overlay for the server session.

The `downloader_group` setting controls the client-side directory below `Multiplayer/Store`. An empty value falls back to the server's `ip_port`; the client sanitizes the resulting name so it is safe to use as a directory. Reuse is allowed only when the complete identity and checksum match, and the active directory must exactly mirror the announced VDF set.

The complete connection bundle has a hard 4 GiB combined limit across manifests, Lua packages, `addons.bin`, and `addons.zip`. The client also accepts at most 32 VDF entries, with no individual VDF larger than 2 GiB.

## Download Settings

| Setting | Default | Notes |
| --- | --- | --- |
| `downloader_file_max_chunk` | `4194304` (4 MiB) | Bytes written in one content-provider call. The accepted range is 16 KiB through 16 MiB. |
| `downloader_rate_limit` | `30` | Requests allowed from one remote address per minute. `0` disables the limit. |
| `downloader_group` | `""` | Client store group, limited to 64 configured characters. |
| `downloader_download_timeout_seconds` | `300` | Maximum duration of one request. `0` disables the timeout. |

Request limits count operations rather than bytes. A connecting client uses two requests for the complete VDF addon set, in addition to two requests per downloaded Lua resource. Invalid numeric values are replaced with their documented defaults; see [Server Configuration](Configuration.md) for the full validation ranges.

## Connection Lifecycle

The client verifies the addon manifest, archive hash and size, ZIP entry order, names, sizes, and CRC before activation. Activation is queued for the next main-thread frame, then GMPC mounts the VDF overlay and reloads the Gothic data parser when a `GOTHIC.DAT` is included. Asset caches are purged when necessary so stale resources are not retained.

On disconnect, client Lua resources, views, multiplayer actors, and addon mounts are unloaded before the base Gothic data is restored. Cached files may remain in `Multiplayer/Store` for a later connection, but they are not active outside the server session.

Any failed validation, download, hash check, ZIP check, or activation aborts the connection. Fix the server's archive set or configuration rather than asking players to copy files manually. See [Server Content](../client-manual/Server-Content.md) for the player-visible side of this process.
