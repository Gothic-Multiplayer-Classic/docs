# Client Configuration

The client reads `GMP_Config.toml` from the current game working directory. If the file is missing, GMPC writes a new one with default values. If the file exists but cannot be parsed, the client logs the error and continues with defaults for that launch.

Several values are also changed by the in-game menus, so manual editing is usually needed only for troubleshooting, renderer selection, or development options.

## Player And Interface

| Setting | Default | What it controls |
| --- | --- | --- |
| `nickname` | `""` | Player name. An empty value marks the config as not yet set up and triggers the first-launch flow. The menu limits names to 24 characters. |
| `language` | `0` | Index into the loaded localization list. Invalid indexes fall back to the first loaded language. |
| `log_chat` | `false` | Writes chat messages to the client log when enabled. |
| `chat_lines` | `6` | Number of chat history lines drawn by the client. The menu normally keeps this at `0` or between `5` and `30`. |

`nickname` is the only setting regular players usually need to care about. Leave the rest to the menu unless you are fixing a broken config by hand.

## Watch Overlay

| Setting | Default | What it controls |
| --- | --- | --- |
| `watch_enabled` | `false` | Shows the watch overlay with real time and server game time. |
| `[watch_position].x` | `7000` | Horizontal position of the watch overlay in Gothic's UI coordinate space. |
| `[watch_position].y` | `2500` | Vertical position of the watch overlay in Gothic's UI coordinate space. |

The options menu adjusts the watch position in fixed steps. Manual edits are useful when a custom resolution or renderer places the overlay somewhere awkward.

## Window And Console

| Setting | Default | What it controls |
| --- | --- | --- |
| `[window_position].x` / `[window_position].y` | not written until known | Restores the game window position. The value is used only when both coordinates are positive and the game is running windowed. |
| `window_always_on_top` | `false` | Keeps the SDL game window above other windows in windowed mode. |
| `[console_position].x` / `[console_position].y` | not written until known | Restores the external debug console position when both coordinates are non-negative. |
| `debug_console_enabled` | `true` | Creates the external debug console. Set to `false` for a cleaner normal-player launch. |

`window_position` and `console_position` are mostly state written by the client. If the window opens off-screen after a monitor change, remove the relevant table and let GMPC recreate it.

## Graphics

| Setting | Default | Valid values | What it controls |
| --- | --- | --- | --- |
| `renderer_type` | `"D3D9"` | `"D3D7"`, `"D3D9"`, `"D3D11"` | Renderer backend selected during startup. |
| `vsync_enabled` | `true` | `true`, `false` | Enables vertical synchronization in the selected renderer. |

Use `D3D9` for normal play, `D3D7` when troubleshooting or using external renderer wrappers, and `D3D11` only for testing. Invalid renderer names leave the compiled default in place.

## Developer Options

| Setting | Default | What it controls |
| --- | --- | --- |
| `mcp_pipe_enabled` | `false` | Starts the local `\\.\pipe\GothicMCP` named-pipe bridge used by development tooling. Regular players should leave this disabled. |
| `[test_mode].enabled` | `false` | Skips the main menu and loads directly into a configured test level. |
| `[test_mode].level` | `""` | Level path used by test mode, for example `NEWWORLD\\NEWWORLD.ZEN`. |
| `[test_mode].spawn_x` / `spawn_y` / `spawn_z` | `0.0` | Spawn position used by test mode. |

Test mode is for local development and quick renderer or script checks. It bypasses normal menu flow, so do not enable it in a player-facing config.
