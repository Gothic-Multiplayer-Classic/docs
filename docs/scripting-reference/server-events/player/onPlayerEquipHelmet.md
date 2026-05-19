---
title: 'onPlayerEquipHelmet'
---
# `event` onPlayerEquipHelmet <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped helmet changes.

## Parameters
```c++
void onPlayerEquipHelmet(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped helmet instance id (nil if none).
