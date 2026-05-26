---
title: 'equipShield'
---
# `function` equipShield <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will equip a shield item for the player.

## Declaration
```cpp
boolean equipShield(number player_id, string instance)
```

## Parameters
* `number` **player_id**: Target player id.
* `string` **instance**: Shield item instance name.
  
## Returns `boolean`
True when the equip packet was sent.
