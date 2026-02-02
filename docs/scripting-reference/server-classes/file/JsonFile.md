---
title: 'JsonFile'
---
# `class` JsonFile <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

JSON-backed key/value file returned by JSON().


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

Value or nil if missing/invalid.

----
### setItem

Set a value by key (autosaves on success).

```cpp
void setItem(string key, any value)
```

**Parameters:**

* `string` **key**: Entry key.
* `any` **value**: Value to store.
  

----
### removeItem

Remove a key (autosaves on success).

```cpp
void removeItem(string key)
```

**Parameters:**

* `string` **key**: Entry key.
  

----
### clear

Remove all keys (autosaves on success).

```cpp
void clear()
```

  

----

## Callbacks
No callbacks.

----
