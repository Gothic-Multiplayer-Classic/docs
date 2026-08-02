---
title: 'setTime'
---
# `function` setTime <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

This function will set the server time (hour, minute, optional day offset).

## Declaration
```cpp
boolean setTime(number hour, number min, number|nil day)
```

## Parameters
* `number` **hour**: Hour (0-23).
* `number` **min**: Minute (0-59).
* `number|nil` **day**: Optional day offset.
  
## Returns `boolean`
True on success.
