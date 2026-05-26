---
title: 'getPlayerPing'
---
# `function` getPlayerPing <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's current network ping.

## Declaration
```cpp
number getPlayerPing(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `number`
Average of all ping times read, or -1 if unavailable.
