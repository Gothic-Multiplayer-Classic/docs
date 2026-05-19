---
title: 'getNextNearestFreepoint'
---
# `function` getNextNearestFreepoint <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the second nearest freepoint for a given position.

## Declaration
```cpp
{name, x, y, z, angle}|nil getNextNearestFreepoint(number x, number y, number z)
```

## Parameters
* `number` **x**: Position X.
* `number` **y**: Position Y.
* `number` **z**: Position Z.
  
## Returns `{name, x, y, z, angle}|nil`
Freepoint information table or nil.
