# Server Content

When a server provides content, GMPC checks it during connection before running server-provided client Lua or changing the active Gothic data. The process is automatic and does not require a client configuration key.

## What Can Be Downloaded

| Content | Used for | Client handling |
| --- | --- | --- |
| Lua resource package | Client and shared Lua files selected by the server. | Verifies the package manifest and SHA-256 hashes, then starts the resource. |
| VDF resource set | Gothic assets such as textures, meshes, sounds, animations, worlds, or an optional `GOTHIC.DAT`. | Verifies the ordered addon manifest and ZIP contents, stores the VDFs, then mounts them for the server session. |

Lua packages and VDF files are separate parts of the same connection flow. A VDF archive is not a Lua resource, and `addons.zip` is not meant to be copied into Gothic's `Data` directory.

## Storage And Reuse

VDF files are stored below the game's current working directory in:

```text
Multiplayer/Store/<group>/
```

The server chooses `<group>` with `downloader_group`. When it is empty, GMPC derives a group from the server `ip_port`; the client replaces unsafe characters and handles reserved device names. A cached set is reused only when its identity and checksum match the server announcement. The active directory is treated as an exact mirror, so stale or extra VDF files are not used as part of that server session.

The cache is separate from the active Gothic data. Disconnecting unloads the server's Lua resources and VDF mounts, restores the base data, and returns to the main menu. Matching files can remain in the store for a later connection.

## Limits And Verification

The client accepts at most 32 VDF entries. Each VDF may be at most 2 GiB, and the complete connection bundle has a hard 4 GiB combined limit covering manifests, Lua packages, `addons.bin`, and `addons.zip`.

Before activation, GMPC checks the manifest identity, archive hash and size, ZIP entry count and order, portable names, sizes, and CRC values. If the server changes an archive, the new identity must be downloaded and verified; a matching filename alone is not enough. Activation is then queued for the next game frame so the content is mounted safely with the rest of the client state.

## When A Connection Fails

An invalid archive, incomplete download, hash mismatch, unsafe ZIP entry, unsupported content layout, or failed data reload aborts the connection. This is deliberate: continuing with only part of a server's content could make the client and server use different game data.

If the same server repeatedly fails, report the server name and the visible error to its creator. Players should not repair the problem by copying VDFs into Gothic's `Data` directory, because GMPC expects the files in its own store and removes their active mounts when the session ends. See [VDF Resources](../server-manual/VDF-Resources.md) for the configuration and validation rules used by server creators.
