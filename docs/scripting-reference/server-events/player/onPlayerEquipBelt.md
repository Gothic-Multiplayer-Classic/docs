---
title: 'onPlayerEquipBelt'
---
# `event` onPlayerEquipBelt <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player's equipped belt changes.

## Parameters
```c++
void onPlayerEquipBelt(number player_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number|nil` **instance**: Equipped belt instance id (nil if none).
