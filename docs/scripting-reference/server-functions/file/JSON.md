---
title: 'JSON'
---
# `function` JSON <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Open a JSON file relative to the server data directory.

## Declaration
```cpp
JsonFile|nil JSON(string relative_path)
```

## Parameters
* `string` **relative_path**: Path under the data directory.
  
## Returns `JsonFile|nil`
File handle or nil on error.
