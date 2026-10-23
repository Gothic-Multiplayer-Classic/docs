---
title: 'giveItem'
---
# `function` giveItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will give an item to the player/npc.

## Declaration
```cpp
boolean giveItem(number player_id, string instance, number amount)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `string` **instance**: [ItemDefinition](../../server-classes/item/ItemDefinition.md) instance name from scripts.
* `number` **amount**: Amount to give.
  
## Returns `boolean`
True on success.
