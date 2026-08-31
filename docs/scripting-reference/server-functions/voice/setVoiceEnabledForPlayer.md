---
title: 'setVoiceEnabledForPlayer'
---
# `function` setVoiceEnabledForPlayer <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function enables or mutes voice transmission for one player. A disabled
player can still hear other players.

## Declaration
```cpp
boolean setVoiceEnabledForPlayer(number player_id, boolean enabled)
```

## Parameters
* `number` **player_id**: Player id.
* `boolean` **enabled**: Whether this player may transmit voice.
  
## Returns `boolean`
True when the player exists and the state was applied.
