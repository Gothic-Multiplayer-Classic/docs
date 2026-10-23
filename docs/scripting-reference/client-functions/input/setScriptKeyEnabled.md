---
title: 'setScriptKeyEnabled'
---
# `function` setScriptKeyEnabled <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will enable or disable Lua polling and key events for a keyboard key. This does not change native game bindings.

## Declaration
```cpp
boolean setScriptKeyEnabled(number keyId, boolean enabled)
```

## Parameters
* `number` **keyId**: The key code to control. For more information about key codes, see [Key Constants](../../client-constants/Key.md).
* `boolean` **enabled**: True to include this input in script polling; false to suppress it.
  
## Returns `boolean`
True on success.
