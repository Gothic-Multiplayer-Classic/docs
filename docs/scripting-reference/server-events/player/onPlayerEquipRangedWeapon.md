---
title: 'onPlayerEquipRangedWeapon'
---
# `event` onPlayerEquipRangedWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped ranged weapon changes.

## Parameters
```c++
void onPlayerEquipRangedWeapon(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped ranged weapon item (nil if none).
