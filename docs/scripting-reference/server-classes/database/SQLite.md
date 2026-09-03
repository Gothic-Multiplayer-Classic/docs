---
title: 'SQLite'
---
# `class` SQLite <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Synchronous SQLite database connection. SQLite.open() returns a connection
or nil plus a structured error. query() and execute() pass the SQL statement
unchanged to SQLite's prepared-statement API and bind positional ? parameters.
Successful results contain rows, columns, affectedRows, and lastInsertId.
Errors contain driver, code, message, and sqlState when available.


## Properties
No properties.

----

## Methods
### close

Close this connection. Connections are also closed during garbage collection.

```cpp
boolean close()
```

  
**Returns `boolean`:**

True when an open connection was closed.

----
### isOpen

Return whether this connection has not been closed.

```cpp
boolean isOpen()
```

  
**Returns `boolean`:**



----
### query

Execute one SQL statement. The statement is passed unchanged to SQLite and
positional ? markers are bound to the remaining arguments. Lua nil binds SQL
NULL; SQL NULL is returned as nil, so use the columns array when column
presence must be distinguished from a missing row key.

```cpp
table|nil, table|nil query(string sql, ... parameters)
```

**Parameters:**

* `string` **sql**: SQL statement.
* `...` **parameters**: Positional nil, boolean, number, or string values.
  
**Returns `table|nil, table|nil`:**

Result and nil, or nil and an error table.

----
### execute

Alias of query(), intended for statements which do not return rows.

```cpp
table|nil, table|nil execute(string sql, ... parameters)
```

**Parameters:**

* `string` **sql**: SQL statement.
* `...` **parameters**: Positional SQL parameter values.
  
**Returns `table|nil, table|nil`:**

Result and nil, or nil and an error table.

----
### open

Open an SQLite database under the server's data/internal directory. The
database option must be relative and cannot contain parent traversal. Use
:memory: for an in-memory database. Missing parent directories are created
when create is enabled. Foreign-key enforcement is enabled by default.

```cpp
SQLite|nil, table|nil open(table options)
```

**Parameters:**

* `table` **options**: database, readOnly=false, create=true, foreignKeys=true, busyTimeout=5000.
  
**Returns `SQLite|nil, table|nil`:**

Connection and nil, or nil and an error table.

----

## Callbacks
No callbacks.

----
