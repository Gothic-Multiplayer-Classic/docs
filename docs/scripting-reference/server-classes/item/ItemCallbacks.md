---
title: 'ItemCallbacks'
---
# `static class` ItemCallbacks <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Manages server-side item callbacks.


## Properties
No properties.

----

## Methods
### `static` setOnUse

Sets the item's use callback.

```cpp
boolean setOnUse(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: [ItemDefinition](ItemDefinition.md) instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----
### `static` setOnEquip

Sets the item's equip callback.

```cpp
boolean setOnEquip(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: [ItemDefinition](ItemDefinition.md) instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----
### `static` setOnUnequip

Sets the item's unequip callback.

```cpp
boolean setOnUnequip(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: [ItemDefinition](ItemDefinition.md) instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----

## Callbacks
No callbacks.

----
