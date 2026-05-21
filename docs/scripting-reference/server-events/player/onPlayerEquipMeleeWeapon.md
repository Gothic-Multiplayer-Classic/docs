---
title: 'onPlayerEquipMeleeWeapon'
---
# `event` onPlayerEquipMeleeWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped melee weapon changes.

## Parameters
```c++
void onPlayerEquipMeleeWeapon(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped melee weapon item (nil if none).
