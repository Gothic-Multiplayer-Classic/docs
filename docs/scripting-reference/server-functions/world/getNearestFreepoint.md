---
title: 'getNearestFreepoint'
---
# `function` getNearestFreepoint <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Retrieve nearest freepoint for a given position.

## Declaration
```cpp
{name, x, y, z, angle}|nil getNearestFreepoint(string world, number x, number y, number z, number|nil distance)
```

## Parameters
* `string` **world**: World name in which the freepoint exists.
* `number` **x**: Position X.
* `number` **y**: Position Y.
* `number` **z**: Position Z.
* `number|nil` **distance**: Optional maximum search distance.
  
## Returns `{name, x, y, z, angle}|nil`
Freepoint information or nil.
