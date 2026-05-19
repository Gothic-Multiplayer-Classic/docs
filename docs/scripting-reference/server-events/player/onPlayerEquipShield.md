---
title: 'onPlayerEquipShield'
---
# `event` onPlayerEquipShield <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped shield changes.

## Parameters
```c++
void onPlayerEquipShield(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped shield instance id (nil if none).
