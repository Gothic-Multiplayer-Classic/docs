# Server Configuration

The server reads `config.toml` from the server working directory. Missing keys fall back to compiled defaults, while the sample file shipped with the server may choose more conservative values for a public release. The notes below describe the runtime behavior in the current GMPC server code.

Most settings are read during startup. Restart the server after editing this file unless you are changing behavior through a script API that explicitly supports runtime changes.

## Basic Identity And Access

| Setting | Default | What it controls |
| --- | --- | --- |
| `name` | `"Gothic Multiplayer Server"` | Server name shown to clients and master-server listings. Values longer than 100 characters are truncated. |
| `port` | `57005` | UDP game server port. Client resource downloads are served from the same bound port through the built-in resource server. |
| `public` | `false` | Enables master-server heartbeats when the server build includes a master-server endpoint. Without that build-time endpoint, the setting is accepted but listing is skipped. |
| `slots` | `12` | Maximum number of connected players accepted by the network server. |
| `admin_passwd` | `""` | Loaded from config, but no active administration flow uses it in the current server code. Treat it as reserved. |
| `auth_key` | `""` | Loaded and limited to 32 characters. The current code does not use it for gameplay authentication. |

`server_identity_seed` is generated automatically when missing or invalid. It is a base64-encoded 32-byte seed used to derive the server identity keys, so back up the generated value if you need the server to keep the same identity across reinstalls.

## World And Gameplay

| Setting | Default | What it controls |
| --- | --- | --- |
| `map` | `"NEWWORLD\\NEWWORLD.ZEN"` | World path sent to clients and used as the server world name. Keep the path format Gothic expects. |
| `map_md5` | `""` | Loaded and logged only. The current server code does not enforce this value as a map integrity check. |
| `allow_modification` | `true` | When `false`, clients that fail the server's modification or CRC check are removed and their connection is temporarily banned. |
| `hide_map` | `false` | Sends a hide-map flag in server game information, useful for servers that do not want the selected world advertised. |
| `respawn_time_seconds` | `5` | Global automatic respawn delay after death. Negative disables automatic global respawn, `0` respawns immediately, positive values wait that many seconds. Player-specific script settings can override this behavior. |
| `seconds_per_game_minute` | `4` in code, `0` in the sample config | Controls the server clock. `0` freezes time. A positive value means one in-game minute passes after that many real seconds. |

For time scale, `seconds_per_game_minute = 1` makes a full in-game day last 24 real minutes. `4` makes it last 96 minutes. Use `0` only when the world time should remain fixed.

`allow_modification` is not a replacement for `map_md5`. The MD5 value is currently passive metadata, while `allow_modification` acts on the modification check result reported by the client/server flow.

## Logging

| Setting | Default | What it controls |
| --- | --- | --- |
| `log_file` | `"log.txt"` | File sink used by the server logger. The file sink is always created. |
| `log_to_stdout` | `true` | Adds console output in addition to the log file. |
| `log_level` | `"trace"` in code, `"info"` in the sample config | Minimum log level. Valid names come from spdlog, such as `trace`, `debug`, `info`, `warning`, `error`, `critical`, and `off`. |

If `log_level` is missing or invalid, the server falls back to the compiled default. Prefer `info` for normal hosting, `debug` or `trace` while diagnosing scripts or connection issues, and `warning` or higher only when you intentionally want a quiet production log.

## Runtime Tuning

| Setting | Default | What it controls |
| --- | --- | --- |
| `tick_rate_ms` | `100` | Interval used for regular server update broadcasts. Lower values can feel more responsive but increase CPU and network pressure. Higher values reduce traffic at the cost of slower state updates. |
| `daemon` | `false` on Windows, `true` on non-Windows when missing | On non-Windows builds, controls whether the server detaches into daemon mode. Windows builds ignore the daemon path. |

For most public servers, start with the sample config, then change only the values that affect your actual hosting model: `name`, `port`, `public`, `slots`, `map`, respawn behavior, and logging level.
