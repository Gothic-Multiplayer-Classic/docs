---
title: 'hasItem'
---
# `function` hasItem <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the amount of a specific item in the player/NPC inventory on the client.

## Declaration
```cpp
number hasItem(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `string` **instance**: ItemDefinition instance name.
  
## Returns `number`
ItemDefinition amount or 0 if missing.
