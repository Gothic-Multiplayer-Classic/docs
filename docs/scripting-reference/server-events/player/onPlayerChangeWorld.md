---
title: 'onPlayerChangeWorld'
---
# `event` onPlayerChangeWorld <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Triggered when player tries to change the played world (ZEN).

## Parameters
```c++
void onPlayerChangeWorld(int player_id, string world, string waypoint)
```

* `int` **player_id**: The id of the player who tries to change the played world.
* `string` **world**: The filename of the world.
* `string` **waypoint**: The name of the waypoint that the player will be teleported to.
