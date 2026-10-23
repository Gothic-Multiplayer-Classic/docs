---
title: 'setPlayerHealth'
---
# `function` setPlayerHealth <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC health, not exceeding his current max health.

## Declaration
```cpp
boolean setPlayerHealth(number player_id, number health)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **health**: New health value.
  
## Returns `boolean`
True on success.
