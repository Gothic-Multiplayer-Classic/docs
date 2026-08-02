# Discord Activity

GMPC exposes a small Discord Rich Presence API to client Lua scripts. Server creators can use it from client resources to show the current server, character state, faction, activity, or other short status text in Discord.

For the generated method signatures, see the [Discord scripting reference](../scripting-reference/client-classes/game/Discord.md).

The API is safe to call even when Discord support is unavailable. In that case the functions simply do nothing.

## Requirements

Discord Rich Presence is active only when the client build was compiled with a Discord application id. In the build system this is provided through the `discord_app_id` option, which defines `DISCORD_APPLICATION_ID` and includes the Discord SDK dependency.

Players also need the Discord desktop client running and logged in. Image keys must exist in the configured Discord application's Rich Presence assets, otherwise Discord will ignore those images.

## API

| Function | Behavior |
| --- | --- |
| `Discord.setActivity(table)` | Updates multiple activity fields at once. Missing fields keep their previous values. |
| `Discord.setState(text)` | Sets the short state line. |
| `Discord.setDetails(text)` | Sets the details line. |
| `Discord.setLargeImage(key, text)` | Sets the large image asset key and optional tooltip text. |
| `Discord.setSmallImage(key, text)` | Sets the small image asset key and optional tooltip text. |
| `Discord.clearActivity()` | Clears the stored activity and removes Rich Presence from Discord. |

`setActivity` accepts both lower camel-case and Pascal-case field names:

| Field | Meaning |
| --- | --- |
| `state` or `State` | Short status text, often current role, faction, or location. |
| `details` or `Details` | Main activity text, often the server or game mode. |
| `largeImageKey` or `LargeImageKey` | Discord asset key for the large image. |
| `largeImageText` or `LargeImageText` | Tooltip for the large image. |
| `smallImageKey` or `SmallImageKey` | Discord asset key for the small image. |
| `smallImageText` or `SmallImageText` | Tooltip for the small image. |

## Example

```lua
Discord.setActivity({
  details = "Valley of Mines RP",
  state = "Guarding the Old Camp",
  largeImageKey = "server_logo",
  largeImageText = "GMP Classic",
  smallImageKey = "guard",
  smallImageText = "Guard"
})
```

For small changes, update only the field that changed:

```lua
Discord.setState("Trading at the market")
Discord.setDetails("Colony Survival")
```

`setLargeImage` and `setSmallImage` keep the previous tooltip when the second argument is omitted. Use `clearActivity` when the player disconnects, returns to a neutral menu state, or joins a mode where you do not want presence shown.

Keep activity text short. Discord truncates long fields, and a concise presence is easier for players to recognize at a glance.
