---
title: 'getPlayerPosition'
---
# `function` getPlayerPosition <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current world position.

## Declaration
```cpp
{x,y,z}|nil getPlayerPosition(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `{x,y,z}|nil`
Table with keys `x`,`y`,`z` or nil.
