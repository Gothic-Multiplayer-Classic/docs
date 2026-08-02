---
title: 'setPlayerTalent'
---
# `function` setPlayerTalent <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc talent value.

## Declaration
```cpp
boolean setPlayerTalent(number player_id, number talent_id, number talent_value)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **talent_id**: Talent identifier. For more information, see [Talent Constants](../../shared-constants/Talent.md).
* `number` **talent_value**: Talent value.
  
## Returns `boolean`
True on success.
