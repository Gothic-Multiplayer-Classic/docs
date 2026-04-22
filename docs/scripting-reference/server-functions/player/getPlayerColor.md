---
title: 'getPlayerColor'
---
# `function` getPlayerColor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player's name color, or nil if unavailable.

## Declaration
```cpp
{r, g, b}|nil getPlayerColor(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `{r, g, b}|nil`
RGB color table or nil.
