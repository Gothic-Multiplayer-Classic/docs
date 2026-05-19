---
title: 'onPlayerEquipAmulet'
---
# `event` onPlayerEquipAmulet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped amulet changes.

## Parameters
```c++
void onPlayerEquipAmulet(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped amulet instance id (nil if none).
