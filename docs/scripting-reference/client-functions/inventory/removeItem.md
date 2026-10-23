---
title: 'removeItem'
---
# `function` removeItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will remove an item from the player/NPC inventory on the client.

## Declaration
```cpp
boolean removeItem(number player_id, string instance, number amount)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **instance**: ItemDefinition instance name.
* `number` **amount**: Amount to remove.
  
## Returns `boolean`
True on success.
