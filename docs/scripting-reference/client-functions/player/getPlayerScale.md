---
title: 'getPlayerScale'
---
# `function` getPlayerScale <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current model scale, or nil if unavailable.

## Declaration
```cpp
{x, y, z}|nil getPlayerScale(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `{x, y, z}|nil`
Player scale or nil.
