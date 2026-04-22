---
title: 'setPlayerSkillWeapon'
---
# `function` setPlayerSkillWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the player's weapon skill hit chance.

## Declaration
```cpp
void setPlayerSkillWeapon(number player_id, number skill_id, number percentage)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **skill_id**: Skill identifier, for more information check [Weapon Constants](../../shared-constants/Weapon.md).
* `number` **percentage**: Hit chance amount.
