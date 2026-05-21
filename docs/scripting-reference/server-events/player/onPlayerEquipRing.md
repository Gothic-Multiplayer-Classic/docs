---
title: 'onPlayerEquipRing'
---
# `event` onPlayerEquipRing <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped ring changes.

## Parameters
```c++
void onPlayerEquipRing(number player_id, number ring_slot, Item|nil item)
```

* `number` **player_id**: Player id.
* `number` **ring_slot**: Logical ring slot (0 or 1).
* `Item|nil` **item**: Equipped ring item (nil if none).
