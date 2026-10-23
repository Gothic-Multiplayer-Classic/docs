---
title: 'setPlayerMana'
---
# `function` setPlayerMana <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/NPC mana, not exceeding his current max mana.

## Declaration
```cpp
boolean setPlayerMana(number player_id, number mana)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
* `number` **mana**: Mana value.
  
## Returns `boolean`
True on success.
