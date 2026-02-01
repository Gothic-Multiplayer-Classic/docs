---
title: 'removeEventHandler'
---
# `function` removeEventHandler <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Unbind function from specified event.

## Declaration
```cpp
boolean removeEventHandler(string eventName, function func)
```

## Parameters
* `string` **eventName**: The name of the event.
* `function` **func**: The reference to a function.
  
## Returns `boolean`
True on success, false otherwise.
