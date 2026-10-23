---
title: 'setPlayerLevel'
---
# `function` setPlayerLevel <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC level.

## Declaration
```cpp
boolean setPlayerLevel(number player_id, number level)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **level**: New level.
  
## Returns `boolean`
True on success.
