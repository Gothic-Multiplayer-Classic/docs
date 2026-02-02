---
title: 'hasItem'
---
# `function` hasItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Get the amount of a specific item in a player's inventory.

## Declaration
```cpp
number hasItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
  
## Returns `number`
Item amount or 0 if missing.
