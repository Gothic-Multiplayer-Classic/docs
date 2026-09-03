# Lua Resources

Each resource is a folder inside `resources/`:

```text
resources/
  economy/
    resource.toml
    server/
      main.lua
    shared/
      constants.lua
    client/
      main.lua
      ui.lua
```

## `resource.toml`

```toml
version = "1.0.0"
author = "GMPC Team"
description = "Economy resource"

scripts = [
  "shared/constants.lua",
  "server/main.lua"
]
```

| Setting | Required | Description |
| --- | --- | --- |
| `version` | yes | Resource version. |
| `scripts` | yes | Server and shared scripts, in execution order. |
| `author` | no | Resource author. |
| `description` | no | Short description. |

Only scripts from `server/` and `shared/` can be listed in `scripts`.

## Script Folders

| Folder | Runs on server | Sent to clients |
| --- | --- | --- |
| `server/` | when listed in `scripts` | no |
| `shared/` | when listed in `scripts` | yes |
| `client/` | no | yes |

Keep passwords and private server code in `server/`. The client starts from `client/main.lua`. Load other client or shared files with `require`:

```lua
local ui = require("ui")
```

## Loading Resources

Add resource folder names to `config.toml`. Only listed resources load, in the listed order:

```toml
resources = [
  "database",
  "economy",
  "gameplay"
]
```

## Lifecycle

```lua
function onResourceStart()
  print("Resource started")
end

function onResourceStop()
  print("Resource stopped")
end
```

## Exports

Expose functions to other resources:

```lua
exports = {
  giveCoins = function(playerId, amount)
    -- Give coins to the player.
  end
}
```

Use the export from another resource:

```lua
local economy = exports.economy

if economy then
  economy.giveCoins(playerId, 10)
end
```
