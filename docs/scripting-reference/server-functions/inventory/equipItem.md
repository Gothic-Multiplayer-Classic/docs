---
title: 'equipItem'
---
# `function` equipItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will equip an item for the player.

## Declaration
```cpp
void equipItem(number player_id, string instance, number slot_id)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
* `number` **slot_id**: Optional slot id. Defaults to -1 for first free slot.
