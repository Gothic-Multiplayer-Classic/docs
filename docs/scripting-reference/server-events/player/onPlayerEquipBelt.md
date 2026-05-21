---
title: 'onPlayerEquipBelt'
---
# `event` onPlayerEquipBelt <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped belt changes.

## Parameters
```c++
void onPlayerEquipBelt(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped belt item (nil if none).
