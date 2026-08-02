---
title: 'setPlayerWeaponMode'
---
# `function` setPlayerWeaponMode <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc weapon mode for all players.

## Declaration
```cpp
boolean setPlayerWeaponMode(number player_id, number weapon_mode)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **weapon_mode**: Weapon mode constant. For more information, see [Weapon Mode Constants](../../shared-constants/WeaponMode.md).
  
## Returns `boolean`
True on success.
