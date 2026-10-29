---
title: 'equipItem'
---
# `function` equipItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function requests equipment for a player or server NPC. The item must exist in the actor's server inventory.

## Declaration
```cpp
boolean equipItem(number player_id, string instance, number|nil slot_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `string` **instance**: Item instance name from scripts.
* `number|nil` **slot_id**: Optional slot id. Defaults to -1 for first free slot.
  
## Returns `boolean`
True on success.
