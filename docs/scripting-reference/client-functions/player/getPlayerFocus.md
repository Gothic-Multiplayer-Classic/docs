---
title: 'getPlayerFocus'
---
# `function` getPlayerFocus <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the focused multiplayer player id for a player or NPC.

## Declaration
```cpp
number getPlayerFocus(number player_id)
```

## Parameters
* `number` **player_id**: Target player or client NPC id.
  
## Returns `number`
Focused player id, or -1 if no multiplayer player is focused.
