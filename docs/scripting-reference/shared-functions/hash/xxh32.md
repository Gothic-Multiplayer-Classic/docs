---
title: 'xxh32'
---
# `function` xxh32 <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

Return the XXH32 hash of the input string as lowercase hexadecimal text.

## Declaration
```cpp
string xxh32(string input, number seed)
```

## Parameters
* `string` **input**: Input bytes to hash.
* `number` **seed**: Integer seed from 0 to 4294967295. (Optional, defaults to 0.)
  
## Returns `string`
Lowercase hexadecimal hash string (8 characters, including leading zeros).
