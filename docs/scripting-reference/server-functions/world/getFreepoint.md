---
title: 'getFreepoint'
---
# `function` getFreepoint <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Retrieve world position of a freepoint by name.

## Declaration
```cpp
{x, y, z, angle}|nil getFreepoint(string world, string name)
```

## Parameters
* `string` **world**: World name in which the freepoint exists.
* `string` **name**: Freepoint name.
  
## Returns `{x, y, z, angle}|nil`
Freepoint position or nil.
