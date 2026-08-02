---
title: 'equipMeleeWeapon'
---
# `function` equipMeleeWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will equip a melee weapon for the player.

## Declaration
```cpp
boolean equipMeleeWeapon(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Melee weapon item instance name.
  
## Returns `boolean`
True when the equip packet was sent.
