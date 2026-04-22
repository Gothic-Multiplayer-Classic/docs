---
title: 'hexToRgb'
---
# `function` hexToRgb <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will convert a hex color string to an RGB table.

## Declaration
```cpp
{r, g, b}|nil hexToRgb(string hex)
```

## Parameters
* `string` **hex**: Hex color string (e.g. "#RRGGBB", "0xRRGGBB", or "RGB").
  
## Returns `{r, g, b}|nil`
Table containing r, g, b components or nil on failure.
