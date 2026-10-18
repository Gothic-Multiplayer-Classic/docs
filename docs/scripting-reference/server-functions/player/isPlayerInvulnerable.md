---
title: 'isPlayerInvulnerable'
---
# `function` isPlayerInvulnerable <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the current player/npc invulnerability.

## Declaration
```cpp
boolean isPlayerInvulnerable(number player_id)
```

## Parameters
* `number` **player_id**: Target player or server NPC id.
  
## Returns `boolean`
True when invulnerable; false when disabled or the actor does not exist.
