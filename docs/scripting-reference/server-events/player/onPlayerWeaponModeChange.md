---
title: 'onPlayerWeaponModeChange'
---
# `event` onPlayerWeaponModeChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's weapon mode changes.

## Parameters
```c++
void onPlayerWeaponModeChange(number player_id, number old_mode, number new_mode)
```

* `number` **player_id**: Player id.
* `number` **old_mode**: Previous weapon mode. For more information, see [Weapon Mode Constants](../../shared-constants/WeaponMode.md).
* `number` **new_mode**: New weapon mode from the same table.
