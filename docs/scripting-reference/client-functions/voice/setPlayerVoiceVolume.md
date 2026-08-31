---
title: 'setPlayerVoiceVolume'
---
# `function` setPlayerVoiceVolume <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function changes a remote player's local volume multiplier.

## Declaration
```cpp
boolean setPlayerVoiceVolume(number player_id, number volume)
```

## Parameters
* `number` **player_id**: Player id.
* `number` **volume**: Multiplier from 0.0 to 1.0, clamped to that range.
  
## Returns `boolean`
True when the player id was valid.
