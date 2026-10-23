---
title: 'getPlayerPosition'
---
# `function` getPlayerPosition <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC's position, or nil if unavailable.

## Declaration
```cpp
{x, y, z}|nil getPlayerPosition(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `{x, y, z}|nil`
Table containing x,y,z or nil.
