---
title: 'ItemDefinition'
---
# `class` ItemDefinition <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Represents a read-only Gothic item definition from the server item registry.


## Properties
### `function|nil` onUse 
!!! note
    Callback receives player_id, consumed quantity and optional target_id. Set through [ItemCallbacks](ItemCallbacks.md).

The item's server-side use callback.

----
### `function|nil` onEquip 
!!! note
    Callback receives player_id and equipment slot. Set through [ItemCallbacks](ItemCallbacks.md).

The item's server-side equip callback.

----
### `function|nil` onUnequip 
!!! note
    Callback receives player_id and equipment slot. Set through [ItemCallbacks](ItemCallbacks.md).

The item's server-side unequip callback.

----
### `string` instance 

Represents the canonical Gothic item instance name.

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
### `ItemDefinition|nil` munitionItem 

Represents the required munition item definition.

----
### `number` spell 

Represents the spell id associated with this item.

----
### `string` schemeName 

Represents the item's Gothic scheme name.

----
### `number` magicCircle 

Represents the magic circle required by this item.

----
### `{...}` protections 

One-based array of protection tables with `type` and `value` fields. The type uses [Damage Constants](../../shared-constants/Damage.md).

----
### `{...}` requirements 

One-based array of requirement tables with `attribute` and `value` fields.

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
### `static` getByInstance

Returns an item definition by Gothic instance name.

```cpp
ItemDefinition|nil getByInstance(string instance)
```

**Parameters:**

* `string` **instance**: Gothic item instance name.
  
**Returns `ItemDefinition|nil`:**

Definition or nil if missing.

----
### `static` exists

Returns whether an item definition exists for the given instance name.

```cpp
boolean exists(string instance)
```

**Parameters:**

* `string` **instance**: Gothic item instance name.
  
**Returns `boolean`:**



----
### `static` size

Returns the number of item definitions loaded by the server.

```cpp
number size()
```

  
**Returns `number`:**



----
### getRequirement

Returns a requirement by its one-based index.

```cpp
table|nil getRequirement(number index)
```

**Parameters:**

* `number` **index**: Index starting at 1.
  
**Returns `table|nil`:**

Requirement or nil if out of range.

----

## Callbacks
No callbacks.

----
