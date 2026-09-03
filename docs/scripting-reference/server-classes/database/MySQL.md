---
title: 'MySQL'
---
# `class` MySQL <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Synchronous MySQL database connection backed by MariaDB Connector/C.
MySQL.open() returns a connection or nil plus a structured error. query()
and execute() pass the SQL statement unchanged to the connector's prepared-
statement API and bind positional ? parameters. Successful results contain
rows, columns, affectedRows, and lastInsertId. Errors contain driver, code,
message, and sqlState when available.


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

Execute one SQL statement. The statement is passed unchanged to the connector
and positional ? markers are bound to the remaining arguments. Lua nil binds
SQL NULL; SQL NULL is returned as nil, so use the columns array when column
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

Open a MySQL connection. Timeouts are expressed in seconds and default to 10.

```cpp
MySQL|nil, table|nil open(table options)
```

**Parameters:**

* `table` **options**: database, username, password="", host="127.0.0.1", port=3306, charset="utf8mb4",
  
**Returns `MySQL|nil, table|nil`:**

Connection and nil, or nil and an error table.

----

## Callbacks
No callbacks.

----
