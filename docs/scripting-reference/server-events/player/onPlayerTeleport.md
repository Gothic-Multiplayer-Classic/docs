---
title: 'onPlayerTeleport'
---
# `event` onPlayerTeleport <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    This event is triggered after the teleport is completed and cannot be cancelled. Calling [setPlayerPosition](../../server-functions/player/setPlayerPosition.md) does not trigger this event.

This event is triggered when a player teleports using a game's spell or teleport trigger.

## Parameters
```c++
void onPlayerTeleport(number playerId, string vobName)
```

* `number` **playerId**: The id of the player who teleported.
* `string` **vobName**: The name of the destination waypoint, freepoint or vob.
