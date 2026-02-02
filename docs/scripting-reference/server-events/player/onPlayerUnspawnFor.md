---
title: 'onPlayerUnspawnFor'
---
# `event` onPlayerUnspawnFor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when a player is unspawned for another player (streaming out).

## Parameters
```c++
void onPlayerUnspawnFor(number player_id, number spawn_id)
```

* `number` **player_id**: Player id losing the spawn.
* `number` **spawn_id**: Player id removed for the receiver.
