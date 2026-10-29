---
title: 'onPlayerEquipMeleeWeapon'
---
# `event` onPlayerEquipMeleeWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when a player's equipped melee weapon changes.

## Parameters
```c++
void onPlayerEquipMeleeWeapon(number player_id, string|nil item, string|nil previous_item)
```

* `number` **player_id**: Player id.
* `string|nil` **item**: Equipped melee weapon item (nil if none).
* `string|nil` **previous_item**: Previously equipped item.
