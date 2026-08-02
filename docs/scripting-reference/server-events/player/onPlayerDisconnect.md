---
title: 'onPlayerDisconnect'
---
# `event` onPlayerDisconnect <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when a player disconnects from the server.

## Parameters
```c++
void onPlayerDisconnect(number player_id, number reason)
```

* `number` **player_id**: The id of the player that disconnected.
* `number` **reason**: The reason why player got disconnected. For more information, see [Network Constants](../../server-constants/Network.md).
