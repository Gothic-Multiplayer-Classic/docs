# Client Configuration

The client settings are stored in `GMP_Config.toml` in the game directory. The file is created automatically. Restart the client after changing it manually.

| Setting | Default | Description |
| --- | --- | --- |
| `nickname` | `""` | Player nickname. |
| `language` | `0` | Language index: English `0`, Polish `1`, German `2`, etc. |
| `renderer_type` | `"D3D9"` | Renderer: `"D3D7"`, `"D3D9"`, or `"D3D11"`. |
| `vsync_enabled` | `true` | Enables VSync. |
| `window_always_on_top` | `false` | Keeps the game above other windows in windowed mode. |
| `debug_console_enabled` | `true` | Shows the debug console. |
| `voice_enabled` | `true` | Enables voice chat. |
| `voice_push_to_talk_key` | `37` | Push-to-talk key. `37` is K. |
| `voice_output_volume` | `100` | Voice volume from `0` to `100`. |

Window and console positions are saved automatically. Delete `GMP_Config.toml` to restore the default settings.