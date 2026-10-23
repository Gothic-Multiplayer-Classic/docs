---
title: 'unequipShield'
---
# `function` unequipShield <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will unequip the player/NPC's current shield.

## Declaration
```cpp
boolean unequipShield(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
  
## Returns `boolean`
True when an equipped shield item was found and unequipped.
