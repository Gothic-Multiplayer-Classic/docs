---
title: 'setPlayerWeaponMode'
---
# `function` setPlayerWeaponMode <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Set the player/npc weapon mode for all players.

## Declaration
```cpp
boolean setPlayerWeaponMode(number player_id, number weapon_mode)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **weapon_mode**: Weapon mode constant.
  
## Returns `boolean`
True on success, false if the player is missing.
