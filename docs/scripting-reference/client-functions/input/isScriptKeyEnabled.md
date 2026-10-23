---
title: 'isScriptKeyEnabled'
---
# `function` isScriptKeyEnabled <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will check whether the specified keyboard key is enabled for script polling.

## Declaration
```cpp
boolean isScriptKeyEnabled(number keyId)
```

## Parameters
* `number` **keyId**: The key code to check. For more information about key codes, see [Key Constants](../../client-constants/Key.md).
  
## Returns `boolean`
True for a valid input enabled for script polling.
