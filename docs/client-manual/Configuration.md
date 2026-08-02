# Client Configuration

The client reads `GMP_Config.toml` from the current game working directory. If the file is absent, GMPC writes a default one. If parsing fails, it logs the error and uses defaults for that launch without overwriting the broken file.

The current client reads only the settings documented below. Old installations may still contain removed keys; they have no effect.

## Player Settings

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `nickname` | `""` | Player name. An empty value triggers first-launch setup; the menu limits input to 24 characters. |
| `language` | `0` | Zero-based entry in `Multiplayer/Localization/index`. The shipped order begins with English (`0`), Polish (`1`), and German (`2`). |

The in-game options menu is the normal place to change both values. Editing the index manually is useful mainly when a localization file fails to load or the menu cannot be reached.

## Window And Console

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `[window_position].x` / `.y` | absent until known | Restores the game window when both coordinates are positive. Used only in windowed mode. |
| `window_always_on_top` | `false` | Keeps the SDL game window above other windows in windowed mode. |
| `[console_position].x` / `.y` | absent until known | Restores the external debug console when both coordinates are non-negative. |
| `debug_console_enabled` | `true` | Creates the external console used for logs and console commands. |

The client normally writes both position tables itself. If a monitor-layout change leaves either window off-screen, remove that table and let GMPC create a new position.

## Graphics

| Setting | Default | Valid values | Runtime behavior |
| --- | --- | --- | --- |
| `renderer_type` | `"D3D9"` | `"D3D7"`, `"D3D9"`, `"D3D11"` | Renderer selected during startup. Unknown values leave the D3D9 default active. |
| `vsync_enabled` | `true` | `true`, `false` | Initial VSync state passed to the selected renderer. |

Use D3D9 as the normal starting point, D3D7 for the original Gothic renderer or third-party renderer wrappers, and D3D11 only when testing the incomplete native backend. See [Renderer](Renderer.md) for compatibility and troubleshooting details.

## Developer Integration

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `mcp_pipe_enabled` | `false` | Starts the local `\\.\pipe\GothicMCP` named-pipe bridge. It is development tooling and should remain disabled for normal play. |

## Removed Settings

The current client no longer reads `log_chat`, `chat_lines`, `watch_enabled`, `watch_position`, or `[test_mode]`. Chat presentation and the watch are now implemented by Lua resources, and the old built-in test-mode configuration was removed. Delete these keys from stale configurations rather than expecting them to affect the client.
