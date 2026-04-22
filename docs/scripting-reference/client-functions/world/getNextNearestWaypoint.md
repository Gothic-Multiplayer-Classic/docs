---
title: 'getNextNearestWaypoint'
---
# `function` getNextNearestWaypoint <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the second nearest waypoint for a given position.

## Declaration
```cpp
{name, x, y, z}|nil getNextNearestWaypoint(number x, number y, number z)
```

## Parameters
* `number` **x**: Position X.
* `number` **y**: Position Y.
* `number` **z**: Position Z.
  
## Returns `{name, x, y, z}|nil`
Waypoint information table or nil.
