---
title: 'onPlayerEquipHelmet'
---
# `event` onPlayerEquipHelmet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped helmet changes.

## Parameters
```c++
void onPlayerEquipHelmet(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped helmet item (nil if none).
