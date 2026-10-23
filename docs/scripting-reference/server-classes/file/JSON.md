---
title: 'JSON'
---
# `class` JSON <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

JSON-backed key/value store returned by `JSON.open()`.


## Properties
No properties.

----

## Methods
### keyAt

Return the key at the given one-based index or nil if out of range.

```cpp
string|nil keyAt(number index)
```

**Parameters:**

* `number` **index**: One-based entry index.
  
**Returns `string|nil`:**

Key at index or nil.

----
### count

Return the number of entries in the file.

```cpp
number count()
```

  
**Returns `number`:**

Entry count.

----
### get

Get a value by key.

```cpp
any|nil get(string key)
```

**Parameters:**

* `string` **key**: Entry key.
  
**Returns `any|nil`:**

Value or nil if missing or invalid.

----
### set

Set a value by key and save the file.

```cpp
boolean, table|nil set(string key, any value)
```

**Parameters:**

* `string` **key**: Entry key.
* `any` **value**: Value to store.
  
**Returns `boolean, table|nil`:**

True and nil on success; false and {message = string} on encoding or persistence failure.

----
### remove

Removes a key if present and persists the store.

```cpp
boolean, table|nil remove(string key)
```

**Parameters:**

* `string` **key**: Entry key.
  
**Returns `boolean, table|nil`:**

True and nil on success; false and {message = string} on persistence failure. In-memory changes are retained on

----
### clear

Removes all keys and persists the store.

```cpp
boolean, table|nil clear()
```

  
**Returns `boolean, table|nil`:**

True and nil on success; false and {message = string} on persistence failure. In-memory changes are retained on

----
### `static` open

Open a JSON file relative to the server data/internal directory.

```cpp
JSON|nil, table|nil open(string relative_path)
```

**Parameters:**

* `string` **relative_path**: Path under the data/internal directory.
  
**Returns `JSON|nil, table|nil`:**

Store and nil on success; nil and {message = string} on failure.

----

## Callbacks
No callbacks.

----
