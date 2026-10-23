---
title: 'unequipMeleeWeapon'
---
# `function` unequipMeleeWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will unequip the player/NPC's current melee weapon.

## Declaration
```cpp
boolean unequipMeleeWeapon(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `boolean`
True when an equipped melee weapon was found and unequipped.
