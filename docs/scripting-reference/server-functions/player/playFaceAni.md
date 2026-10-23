---
title: 'playFaceAni'
---
# `function` playFaceAni <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will play a face animation on the player's.

## Declaration
```cpp
boolean playFaceAni(number player_id, string aniName)
```

## Parameters
* `number` **player_id**: Target player id; NPC ids are not supported.
* `string` **aniName**: Face animation name (e.g. "S_FRIENDLY").
  
## Returns `boolean`
True on success.
