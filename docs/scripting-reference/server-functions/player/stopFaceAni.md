---
title: 'stopFaceAni'
---
# `function` stopFaceAni <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will stop a played face animation on the player's character.

## Declaration
```cpp
void stopFaceAni(number player_id, string|nil aniName)
```

## Parameters
* `number` **player_id**: Target player id.
* `string|nil` **aniName**: Face animation name to stop. Defaults to "" for first active animation.
