---
title: 'equipItem'
---
# `function` equipItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will equip an item for the player/NPC.

## Declaration
```cpp
boolean equipItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **instance**: Item instance name.
  
## Returns `boolean`
True on success.
