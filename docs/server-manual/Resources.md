# Lua Resources

Lua resources group server scripts, shared code, client scripts, and package metadata. Current GMPC resource loading is declarative: `config.toml` chooses resources and their order, while each `resource.toml` chooses server scripts and their order. For ordinary Gothic assets or a modified `GOTHIC.DAT`, use [VDF Resources](VDF-Resources.md) instead; Lua packages and VDF archives are downloaded and activated through separate parts of the same connection flow.

```text
resources/
  economy/
    resource.toml
    shared/
      constants.lua
    server/
      database.lua
      main.lua
    client/
      main.lua
      ui.lua
```

A directory without `resource.toml` is skipped during discovery. A resource with invalid metadata is discovered as inactive and cannot be selected in the server configuration.

## Selecting Resources

The `resources` array in the server's `config.toml` is the authoritative load order:

```toml
resources = [
  "database",
  "economy",
  "gameplay"
]
```

Only listed resources are packaged and loaded. Directory names do not determine startup order, and an active but unlisted resource does nothing. If a listed resource is missing, inactive, or invalid, server startup fails rather than silently continuing with a partial game mode.

## `resource.toml`

| Field | Required | Meaning |
| --- | --- | --- |
| `version` | yes | Non-empty package version. Change it when players must receive a changed client package. |
| `active` | yes | Whether the resource may be selected. Selecting a resource with `active = false` prevents server startup. |
| `scripts` | yes | Ordered list of server-side `.lua` files to execute. An empty array is valid. |
| `author` | no | Author shown in client-resource metadata. |
| `description` | no | Short description shown in client-resource metadata. |

```toml
version = "1.2.0"
active = true
author = "GMPC Team"
description = "Economy and trading"

scripts = [
  "shared/constants.lua",
  "server/database.lua",
  "server/main.lua"
]
```

Every script path must be relative, end in `.lua`, stay below `shared/` or `server/`, and contain no `..` segment. Files may be nested. They run exactly in array order; GMPC no longer scans either directory for server entry points.

The distinction between the two directories remains important:

| Directory | Server execution | Client packaging |
| --- | --- | --- |
| `server/` | Only when listed in `scripts` | Never packaged. Put secrets and authoritative-only code here. |
| `shared/` | Only when listed in `scripts` | Every `.lua` file is recursively included in the client package. |
| `client/` | Never executed by the server | Every `.lua` file is recursively included in the client package. |

The `scripts` array controls only server execution. It does not restrict what the packager sends from `shared/`, so a shared file must not contain credentials or other server-only data.

## Client Packages

For each configured resource containing Lua files under `client/` or `shared/`, the server compiles those files to stripped Lua bytecode, creates a ZIP-based `.pak`, and writes a manifest under `data/public/`. The manifest records archive and per-file SHA-256 hashes. The client verifies those hashes before executing code; a corrupt or mismatched package stops the connection flow.

`client/main.lua` is the only automatic client entry point. Other packaged files must be loaded from it with `require`. A package without `client/main.lua` can still be downloaded, but it executes no client entry point.

Configured resource order is preserved when packages are announced and loaded by the client. This makes dependencies predictable, but a resource should still fail clearly when a required earlier resource is unavailable.

## Client `require`

Each client resource has an isolated module cache. `require("ui.scoreboard")` normalizes the name to `ui/scoreboard` and searches in this order:

| Order | Path |
| --- | --- |
| 1 | `client/<module>.luac` |
| 2 | `client/<module>.lua` |
| 3 | `shared/<module>.luac` |
| 4 | `shared/<module>.lua` |
| 5 | `<module>.luac` |
| 6 | `<module>.lua` |

A missing module, syntax error, or runtime error fails resource startup and disconnects the client. Keep `client/main.lua` focused on assembling modules so the log identifies failures close to their source.

## Lifecycle

Server scripts may each define `onResourceStart` and `onResourceStop`. Start hooks run in declared `scripts` order after every script has loaded. Stop hooks run in reverse order. Resource-owned timers and event handlers are removed during unload.

Client entry points and required modules can also define resource lifecycle hooks. After every configured client resource has started, GMPC emits [onInit](../scripting-reference/client-events/game/onInit.md) once. During unload it emits [onExit](../scripting-reference/client-events/game/onExit.md) first, then stops resources in reverse resource order and runs each resource's stop hooks in reverse capture order.

Timers created through [setTimer](../scripting-reference/shared-functions/timer/setTimer.md) are associated with the current server resource and are cleaned up when that resource unloads.

## Exports

A server resource exposes functions by assigning an `exports` table:

```lua
exports = {
  giveCoins = function(playerId, amount)
    -- authoritative implementation
  end
}
```

The Lua state also provides a global resource-export proxy. Defining the local resource's `exports` table shadows that proxy, so retain it first when the same resource also consumes another resource:

```lua
local resourceExports = exports

exports = {
  rewardPlayer = function(playerId)
    local economy = resourceExports.economy
    if economy and economy.giveCoins then
      economy.giveCoins(playerId, 10)
    end
  end
}
```

A missing resource, export table, or exported member evaluates to `nil`. Check it before calling unless the dependency is guaranteed by your configured resource order.

See [Data Layout](Data-Layout.md) for the generated public directory, internal Lua data, instance registries, and navigation files used alongside resources.
