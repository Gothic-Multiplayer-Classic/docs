---
title: 'unequipItem'
---
# `function` unequipItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will unequip an item for the player/npc.

## Declaration
```cpp
boolean unequipItem(number player_id, string instance, number|nil slot_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `string` **instance**: Item instance name from scripts.
* `number|nil` **slot_id**: Equipment slot. Omit to clear all matching slots.
  
## Returns `boolean`
True on success.
