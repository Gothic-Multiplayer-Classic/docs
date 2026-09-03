---
title: 'JSON'
---
# `class` JSON <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

JSON-backed key/value file returned by JSON.open().


## Properties
No properties.

----

## Methods
### key

Return the key at the given 0-based index or nil if out of range.

```cpp
string|nil key(number index)
```

**Parameters:**

* `number` **index**: Zero-based entry index.
  
**Returns `string|nil`:**

Key at index or nil.

----
### len

Return the number of entries in the file.

```cpp
number len()
```

  
**Returns `number`:**

Entry count.

----
### getItem

Get a value by key.

```cpp
any|nil getItem(string key)
```

**Parameters:**

* `string` **key**: Entry key.
  
**Returns `any|nil`:**

Value or nil if missing or invalid.

----
### setItem

Set a value by key and save the file.

```cpp
void setItem(string key, any value)
```

**Parameters:**

* `string` **key**: Entry key.
* `any` **value**: Value to store.
  

----
### removeItem

Remove a key and save the file.

```cpp
void removeItem(string key)
```

**Parameters:**

* `string` **key**: Entry key.
  

----
### clear

Remove all keys and save the file.

```cpp
void clear()
```

  

----
### open

Open a JSON file relative to the server data/internal directory.

```cpp
JSON|nil open(string relative_path)
```

**Parameters:**

* `string` **relative_path**: Path under the data/internal directory.
  
**Returns `JSON|nil`:**

File handle or nil on error.

----

## Callbacks
No callbacks.

----
