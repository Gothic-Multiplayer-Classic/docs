---
title: 'Item'
---
# `class` Item <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Represents a read-only Gothic item definition from the server item registry.


## Properties
### `string` instance 

Represents the canonical Gothic item instance name.

----
### `number` index 

Represents the Gothic parser symbol index for this item instance.

----
### `number` mainflag 

Represents the item's main category flag. For more information, see [Item Constants](../../shared-constants/Item.md).

----
### `number` mainFlag 

Represents the item's main category flag. For more information, see [Item Constants](../../shared-constants/Item.md).

----
### `number` flags 

Represents the item's Gothic flags. For more information, see [Item Constants](../../shared-constants/Item.md).

----
### `string` visual 

Represents the item's visual model file.

----
### `number` wear 

Represents the armor wear slot value. For more information, see [Item Constants](../../shared-constants/Item.md).

----
### `number` range 

Represents the item's range value.

----
### `number` value 

Represents the item's value in currency units.

----
### `{total, types}|nil` damage 

Represents the item's damage information. Its `types` field uses [Damage Constants](../../shared-constants/Damage.md).

----
### `number` damageTotal 

Represents the item's total damage.

----
### `number` damageTypes 

Represents the item's Gothic damage type flags. For more information, see [Damage Constants](../../shared-constants/Damage.md).

----
### `string` munition 

Represents the required munition item instance name.

----
### `Item|nil` munitionItem 

Represents the required munition item definition.

----
### `number` spell 

Represents the spell id associated with this item.

----
### `string` scemename 

Represents the item's Gothic sceme name.

----
### `number` mag_circle 

Represents the magic circle required by this item.

----
### `{...}` protections 

Represents protection values exported for this item.

----
### `{...}` conditions 

Represents attribute conditions exported for this item.

----

## Methods
### getProtection

Returns the protection value for a Gothic damage type.

```cpp
number getProtection(number damageType)
```

**Parameters:**

* `number` **damageType**: Gothic damage type. For more information, see [Damage Constants](../../shared-constants/Damage.md).
  
**Returns `number`:**



----
### getCondAtr

Returns the required attribute type at the given condition index.

```cpp
number getCondAtr(number index)
```

**Parameters:**

* `number` **index**: Zero-based condition index.
  
**Returns `number`:**



----
### getCondValue

Returns the required attribute value at the given condition index.

```cpp
number getCondValue(number index)
```

**Parameters:**

* `number` **index**: Zero-based condition index.
  
**Returns `number`:**



----
### getByInstance

Returns an item definition by Gothic instance name.

```cpp
Item|nil getByInstance(string instance)
```

**Parameters:**

* `string` **instance**: Gothic item instance name.
  
**Returns `Item|nil`:**

Item definition or nil if missing.

----
### getByIndex

Returns an item definition by Gothic parser symbol index.

```cpp
Item|nil getByIndex(number index)
```

**Parameters:**

* `number` **index**: Gothic parser symbol index.
  
**Returns `Item|nil`:**

Item definition or nil if missing.

----
### exists

Returns whether an item definition exists for the given instance name.

```cpp
boolean exists(string instance)
```

**Parameters:**

* `string` **instance**: Gothic item instance name.
  
**Returns `boolean`:**



----
### size

Returns the number of item definitions loaded by the server.

```cpp
number size()
```

  
**Returns `number`:**



----

## Callbacks
No callbacks.

----
