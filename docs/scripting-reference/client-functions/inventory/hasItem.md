---
title: 'hasItem'
---
# `function` hasItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Get the amount of a specific item in a player's inventory on the client.

## Declaration
```cpp
int hasItem(int player_id, string instance)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **instance**: Item instance name.
  
## Returns `int`
Item amount or 0 if missing.
