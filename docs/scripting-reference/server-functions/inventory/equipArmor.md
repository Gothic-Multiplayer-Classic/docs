---
title: 'equipArmor'
---
# `function` equipArmor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will equip an armor item for the player.

## Declaration
```cpp
boolean equipArmor(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Armor item instance name.
  
## Returns `boolean`
True when the equip packet was sent.
