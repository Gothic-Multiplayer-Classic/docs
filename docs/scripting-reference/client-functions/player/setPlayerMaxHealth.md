---
title: 'setPlayerMaxHealth'
---
# `function` setPlayerMaxHealth <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC maximum health. If the current health exceeds the new maximum, it will be clamped down to the new value.

## Declaration
```cpp
boolean setPlayerMaxHealth(number player_id, number max_health)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **max_health**: New maximum health.
  
## Returns `boolean`
True on success.
