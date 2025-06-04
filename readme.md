# Setup

Add bluepad32 url to board manager in arduino-cli.yaml

```yaml
board_manager:
  additional_urls:
    - https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
    - https://raw.githubusercontent.com/ricardoquesada/esp32-arduino-lib-builder/master/bluepad32_files/package_esp32_bluepad32_index.json
```

Then update the core

```bash
arduino-cli core update-index
arduino-cli core search bluepad
arduino-cli core install bluepad32:esp32
arduino-cli board listall | grep bluepad
```


Then build

```bash
make compile
make upload
make monitor
```
