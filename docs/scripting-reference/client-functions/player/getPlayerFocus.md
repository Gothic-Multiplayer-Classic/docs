---
title: 'getPlayerFocus'
---
# `function` getPlayerFocus <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the focused player or NPC id.

## Declaration
```cpp
number|nil getPlayerFocus(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `number|nil`
Focused player or NPC id, including negative client-local NPC ids; nil when the focus has no known id.
