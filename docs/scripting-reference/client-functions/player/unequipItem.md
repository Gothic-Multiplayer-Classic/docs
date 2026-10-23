---
title: 'unequipItem'
---
# `function` unequipItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will unequip an item from the player/NPC.

## Declaration
```cpp
boolean unequipItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **instance**: ItemDefinition instance name.
  
## Returns `boolean`
True on success.
