---
title: 'getWaypoint'
---
# `function` getWaypoint <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return world position of a waypoint by name.

## Declaration
```cpp
{x, y, z, angle}|nil getWaypoint(string name)
```

## Parameters
* `string` **name**: Waypoint name.
  
## Returns `{x, y, z, angle}|nil`
Waypoint position table or nil.
