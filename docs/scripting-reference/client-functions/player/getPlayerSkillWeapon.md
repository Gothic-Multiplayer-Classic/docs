---
title: 'getPlayerSkillWeapon'
---
# `function` getPlayerSkillWeapon <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/npc weapon skill hit chance, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerSkillWeapon(number player_id, number skill_id)
```

## Parameters
* `number` **player_id**: Target player id.
* `number` **skill_id**: Skill identifier.
  
## Returns `number|nil`
Hit chance (0-100) or nil.
