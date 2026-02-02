---
title: 'setPlayerName'
---
# `function` setPlayerName <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Set a player's display name.

## Declaration
```cpp
boolean setPlayerName(number player_id, string name)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **name**: New player name.
  
## Returns `boolean`
True on success, false if the player is missing.
