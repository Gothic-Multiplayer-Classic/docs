---
title: 'removeItem'
---
# `function` removeItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will remove an item from the player/NPC's inventory.

## Declaration
```cpp
boolean removeItem(number player_id, string instance, number amount)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `string` **instance**: [ItemDefinition](../../server-classes/item/ItemDefinition.md) instance name from scripts.
* `number` **amount**: Amount to remove.
  
## Returns `boolean`
True on success.
