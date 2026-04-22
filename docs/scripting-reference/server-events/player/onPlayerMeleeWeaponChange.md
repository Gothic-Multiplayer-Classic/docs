---
title: 'onPlayerMeleeWeaponChange'
---
# `event` onPlayerMeleeWeaponChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's melee weapon changes.

## Parameters
```c++
void onPlayerMeleeWeaponChange(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: New melee weapon instance id (nil if none).
