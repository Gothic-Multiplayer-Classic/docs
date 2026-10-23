---
title: 'setPlayerStrength'
---
# `function` setPlayerStrength <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC strength attribute.

## Declaration
```cpp
boolean setPlayerStrength(number player_id, number strength)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **strength**: Strength value.
  
## Returns `boolean`
True on success.
