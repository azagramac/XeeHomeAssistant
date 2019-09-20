![GitHub top language](https://img.shields.io/github/languages/top/azagramac/XeeHomeAssistant.svg) ![GitHub last commit (branch)](https://img.shields.io/github/last-commit/azagramac/XeeHomeAssistant/master.svg)

# Xee
<p align="center">
        <img src="logo_xee.png" alt="PNG" height="180px" />
         <img src="logo_ha.png" alt="PNG" height="180px" />
</p>

## Requirements
- Home Assistant installed and configured on your server
- Device "**[XeeConnect](https://www.midas.es/midas-connect)**" installed and configured in your car



## Example
<p align="center">
        <img src="example.png" alt="PNG" height="720px" />
</p>


## Setting
- Copy the file "*configuration.yaml*" into the configuration directory of your HA.
- Edit lovelace by code.
```
    title: Casa
    views:
      - badges: []
        cards:
          - entity: weather.casa
            type: weather-forecast
        path: default_view
        title: Home
      - badges: []
        cards:
          - entities:
              - sensor.car_lock
              - sensor.car_speed
              - sensor.car_fuel
              - sensor.car_battery
              - sensor.car_pressure
              - sensor.car_total_km
              - sensor.car_update_date
              - sensor.car_engine_state
              - sensor.car_latitude
              - sensor.car_longitude
            show_header_toggle: false
            theme: default
            title: Audi A4 State
            type: entities
          - entity: camera.generic_camera
            type: picture-entity
        icon: 'mdi:car'
        path: car_view
        title: Car

