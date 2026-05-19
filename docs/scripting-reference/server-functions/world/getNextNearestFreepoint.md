---
title: 'getNextNearestFreepoint'
---
# `function` getNextNearestFreepoint <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Retrieve second nearest freepoint for a given position.

## Declaration
```cpp
{name, x, y, z, angle}|nil getNextNearestFreepoint(string world, number x, number y, number z)
```

## Parameters
* `string` **world**: World name in which the freepoint exists.
* `number` **x**: Position X.
* `number` **y**: Position Y.
* `number` **z**: Position Z.
  
## Returns `{name, x, y, z, angle}|nil`
Freepoint information or nil.
