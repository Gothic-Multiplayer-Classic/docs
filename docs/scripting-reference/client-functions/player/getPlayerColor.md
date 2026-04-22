---
title: 'getPlayerColor'
---
# `function` getPlayerColor <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/npc current character name color, or nil if unavailable.

## Declaration
```cpp
{r, g, b}|nil getPlayerColor(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `{r, g, b}|nil`
Table containing color in RGB model or nil.
