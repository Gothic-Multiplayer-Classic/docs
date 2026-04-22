---
title: 'getPlayerPosition'
---
# `function` getPlayerPosition <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/npc current world position.

## Declaration
```cpp
{x,y,z}|nil getPlayerPosition(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `{x,y,z}|nil`
Table with keys `x`,`y`,`z` or nil.
