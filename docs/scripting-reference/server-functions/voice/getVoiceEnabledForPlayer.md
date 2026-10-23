---
title: 'getVoiceEnabledForPlayer'
---
# `function` getVoiceEnabledForPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function returns whether a player is allowed to transmit voice.

## Declaration
```cpp
boolean|nil getVoiceEnabledForPlayer(number player_id)
```

## Parameters
* `number` **player_id**: Target player id; NPC ids are not supported.
  
## Returns `boolean|nil`
True when the player may transmit, or nil when missing.
