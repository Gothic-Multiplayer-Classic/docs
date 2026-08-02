---
title: 'isLogicalKeyDisabled'
---
# `function` isLogicalKeyDisabled <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether a Gothic logical game action is disabled for Lua input polling.

## Declaration
```cpp
boolean isLogicalKeyDisabled(number key)
```

## Parameters
* `number` **key**: The logical game action code to check. For more information about key codes, see [Logical Key Constants](../../client-constants/LogicalKey.md).
  
## Returns `boolean`
True when disabled, otherwise false.
