---
title: 'getBarSize'
---
# `function` getBarSize <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return a Gothic HUD status bar size in virtual coordinates.

## Declaration
```cpp
{width, height}|nil getBarSize(number hud_type)
```

## Parameters
* `number` **hud_type**: Status bar HUD type constant.
  
## Returns `{width, height}|nil`
Status bar size, or nil for unsupported HUD types.
