---
title: 'setPlayerFatness'
---
# `function` setPlayerFatness <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC model fatness.

## Declaration
```cpp
boolean setPlayerFatness(number player_id, number fatness)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **fatness**: Fatness value.
  
## Returns `boolean`
True on success.
