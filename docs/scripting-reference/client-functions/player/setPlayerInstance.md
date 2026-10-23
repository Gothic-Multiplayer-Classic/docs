---
title: 'setPlayerInstance'
---
# `function` setPlayerInstance <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will change the player/NPC in-game instance.

## Declaration
```cpp
boolean setPlayerInstance(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **instance**: Instance name.
  
## Returns `boolean`
True if the change was queued for the next frame, false otherwise.
