---
title: 'onPlayerEquipAmulet'
---
# `event` onPlayerEquipAmulet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped amulet changes.

## Parameters
```c++
void onPlayerEquipAmulet(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped amulet item (nil if none).
