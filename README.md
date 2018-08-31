# hass-xiaomi-ir-climate
```yaml
climate:
  - platform: xiaomi_miio
    name: Name
    host: !secret xiaomi_ir_host
    token: !secret xiaomi_ir_token
    ircodes_ini: 'xiaomi_climate_codes/lanzkraft.ini'
    min_temp: 16
    max_temp: 32
    target_temp: 24
    target_temp_step: 1
    temp_sensor: sensor.temperature
    default_operation: "off"
    default_fan_mode: mid
    customize:
      operations:
        - cool
        # - dry
        # - heat
      fan_modes:
        - high
        - mid
        - low
```

ini file format is as follows
```
[off]
off_command = Z6XTAAgCAABJAgAAdAYAAF0RAAAyIwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0ISEBAQEBISEhISEBAQEBIQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBASEBIQEBAQEBISEhIQEhASEB

[cool]
low_16 = Z6XTAAQCAABNAgAAcAYAAFgRAAA4IwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0ISEBAQEBISEhISEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBASEhAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBASEBAQEBAQEBISEBIQEhASEB
low_17 = Z6XTAAQCAABNAgAAbwYAAFYRAAA4IwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0ISEBAQEBISEhISEhAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBASEhAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBASEBASEhASEB
low_18 = Z6XTAAQCAABNAgAAcAYAAFkRAAA1IwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA0ISEBAQEBISEhISEBIQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBASEhAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEhAQEBAQEBAQEBAQEBAQEBAQEBASEBISEhASEB
...
low_32 = ...
mid_16 = ...
...
mid_32 = ...
high_16 = ...
...
high_32 = ...
```
