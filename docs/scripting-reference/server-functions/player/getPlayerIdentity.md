---
title: 'getPlayerIdentity'
---
# `function` getPlayerIdentity <font size="4">(server-side)</font>
!!! info "Available since version: 0.3.0"

Returns the player's stable OS installation identity, or nil if unavailable.
The 64-character lowercase hex value comes from the peer's GNS certificate.
It is self-asserted and can be spoofed by a modified client. OS reinstalls,
cloned installations, or changes to the OS identifier affect this identity.

## Declaration
```cpp
string|nil getPlayerIdentity(number player_id)
```

## Parameters
* `number` **player_id**: Target player id.
  
## Returns `string|nil`
Machine identity or nil.
