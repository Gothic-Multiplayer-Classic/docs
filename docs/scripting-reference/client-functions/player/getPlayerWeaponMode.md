---
title: 'getPlayerWeaponMode'
---
# `function` getPlayerWeaponMode <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will return the player/NPC current weapon mode, or nil if unavailable.

## Declaration
```cpp
number|nil getPlayerWeaponMode(number player_id)
```

## Parameters
* `number` **player_id**: Target player or NPC id; negative ids refer to client-local NPCs.
  
## Returns `number|nil`
Weapon mode from [Weapon Mode Constants](../../shared-constants/WeaponMode.md), or nil.
