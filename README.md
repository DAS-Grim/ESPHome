# ESPHome Configurations

ESPHome YAML configurations for small home-automation and arcade projects. Each file describes a separate device.

## Devices

| Configuration | Function |
| --- | --- |
| `air-wick-automatic-spray.yaml` | Controls an automatic spray device and provides an enable switch and adjustable spray schedule. |
| `data-east-arcade.yaml` | Selects a daily game and provides button controls for a Data East arcade cabinet. |
| `digi-reaper.yaml` | Controls two dimmable lights with pulse and flicker effects. |
| `question-block-lamp.yaml` | Controls a lamp and provides a repeating alert effect. |
| `street-fighter-2-arcade.yaml` | Provides button controls and startup sequences for a Street Fighter II arcade cabinet. |

## Hardware and frameworks

All configurations target the ESP32-C3 DevKitM-1. The four configurations other than `question-block-lamp.yaml` use the Arduino framework; the Question Block Lamp uses ESP-IDF. Check each YAML file for its GPIO assignments and required peripherals before connecting or flashing hardware.

## Validate and build

Install ESPHome and run commands from this directory, substituting the configuration you want to use:

```sh
esphome config air-wick-automatic-spray.yaml
esphome compile air-wick-automatic-spray.yaml
```

To compile, upload, and monitor a device with the ESPHome CLI, use `esphome run <configuration.yaml>`. Confirm the selected device, network settings, GPIO wiring, and any automated actions before uploading a configuration.