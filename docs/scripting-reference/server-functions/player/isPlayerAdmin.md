---
title: 'isPlayerAdmin'
---
# `function` isPlayerAdmin <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether player is logged in through rcon.

## Declaration
```cpp
boolean isPlayerAdmin(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `boolean`
True when player is rcon-authenticated, otherwise false.
