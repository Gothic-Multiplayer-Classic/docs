---
title: 'setPlayerInstance'
---
# `function` setPlayerInstance <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Set a player's instance name.

## Declaration
```cpp
boolean setPlayerInstance(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Instance name.
  
## Returns `boolean`
True on success, false if the player is missing.
