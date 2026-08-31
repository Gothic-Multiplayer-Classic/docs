---
title: 'isPlayerVoiceTalking'
---
# `function` isPlayerVoiceTalking <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function checks whether a remote player is currently speaking.

## Declaration
```cpp
boolean isPlayerVoiceTalking(number player_id)
```

## Parameters
* `number` **player_id**: Player id.
  
## Returns `boolean`
True while recent valid voice frames are being received.
