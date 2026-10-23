---
title: 'onPlayerEquipRing'
---
# `event` onPlayerEquipRing <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when a player's equipped ring changes.

## Parameters
```c++
void onPlayerEquipRing(number player_id, number ring_slot, ItemDefinition|nil item, ItemDefinition|nil previous_item)
```

* `number` **player_id**: Player id.
* `number` **ring_slot**: Logical ring slot (0 or 1).
* `ItemDefinition|nil` **item**: Equipped ring item (nil if none).
* `ItemDefinition|nil` **previous_item**: Previously equipped item.
