---
title: 'setPlayerColor'
---
# `function` setPlayerColor <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Set a player's name color (RGB 0-255).

## Declaration
```cpp
boolean setPlayerColor(number player_id, number r, number g, number b)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **r**: Red (0-255).
* `number` **g**: Green (0-255).
* `number` **b**: Blue (0-255).
  
## Returns `boolean`
True on success, false if the player is missing.
