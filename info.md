## MQTT Share Remote integration

Allow the sharing of entities between multiple instances of Home Assistant using MQTT. Primarily tested with binary_sensor, switch, light, and fan entities.

### Features

* Support binary_sensor, switch, light, and fan entities.
* Supports isy994_control events.
* Supports call_service events which means remote switch, light or fan can be controlled.
* It is important that entity_ids be unique across all Home Assistant instances.

### Usage

For the mqtt_share_remote integration you must specify the MQTT ```base_topic:```. The rest of the configuration is to specify the entities to share on the MQTT server. Look at the Include/exclude section of the [MQTT Statestream](https://www.home-assistant.io/components/mqtt_statestream/) component for details on how to configure this part of the configuration.

```yaml
mqtt_share_remote:
  base_topic: hass_share
  include:
    entities:
      - switch.studio_state
      - switch.studio_christmas_lights
```
