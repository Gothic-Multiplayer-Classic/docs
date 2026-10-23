---
title: 'onPlayerEquipAmulet'
---
# `event` onPlayerEquipAmulet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event can be cancelled.

This event is triggered when a player's equipped amulet changes.

## Parameters
```c++
void onPlayerEquipAmulet(number player_id, ItemDefinition|nil item, ItemDefinition|nil previous_item)
```

* `number` **player_id**: Player id.
* `ItemDefinition|nil` **item**: Equipped amulet item (nil if none).
* `ItemDefinition|nil` **previous_item**: Previously equipped item.
