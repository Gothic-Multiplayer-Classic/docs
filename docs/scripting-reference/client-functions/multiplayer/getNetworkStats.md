---
title: 'getNetworkStats'
---
# `function` getNetworkStats <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"
!!! note
    GNS connection quality is a recent fraction from 0.0 to 1.0, or -1 when unavailable; it is not cumulative packet loss.
!!! note
    Traffic rates are recent transport estimates. Pending and unacknowledged values are bytes, queue time is microseconds.

This function will return client network statistics.

## Declaration
```cpp
void getNetworkStats()
```

## Parameters
No parameters.
