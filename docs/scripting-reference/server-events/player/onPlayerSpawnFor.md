---
title: 'onPlayerSpawnFor'
---
# `event` onPlayerSpawnFor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player is spawned for another player (streaming in).

## Parameters
```c++
void onPlayerSpawnFor(number player_id, number spawn_id)
```

* `number` **player_id**: Player id receiving the spawn.
* `number` **spawn_id**: Player id spawned for the receiver.
