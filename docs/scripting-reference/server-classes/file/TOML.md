---
title: 'TOML'
---
# `class` TOML <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Read-only TOML document returned by TOML.open(). Nested sections and arrays
are returned as TOML values. Use getOr() when a missing value should fall
back without replacing configured false.


## Properties
No properties.

----

## Methods
### has

Return true when a key or nested path exists. A string path uses dots as
separators; a table path can be used for dynamic or literal key segments.

```cpp
boolean has(string|table|number path)
```

**Parameters:**

* `string|table|number` **path**: Key, dotted path, path table, or array index.
  
**Returns `boolean`:**

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
### getOr

Return a value by key or nested path, or the fallback only when the value is
missing. This preserves configured false values.

```cpp
any getOr(string|table|number path, any fallback)
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
### open

Open a read-only TOML file relative to the server data/internal directory.

```cpp
TOML|nil open(string relative_path)
```

**Parameters:**

* `string` **relative_path**: Path under the data/internal directory.
  
**Returns `TOML|nil`:**

File handle or nil on error.

----

## Callbacks
No callbacks.

----
