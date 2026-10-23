---
title: 'setPlayerInvulnerable'
---
# `function` setPlayerInvulnerable <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc invulnerability.

## Declaration
```cpp
boolean setPlayerInvulnerable(number player_id, boolean enabled)
```

## Parameters
* `number` **player_id**: Target player or NPC id.
* `boolean` **enabled**: Whether damage should be blocked.
  
## Returns `boolean`
True on success; false for an unknown actor.
