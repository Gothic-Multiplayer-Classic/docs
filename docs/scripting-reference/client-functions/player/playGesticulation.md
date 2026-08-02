---
title: 'playGesticulation'
---
# `function` playGesticulation <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will play a gesticulation animation on the player/npc character.
Calls for the same id are throttled to once every 3500 ms.

## Declaration
```cpp
boolean playGesticulation(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `boolean`
True on success.
