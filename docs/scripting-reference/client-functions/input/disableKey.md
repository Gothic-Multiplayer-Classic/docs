---
title: 'disableKey'
---
# `function` disableKey <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Disable/enable specified keyboard key, like: ESCAPE, TAB, etc.

## Declaration
```cpp
boolean disableKey(int keyId, boolean toggle)
```

## Parameters
* `int` **keyId**: The key code to disable. For more information about key codes, see [Key Constants](../../client-constants/Key.md).
* `boolean` **toggle**: true when you want to disable specified keyboard key, otherwise false
  
## Returns `boolean`
True on success.
