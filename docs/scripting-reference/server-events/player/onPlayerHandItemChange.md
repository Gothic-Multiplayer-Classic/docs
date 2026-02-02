---
title: 'onPlayerHandItemChange'
---
# `event` onPlayerHandItemChange <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player's hand item changes.

## Parameters
```c++
void onPlayerHandItemChange(number player_id, number hand, number|nil instance)
```

* `number` **player_id**: Player id.
* `number` **hand**: Hand id (0 = left, 1 = right).
* `number|nil` **instance**: New hand item instance id (nil if none).
