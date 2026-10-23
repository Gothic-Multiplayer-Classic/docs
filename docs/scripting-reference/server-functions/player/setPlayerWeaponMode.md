---
title: 'setPlayerWeaponMode'
---
# `function` setPlayerWeaponMode <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC's weapon mode.

## Declaration
```cpp
boolean setPlayerWeaponMode(number player_id, number weapon_mode)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `number` **weapon_mode**: Weapon mode constant. For more information, see [Weapon Mode Constants](../../shared-constants/WeaponMode.md).
  
## Returns `boolean`
True on success.
