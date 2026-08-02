---
title: 'disableLogicalKey'
---
# `function` disableLogicalKey <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will disable/enable a Gothic logical game action for Lua input polling.

## Declaration
```cpp
boolean disableLogicalKey(number key, boolean toggle)
```

## Parameters
* `number` **key**: The logical game action code to disable. For more information about key codes, see [Logical Key Constants](../../client-constants/LogicalKey.md).
* `boolean` **toggle**: True to disable, false to enable.
  
## Returns `boolean`
True on success.
