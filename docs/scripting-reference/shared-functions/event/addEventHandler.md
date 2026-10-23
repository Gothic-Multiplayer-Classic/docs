---
title: 'addEventHandler'
---
# `function` addEventHandler <font size="4">(shared-side)</font>

Subscribes to a built-in or custom event. Custom handlers receive (context, ...), including nil arguments.
Server handlers execute in their owning resource's context and are removed when that resource unloads.

## Declaration
```cpp
boolean addEventHandler(string event_name, function lua_callback, number|nil priority)
```

## Parameters
* `string` **event_name**: Event name.
* `function` **lua_callback**: Handler; retain the same function for removal.
* `number|nil` **priority**: Lower priorities execute first; default 9999.
  
## Returns `boolean`
Whether the subscription was installed.
