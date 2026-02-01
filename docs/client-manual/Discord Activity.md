# Discord Activity
The `Discord` class provides access to Discord Rich Presence from the game client.
It allows Lua scripts to update the player's Discord activity, such as showing the current state, details, and images while playing.

## Overview
Using the `Discord` class, you can:

* Display custom text in the player's Discord status
* Show large and small images with optional tooltips
* Update activity dynamically during gameplay
* Clear the activity when it is no longer needed

All methods are static and are called directly on the Discord table.

## Usage Example
#### This will update the player's Discord status to show the provided text.
```lua
Discord.setState("Exploring the world")
Discord.setDetails("Level 10 - Old Camp")
```

#### Updates multiple activity fields at once.
```lua
Discord.setActivity({
  state = "In Combat",
  details = "Fighting Orcs",
  largeImageKey = "world",
  largeImageText = "Myrtana",
  smallImageKey = "sword",
  smallImageText = "Armed"
})
```

#### Clears the current Discord Rich Presence and resets all stored activity values.
```lua
Discord.clearActivity()
```

## Activity Fields
Discord Rich Presence supports the following fields, all of which are optional:

| Field            | Description                                   |
| ---------------- | --------------------------------------------- |
| `state`          | Short status text (shown below the game name) |
| `details`        | Detailed description (shown above the state)  |
| `largeImageKey`  | Asset key for the large image                 |
| `largeImageText` | Tooltip text for the large image              |
| `smallImageKey`  | Asset key for the small image                 |
| `smallImageText` | Tooltip text for the small image              |

Any field not explicitly set will retain its previous value.
