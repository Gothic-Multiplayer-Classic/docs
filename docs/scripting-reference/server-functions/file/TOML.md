---
title: 'TOML'
---
# `function` TOML <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Open a read-only TOML file relative to the server data/internal directory.

## Declaration
```cpp
TomlFile|nil TOML(string relative_path)
```

## Parameters
* `string` **relative_path**: Path under the data/internal directory.
  
## Returns `TomlFile|nil`
File handle or nil on error.
