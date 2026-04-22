---
title: 'sscanf'
---
# `function` sscanf <font size="4">(shared-side)</font>
!!! info "Available since version: 0.3.0"

This function will split text according to a format string and return the parsed values.

## Declaration
```cpp
table|nil sscanf(string format, string text)
```

## Parameters
* `string` **format**: Format string where each specifier maps to a value. Supported specifiers: `d` (integer), `f` (number), `s` (string).
* `string` **text**: Input text to parse.
  
## Returns `table|nil`
Array of parsed values, or nil on parse failure.
