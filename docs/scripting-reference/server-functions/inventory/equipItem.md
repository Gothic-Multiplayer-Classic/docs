---
title: 'equipItem'
---
# `function` equipItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Equip an item for all players.

## Declaration
```cpp
boolean equipItem(number player_id, string instance, number slot_id)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
* `number` **slot_id**: Optional slot id. Defaults to -1 for first free slot.
  
## Returns `boolean`
True on success.
