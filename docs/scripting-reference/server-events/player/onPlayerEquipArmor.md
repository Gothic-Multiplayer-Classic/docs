---
title: 'onPlayerEquipArmor'
---
# `event` onPlayerEquipArmor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped armor changes.

## Parameters
```c++
void onPlayerEquipArmor(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped armor instance id (nil if none).
