---
title: 'getNearestWaypoint'
---
# `function` getNearestWaypoint <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the nearest waypoint for a given position.

## Declaration
```cpp
{name, x, y, z, angle}|nil getNearestWaypoint(number x, number y, number z, number|nil distance)
```

## Parameters
* `number` **x**: Position X.
* `number` **y**: Position Y.
* `number` **z**: Position Z.
* `number|nil` **distance**: Optional maximum search distance.
  
## Returns `{name, x, y, z, angle}|nil`
Waypoint information table or nil.
