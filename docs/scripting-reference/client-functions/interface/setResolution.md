---
title: 'setResolution'
---
# `function` setResolution <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the current game resolution.

## Declaration
```cpp
boolean setResolution(number width, number height, number|nil bpp)
```

## Parameters
* `number` **width**: Resolution width.
* `number` **height**: Resolution height.
* `number|nil` **bpp**: Optional bits per pixel. Defaults to the current renderer bpp.
  
## Returns `boolean`
True on success.
