---
title: 'onPlayerEquipShield'
---
# `event` onPlayerEquipShield <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped shield changes.

## Parameters
```c++
void onPlayerEquipShield(number player_id, Item|nil item)
```

* `number` **player_id**: Player id.
* `Item|nil` **item**: Equipped shield item (nil if none).
