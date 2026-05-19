---
title: 'onPlayerEquipMeleeWeapon'
---
# `event` onPlayerEquipMeleeWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped melee weapon changes.

## Parameters
```c++
void onPlayerEquipMeleeWeapon(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped melee weapon instance id (nil if none).
