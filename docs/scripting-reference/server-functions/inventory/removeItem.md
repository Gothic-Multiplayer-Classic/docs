---
title: 'removeItem'
---
# `function` removeItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Remove an item from a player or NPC.

## Declaration
```cpp
bool removeItem(int player_id, string instance, int amount)
```

## Parameters
* `int` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
* `int` **amount**: Amount to remove.
  
## Returns `bool`
True on success.
