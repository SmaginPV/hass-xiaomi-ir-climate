# hass-xiaomi-ir-climate

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
