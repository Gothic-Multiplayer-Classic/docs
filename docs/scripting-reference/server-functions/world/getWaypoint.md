---
title: 'getWaypoint'
---
# `function` getWaypoint <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Retrieve world position of a waypoint by name.

## Declaration
```cpp
{x, y, z, angle}|nil getWaypoint(string world, string name)
```

## Parameters
* `string` **world**: World name in which the waypoint exists.
* `string` **name**: Waypoint name.
  
## Returns `{x, y, z, angle}|nil`
Waypoint position or nil.
