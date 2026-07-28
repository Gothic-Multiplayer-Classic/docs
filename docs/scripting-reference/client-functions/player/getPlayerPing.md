---
title: 'getPlayerPing'
---
# `function` getPlayerPing <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the local player's current network ping.

## Declaration
```cpp
number getPlayerPing(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `number`
Player ping replicated by the server, or -1 if unavailable.
