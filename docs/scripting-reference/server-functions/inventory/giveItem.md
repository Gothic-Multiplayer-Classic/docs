---
title: 'giveItem'
---
# `function` giveItem <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Give an item to a player or NPC.

## Declaration
```cpp
boolean giveItem(number player_id, string instance, number amount)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Item instance name from scripts.
* `number` **amount**: Amount to give.
  
## Returns `boolean`
True on success.
