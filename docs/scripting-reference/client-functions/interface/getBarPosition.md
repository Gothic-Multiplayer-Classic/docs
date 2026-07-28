---
title: 'getBarPosition'
---
# `function` getBarPosition <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return a Gothic HUD status bar position in virtual coordinates.

## Declaration
```cpp
{x, y}|nil getBarPosition(number hud_type)
```

## Parameters
* `number` **hud_type**: Status bar HUD type constant.
  
## Returns `{x, y}|nil`
Status bar position, or nil for unsupported HUD types.
