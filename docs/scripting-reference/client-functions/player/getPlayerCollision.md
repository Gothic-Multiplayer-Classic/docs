---
title: 'getPlayerCollision'
---
# `function` getPlayerCollision <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return whether collision is enabled for a player or NPC.

## Declaration
```cpp
boolean|nil getPlayerCollision(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `boolean|nil`
Collision state, or nil if unavailable.
