---
title: 'setPlayerSkillWeapon'
---
# `function` setPlayerSkillWeapon <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Set a player's weapon skill hit chance (0-100).

## Declaration
```cpp
boolean setPlayerSkillWeapon(number player_id, number skill_id, number percentage)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **skill_id**: Skill identifier.
* `number` **percentage**: Hit chance (0-100).
  
## Returns `boolean`
True on success.
