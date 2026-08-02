---
title: 'setPlayerSkillWeapon'
---
# `function` setPlayerSkillWeapon <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player/npc weapon skill hit chance.

## Declaration
```cpp
boolean setPlayerSkillWeapon(number player_id, number skill_id, number percentage)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **skill_id**: Skill identifier. For more information, see [Weapon Constants](../../shared-constants/Weapon.md).
* `number` **percentage**: Hit chance (0-100).
  
## Returns `boolean`
True on success.
