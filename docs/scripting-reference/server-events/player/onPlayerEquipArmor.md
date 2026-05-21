---
title: 'onPlayerEquipArmor'
---
# `event` onPlayerEquipArmor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped armor changes.

## Parameters
```c++
void onPlayerEquipArmor(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped armor item (nil if none).
