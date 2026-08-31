# Server Data Layout

GMPC separates source resources, generated client files, server-owned script data, and Gothic registries. Paths below are relative to the server working directory unless stated otherwise.

```text
config.toml
resources/
data/
  public/
  internal/
  instances/
  navigation/
```

| Path | Purpose | Maintained by |
| --- | --- | --- |
| `resources/` | Resource directories containing `resource.toml`, Lua source, and optional client or shared code. | Server creator |
| `data/public/` | Generated files served to clients: Lua `.pak` files and manifests, plus `addons.bin` and `addons.zip` for VDF resources. | GMPC server |
| `data/internal/` | Server-only JSON and TOML data used by Lua scripts. | Server creator or server scripts |
| `data/instances/` | Required `items.json` and `anims.json` registries used during startup and VDF `GOTHIC.DAT` validation. | Server creator, usually from client console output |
| `data/navigation/` | Optional per-world navigation JSON files containing waypoints and, when available, freepoints. | Server creator, usually from client console output |

The server must be able to load valid `items.json` and `anims.json` before it binds the network port. A missing or malformed registry is a startup error, not an empty fallback. The client console can export these registries to `System/Multiplayer`; copy them into `data/instances/` before hosting. The same console workflow can export a world's navigation file.

Navigation filenames use the lower-case world stem, for example `data/navigation/newworld.json`. The file's `zen` value must match the configured world exactly. Waypoints are required for a usable navigation file; freepoints are optional.

JSON and TOML opened through the server scripting API are resolved below `data/internal/`. Relative paths are required and parent traversal is rejected. See the [JSON](../scripting-reference/server-functions/file/JSON.md) and [TOML](../scripting-reference/server-functions/file/TOML.md) references for those APIs.

`data/public/` is part of the server's generated content surface. Do not move Lua packages or VDF bundles into the Gothic installation manually; the client receives their manifests through the server and stores VDFs under `Multiplayer/Store/<group>`. See [VDF Resources](VDF-Resources.md) and [Lua Resources](Resources.md) for the two packaging workflows.
