---
title: 'onPlayerRingChange'
---
# `event` onPlayerRingChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player's ring changes.

## Parameters
```c++
void onPlayerRingChange(number player_id, number hand_id, number|nil instance)
```

* `number` **player_id**: Player id.
* `number` **hand_id**: Hand id (0 = left, 1 = right).
* `number|nil` **instance**: New ring instance id (nil if none).
