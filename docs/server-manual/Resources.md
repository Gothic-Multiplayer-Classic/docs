# Resources

Resources are the unit GMPC uses to group Lua code, metadata, and client downloads. A server can run several resources at once: one for core gameplay, one for chat, one for scoreboards, one for custom UI, and so on.

The server discovers resources from the `resources/` directory. Each immediate subdirectory is treated as a resource name.

```text
resources/
  chat/
    resource.toml
    shared/
      constants.lua
    server/
      main.lua
    client/
      main.lua
      ui.lua
```

`resource.toml` is optional for server-side loading, but required when the resource should ship client or shared scripts to players. Without metadata and a non-empty `version`, the server can still run the resource's server scripts, but the client packager skips it.

## Metadata

| Field | Default | Meaning |
| --- | --- | --- |
| `version` | none | Required for client resource packages. Change it when clients must download a new package. |
| `active` | `true` | Set to `false` to keep the resource directory present but prevent server loading and client packaging. |
| `author` | `""` | Optional descriptive metadata. |
| `description` | `""` | Optional descriptive metadata. |

A minimal client-capable metadata file looks like this:

```toml
version = "1.0.0"
active = true
author = "GMPC Team"
description = "Chat and basic player messages"
```

Resource directories are loaded alphabetically after inactive resources are filtered out. If two resources depend on each other, give them names that make the startup order obvious, or move shared behavior into a separate resource that starts first.

## Server Scripts

On the server, GMPC executes direct `.lua` files from these directories:

| Directory | Loaded on server | Notes |
| --- | --- | --- |
| `shared/` | yes | Runs before `server/`. Use it for constants and functions shared with client code. |
| `server/` | yes | Runs after `shared/`. Use it for authoritative gameplay, persistence, validation, and server events. |
| `client/` | no | Never executed by the server runtime. Packaged for clients when metadata allows it. |

Server-side loading is not recursive. Only Lua files directly inside `shared/` and `server/` are executed automatically, sorted by file name. If order matters, make it visible in file names, such as `00_config.lua`, `10_events.lua`, and `20_gameplay.lua`.

Each resource runs in its own Lua environment. Global variables from one resource are not a reliable way to communicate with another resource. Use explicit APIs, events, or exports.

## Client Packages

When a resource has valid metadata and a `version`, the server can package Lua files from `client/` and `shared/` for players. Client packages are written under the server's `public/` directory and downloaded through the built-in resource server.

The packager includes Lua files from `client/` and `shared/` recursively, compiles them to bytecode by default, creates a ZIP-based `.pak`, and writes a manifest with sizes and SHA-256 hashes. The client verifies both the manifest and archive before starting the resource. A missing, corrupt, or mismatched package prevents the client from joining normally.

Only `client/main.lua` is used as the automatic client entry point. Additional client files should be loaded from that entry point with `require`.

## Client `require`

Client resources use a resource-local `require` cache. Module names are normalized so `require("ui.scoreboard")` looks for `ui/scoreboard` paths.

The client search order is:

| Order | Path pattern |
| --- | --- |
| 1 | `client/<module>.luac` |
| 2 | `client/<module>.lua` |
| 3 | `shared/<module>.luac` |
| 4 | `shared/<module>.lua` |
| 5 | `<module>.luac` |
| 6 | `<module>.lua` |

If a required module is missing or throws during loading, the resource startup fails and the client disconnects from the server. Keep `client/main.lua` small and make failures obvious in the log.

## Lifecycle

After scripts are loaded, GMPC calls `onResourceStart` for that resource when the hook exists. During unload, it calls `onResourceStop`, clears resource-owned timers, and releases the Lua environment.

Client resources also receive a single `onInit` after the first client resource starts and a single `onExit` when client resources are unloaded. Use resource-level hooks for per-resource setup and cleanup, and reserve `onInit` or `onExit` for client-wide behavior.

## Exports

A resource can expose a table named `exports`:

```lua
exports = {
  giveCoins = function(playerId, amount)
    -- server-side implementation
  end
}
```

Other server resources can call exported functions through the global export proxy. If the calling resource also defines its own `exports` table, save the proxy before overwriting the name:

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

If the target resource is missing, unloaded, or does not expose the function, the lookup returns `nil`.

Exports are useful for stable cross-resource APIs. They are a poor substitute for clear ownership: validation, persistence, and authority should still live in the resource that owns that data.

## Practical Structure

A maintainable resource usually has one clear responsibility. Put values shared by client and server in `shared/`, authoritative decisions in `server/`, and presentation or input handling in `client/`.

Avoid hiding required startup order in comments. If `inventory` depends on `database`, make the order clear through resource names, metadata, or one explicit bootstrap resource. The server loads alphabetically, so accidental ordering bugs are otherwise easy to introduce.
