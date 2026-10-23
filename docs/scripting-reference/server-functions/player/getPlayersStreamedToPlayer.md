---
title: 'getPlayersStreamedToPlayer'
---
# `function` getPlayersStreamedToPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the list of players that have been spawned for the given player.

## Declaration
```cpp
{...} getPlayersStreamedToPlayer(number player_id)
```

## Parameters
* `number` **player_id**: Target player id; NPC ids are not supported.
  
## Returns `{...}`
One-based array of player and server NPC ids visible to this player.
