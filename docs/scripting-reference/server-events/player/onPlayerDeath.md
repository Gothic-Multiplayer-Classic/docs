---
title: 'onPlayerDeath'
---
# `event` onPlayerDeath <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player dies.

## Parameters
```c++
void onPlayerDeath(number player_id, number killer_id)
```

* `number` **player_id**: The id of the player who died.
* `number` **killer_id**: Optional id of the killer (nil if none).
