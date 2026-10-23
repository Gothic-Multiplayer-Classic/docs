---
title: 'isPlayerDead'
---
# `function` isPlayerDead <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether a player or NPC is dead.

## Declaration
```cpp
boolean|nil isPlayerDead(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `boolean|nil`
Dead state, or nil if unavailable.
