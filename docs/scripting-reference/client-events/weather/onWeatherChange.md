---
title: 'onWeatherChange'
---
# `event` onWeatherChange <font size="4">(client-side)</font>
!!! info "Available since version: 0.3.0"

This event is triggered when weather changes.

## Parameters
```c++
void onWeatherChange(number old_weather_type, number new_weather_type)
```

* `number` **old_weather_type**: Previous weather type. For more information, see [Weather Constants](../../shared-constants/Weather.md).
* `number` **new_weather_type**: New weather type from the same table.
