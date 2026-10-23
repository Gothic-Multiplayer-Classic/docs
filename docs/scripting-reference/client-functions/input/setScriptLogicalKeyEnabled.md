---
title: 'setScriptLogicalKeyEnabled'
---
# `function` setScriptLogicalKeyEnabled <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This function will enable or disable a Gothic logical game action for Lua input polling. This does not change native game bindings.

## Declaration
```cpp
boolean setScriptLogicalKeyEnabled(number key, boolean enabled)
```

## Parameters
* `number` **key**: The logical game action code to control. For more information about key codes, see [Logical Key
* `boolean` **enabled**: True to include this input in script polling; false to suppress it.
  
## Returns `boolean`
True on success.
