---
title: 'getPlayerDexterity'
---
# `function` getPlayerDexterity <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC dexterity attribute, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerDexterity(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `number|nil`
Dexterity value or nil.
