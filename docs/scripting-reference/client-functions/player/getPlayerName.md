---
title: 'getPlayerName'
---
# `function` getPlayerName <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current name, or nil if unavailable.

## Declaration
```cpp
string|nil getPlayerName(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `string|nil`
Player name or nil.
