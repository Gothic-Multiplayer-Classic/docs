---
title: 'setPlayerMaxMana'
---
# `function` setPlayerMaxMana <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc maximum mana. If the current mana exceeds the new maximum, it will be clamped down to the new value.

## Declaration
```cpp
void setPlayerMaxMana(number player_id, number max_mana)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **max_mana**: New maximum mana.
