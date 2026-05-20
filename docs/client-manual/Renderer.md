# Renderer

GMPC can start Gothic through three renderer paths. Choose the renderer in `GMP_Config.toml` with `renderer_type`, then restart the client.

```toml
renderer_type = "D3D9"
vsync_enabled = true
```

## Renderer Choices

| Value | Best use | Notes |
| --- | --- | --- |
| `"D3D7"` | Vanilla compatibility, troubleshooting, and external renderer wrappers | Uses Gothic's original Direct3D 7 renderer. GMPC does not replace the renderer in this mode. |
| `"D3D9"` | Normal play | Default GMPC renderer. It supports modern resolution handling, but the client still marks it as experimental because visual glitches are possible. |
| `"D3D11"` | Testing only | Native GMPC Direct3D 11 path. The client warns that it is not fully implemented. |

For most players, start with `D3D9`. If the game fails to start, crashes during video initialization, or renders incorrectly, switch to `D3D7` and test again. Use `D3D11` only when you specifically want to test that backend.

## External Renderers

Third-party Gothic renderers such as GD3D11 and LegacyAltRenderer expect Gothic's original rendering path. Use `renderer_type = "D3D7"` when testing those tools with GMPC.

Do not combine GMPC's native `D3D9` or `D3D11` renderer with a separate renderer wrapper unless you already know that wrapper supports this setup. Those modes replace Gothic's renderer instead of leaving the original path untouched.

## VSync

`vsync_enabled` is read from the same config file. The exact effect depends on the selected renderer and graphics driver. In the D3D9 path, changing VSync may require a device reset or client restart before the result is visible.

## Troubleshooting

| Symptom | First check |
| --- | --- |
| Black screen or crash on launch | Set `renderer_type = "D3D7"` and restart. |
| External renderer wrapper does not load | Use `D3D7`; native GMPC renderers replace the original Gothic renderer path. |
| Tearing or uneven frame pacing | Toggle `vsync_enabled` and restart the client. |
| Visual glitches in normal play | Try `D3D7` to separate renderer bugs from server or script issues. |

When reporting renderer issues, include the selected renderer, whether VSync is enabled, your Gothic version, and any external renderer or wrapper you are using.
