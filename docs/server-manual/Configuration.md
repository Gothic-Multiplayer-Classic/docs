# Server Configuration

The server reads `config.toml` from its working directory. Missing keys use compiled defaults; malformed or wrongly typed values are generally ignored in favor of those defaults. Restart the server after editing the file unless a Lua API explicitly supports changing the same setting at runtime.

## Identity And Access

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `name` | `"Gothic Multiplayer Server"` | Name sent to clients and master-server listings. Values longer than 100 characters are truncated. |
| `port` | `57005` | Game server port. The built-in client-resource server uses the same bound port. |
| `public` | `false` | Starts master-server heartbeats when the binary was built with a master-server endpoint. Otherwise registration is skipped. |
| `slots` | `12` | Maximum number of players accepted by the network server. |
| `admin_passwd` | `""` | Password for `/rcon login <password>`. An empty value disables administrator login. |
| `auth_key` | `""` | Loaded and truncated to 32 characters, but otherwise unused by the current server implementation. |

An authenticated administrator can use `/rcon diagnostics` to write `diagnostic.txt` in the server working directory. Authentication also unlocks the client's administrator-only noclip tooling. Use a strong password: failed logins are logged, but the current command handler does not rate-limit attempts.

After `config.toml` has loaded successfully, `server_identity_seed` is generated and saved automatically when the field is missing or invalid. It is a base64-encoded 32-byte seed used to derive the server's Ed25519 identity keys. Back it up to preserve the same identity after migration. If the entire configuration file is missing or cannot be parsed, the server uses defaults but skips seed generation, so restore a valid file before hosting.

!!! warning
    Treat `server_identity_seed` as sensitive. The current public-server heartbeat sends this value as `server_seed` to the configured master server, so use only a master-server endpoint you trust and do not reuse the seed for anything outside GMPC.

## World And Gameplay

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `map` | `"NEWWORLD\\NEWWORLD.ZEN"` | World path sent to clients and used as the server world name. |
| `map_md5` | `""` | Loaded and logged only. The current server does not compare or enforce it. |
| `allow_modification` | `true` | Controls admission based on the player's CRC-check state. See the warning below before disabling it. |
| `hide_map` | `false` | Sets the hide-map flag in the game information sent to clients. |
| `respawn_time_seconds` | `5` | Global automatic respawn delay. Negative disables automatic respawn, `0` is immediate, and positive values wait that many seconds. Per-player Lua settings can override it. |
| `seconds_per_game_minute` | `4` | Real seconds per in-game minute. `0` freezes the authoritative server clock. Negative values are rejected and reset to `4`. |

At the default time scale, a full in-game day lasts 96 real minutes. A value of `1` produces a 24-minute day.

!!! danger
    Do not set `allow_modification = false` in the current implementation. Every player starts with `passed_crc_test = false`, and no current code path marks that check as passed. Disabling modifications therefore rejects and temporarily bans every player who tries to join.

`map_md5` does not repair that limitation: it is currently passive configuration data, not an implemented integrity check.

## Resource Startup

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `resources` | `["default", "prototype"]` | Exact resource selection and startup order. Unlisted resource directories are not loaded or sent to clients. |

Empty names and duplicates are removed while the configuration is validated. Startup fails if a listed resource is missing, inactive, has invalid metadata, cannot be packaged, or fails to execute a declared server script. See [Resources](Resources.md) for the required metadata and script-order rules.

## Logging

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `log_file` | `"log.txt"` | File sink created by the server logger. |
| `log_to_stdout` | `true` | Adds terminal output alongside the file log. |
| `log_level` | `"trace"` in code, `"info"` in the sample | Minimum spdlog level. Common values are `trace`, `debug`, `info`, `warning`, `error`, `critical`, and `off`. |

An invalid `log_level` falls back to `trace`. `info` is a practical normal-hosting value; use `debug` or `trace` when investigating resource or network behavior.

## Streaming And Updates

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `tick_rate_ms` | `100` | Interval between regular state-streaming passes. Lower values increase update frequency, CPU work, and network traffic. |
| `stream_radius` | `5000` | Horizontal X/Z distance within which players in the same world and virtual world are streamed to each other. |
| `stream_height` | `0` | Optional vertical Y-distance limit. `0` disables the vertical limit; positive values reject pairs farther apart than this height. |

Negative streaming values are reset to their defaults. Scripts can change the active values through [setStreamerRadius](../scripting-reference/server-functions/streamer/setStreamerRadius.md) and [setStreamerHeight](../scripting-reference/server-functions/streamer/setStreamerHeight.md); those runtime changes are not written back to `config.toml`.

## Process Management

| Setting | Default | Runtime behavior |
| --- | --- | --- |
| `daemon` | `false` on Windows, `true` on non-Windows when omitted | Detaches the process on supported non-Windows builds. The Windows build does not execute the daemon path. |
