---
title: 'getPlayerNameColor'
---
# `function` getPlayerNameColor <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    Accepts player and server NPC ids; negative client-local NPC ids are not supported.

This function will return the player/NPC current name color, or nil if unavailable.

## Declaration
```cpp
{r, g, b}|nil getPlayerNameColor(number player_id)
```

## Parameters
* `number` **player_id**: Target player or server NPC id; client-local NPC ids are not supported.
  
## Returns `{r, g, b}|nil`
Table containing color in RGB model or nil.
