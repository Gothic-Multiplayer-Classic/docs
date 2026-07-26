---
title: 'TomlFile'
---
# `class` TomlFile <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Read-only TOML document returned by TOML(). Values can be accessed with
normal field or index syntax, including nested sections. Use get_or when a
missing value should fall back without replacing configured false.


## Properties
No properties.

----

## Methods
### has

Return true when a key or nested path exists. A string path uses dots as
separators; a table path can be used for dynamic or literal key segments.

```cpp
bool has(string|table|number path)
```

**Parameters:**

* `string|table|number` **path**: Key, dotted path, path table, or array index.
  
**Returns `bool`:**

True if the value exists.

----
### get

Return a value by key or nested path. Missing keys return nil.

```cpp
any|nil get(string|table|number path)
```

**Parameters:**

* `string|table|number` **path**: Key, dotted path, path table, or array index.
  
**Returns `any|nil`:**

Value or nil when missing.

----
### get_or

Return a value by key or nested path, or the fallback only when the value is
missing. This preserves configured false values.

```cpp
any get_or(string|table|number path, any fallback)
```

**Parameters:**

* `string|table|number` **path**: Key, dotted path, path table, or array index.
* `any` **fallback**: Value returned when path is missing.
  
**Returns `any`:**

Configured value or fallback.

----
### entries

Return a Lua table containing the entries of this document, section, or array.
The returned table is a snapshot; nested TOML sections remain read-only.

```cpp
table entries()
```

  
**Returns `table`:**

Entries table.

----

## Callbacks
No callbacks.

----
