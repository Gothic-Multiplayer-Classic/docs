---
title: 'findNearbyPlayers'
---
# `function` findNearbyPlayers <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Find player ids within a radius of a given position in a world.

## Declaration
```cpp
{...} findNearbyPlayers({x, y, z} position_table, number radius, string world, number virtual_world)
```

## Parameters
* `{x, y, z}` **position_table**: Table with x,y,z coordinates.
* `number` **radius**: Search radius.
* `string` **world**: World name to search in.
* `number` **virtual_world**: Optional virtual world id.
  
## Returns `{...}`
Array of player ids.
