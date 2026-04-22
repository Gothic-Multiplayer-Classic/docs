---
title: 'hasItem'
---
# `function` hasItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the amount of a specific item in the player/npc inventory on the client.

## Declaration
```cpp
number hasItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Item instance name.
  
## Returns `number`
Item amount or 0 if missing.
