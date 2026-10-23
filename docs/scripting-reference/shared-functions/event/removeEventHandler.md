---
title: 'removeEventHandler'
---
# `function` removeEventHandler <font size="4">(shared-side)</font>

Unsubscribes the original callback passed to [addEventHandler](addEventHandler.md).
On the server, a resource may remove only its own subscription.

## Declaration
```cpp
boolean removeEventHandler(string event_name, function lua_callback)
```

## Parameters
* `string` **event_name**: Event name.
* `function` **lua_callback**: The same function object used to subscribe.
  
## Returns `boolean`
Whether a handler was removed.
