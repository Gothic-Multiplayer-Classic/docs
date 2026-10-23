---
title: 'setPlayerName'
---
# `function` setPlayerName <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will change the player/NPC name.

## Declaration
```cpp
boolean setPlayerName(number player_id, string name)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **name**: New player name.
  
## Returns `boolean`
True on success.
