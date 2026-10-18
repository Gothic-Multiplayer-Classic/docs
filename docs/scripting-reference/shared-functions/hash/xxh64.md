---
title: 'xxh64'
---
# `function` xxh64 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Return the XXH64 hash of the input string as lowercase hexadecimal text.

## Declaration
```cpp
string xxh64(string input, number seed)
```

## Parameters
* `string` **input**: Input bytes to hash.
* `number` **seed**: Integer seed from 0 to 4294967295. (Optional, defaults to 0.)
  
## Returns `string`
Lowercase hexadecimal hash string (16 characters, including leading zeros).
