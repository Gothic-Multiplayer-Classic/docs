---
title: 'onPlayerEquipHandItem'
---
# `event` onPlayerEquipHandItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped hand item changes.

## Parameters
```c++
void onPlayerEquipHandItem(number player_id, number hand, Item|nil item)
```

* `number` **player_id**: Player id.
* `number` **hand**: Hand id (0 = left, 1 = right).
* `Item|nil` **item**: Equipped hand item (nil if none).
