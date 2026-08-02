---
title: 'getHudMode'
---
# `function` getHudMode <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the Gothic HUD display mode.

## Declaration
```cpp
number|nil getHudMode(number hud_type)
```

## Parameters
* `number` **hud_type**: HUD type constant. For more information, see [HUD Constants](../../client-constants/HUD.md).
  
## Returns `number|nil`
HUD mode constant from the same table, or nil for unsupported HUD types.
