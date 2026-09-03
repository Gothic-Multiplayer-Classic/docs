# Renderer

GMPC can use its own renderer or Gothic's original rendering path.

## Which Renderer Should I Use?

- **D3D9** is the default and recommended renderer for normal play.
- **D3D7** uses Gothic's original renderer. Use it for compatibility, troubleshooting, or external renderer mods.
- **D3D11** is not finished and should only be used for testing.

## External Renderers

External renderers such as [GD3D11](https://github.com/kirides/GD3D11) and [LegacyAltRenderer](https://github.com/SaiyansKing/Gothic-LegacyAltRenderer) expect Gothic's original rendering method. Select D3D7 when using them. Do not combine them with GMPC's D3D9 or D3D11 renderer.

## Troubleshooting

- For a black screen or startup crash, try D3D7.
- If an external renderer does not load, select D3D7.
- For screen tearing, toggle VSync and restart the client.
- For visual glitches, compare the result with D3D7 before reporting the problem.