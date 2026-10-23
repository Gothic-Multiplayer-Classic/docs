---
title: 'unequipArmor'
---
# `function` unequipArmor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will unequip the player/NPC's current armor.

## Declaration
```cpp
boolean unequipArmor(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `boolean`
True when an equipped armor item was found and unequipped.
