---
title: 'onPlayerEquipRangedWeapon'
---
# `event` onPlayerEquipRangedWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when a player's equipped ranged weapon changes.

## Parameters
```c++
void onPlayerEquipRangedWeapon(number player_id, ItemDefinition|nil item, ItemDefinition|nil previous_item)
```

* `number` **player_id**: Player id.
* `ItemDefinition|nil` **item**: Equipped ranged weapon item (nil if none).
* `ItemDefinition|nil` **previous_item**: Previously equipped item.
