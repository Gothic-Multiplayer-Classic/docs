---
title: 'ItemGround'
---
# `class` ItemGround <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

Represents a synchronized server-side ground item visible on the client.


## Properties
### `number` id 

Represents the unique ground item id.

----
### `string` instance 

Represents the Gothic item instance name.

----
### `number` amount 

Represents the item amount.

----
### `nil` definition 

ItemDefinition definitions are currently available on the server only.

----

## Methods
### isValid

Checks whether this handle still refers to an existing synchronized ground item.

```cpp
boolean isValid()
```

  
**Returns `boolean`:**

True while the item exists.

----

## Callbacks
No callbacks.

----
