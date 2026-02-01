---
title: 'anx'
---
# `function` anx <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    Use this function only when you want to convert x position or width on the screen.
!!! note
    Virtual screen coordinates are similar to percentage values, where 0 is 0% and 8192 is 100%.

Convert pixels to virtuals screen X dimension and return it as a result.
Virtuals are special type of unit used by the game to position UI elements independent from game resolution.

## Declaration
```cpp
int anx(int pixels)
```

## Parameters
* `int` **pixels**: The pixels to convert.
  
## Returns `int`
The virtuals after conversion.
