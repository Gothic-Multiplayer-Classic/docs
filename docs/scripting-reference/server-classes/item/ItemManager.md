---
title: 'ItemManager'
---
# `class` ItemManager <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Manages server-side item callbacks.


## Properties
No properties.

----

## Methods
### setOnUse

Sets the item's use callback.

```cpp
boolean setOnUse(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: Item instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----
### setOnEquip

Sets the item's equip callback.

```cpp
boolean setOnEquip(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: Item instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----
### setOnUnequip

Sets the item's unequip callback.

```cpp
boolean setOnUnequip(string instance, function|nil callback)
```

**Parameters:**

* `string` **instance**: Item instance name.
* `function|nil` **callback**: Callback, or nil to remove it.
  
**Returns `boolean`:**

True on success.

----

## Callbacks
No callbacks.

----
