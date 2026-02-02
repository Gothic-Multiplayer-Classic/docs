---
title: 'stopAni'
---
# `function` stopAni <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Stop a played animation on a player/npc for all players.

## Declaration
```cpp
boolean stopAni(number player_id, string|nil aniName)
```

## Parameters
* `number` **player_id**: Target player id.
* `string|nil` **aniName**: Animation name to stop. Defaults to "" for first active animation.
  
## Returns `boolean`
True on success.
