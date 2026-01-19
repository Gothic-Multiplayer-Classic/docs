---
title: 'setPlayerAngle'
---
# `function` setPlayerAngle <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Set a player's facing angle (radians) in world space.

## Declaration
```cpp
void setPlayerAngle(int player_id, float angle, bool|nil interpolate)
```

## Parameters
* `int` **player_id**: Target player id.
* `float` **angle**: Angle in radians.
* `bool|nil` **interpolate**: Optional interpolation flag.
