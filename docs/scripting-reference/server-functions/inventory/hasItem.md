---
title: 'hasItem'
---
# `function` hasItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the amount of a specific item in the player/NPC's inventory.

## Declaration
```cpp
number hasItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `string` **instance**: Item instance name from scripts.
  
## Returns `number`
Item quantity, or 0 if missing.
