---
title: 'stopAni'
---
# `function` stopAni <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will stop a played animation on the player/npc character.

## Declaration
```cpp
boolean stopAni(number player_id, string|nil aniName)
```

## Parameters
* `number` **player_id**: Target player id.
* `string|nil` **aniName**: Animation name to stop. Defaults to "" for first active animation.
  
## Returns `boolean`
True on success.
