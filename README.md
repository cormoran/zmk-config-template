# cormoran's ZMK config template

## Local Development

```bash
mkdir zmk-workspace
cd zmk-workspace
git clone <your zmk-config>
cd <your zmk-config>
west init -l . --mf config/west-workspace.yml # It downloads dependencies under zmk-workspace/
# Or
# west init -l config # It downloads dependencies to zmk-workspace/<your zmk-config>/dependencies
west update --narrow
west zmk-build

# Build with debug
west zmk-build -S zmk-usb-logging

# Build specific firmware with debug mode and flash
west zmk-build -a <artifact name> -S zmk-usb-logging --flash
```

## Keymap

![Your keymap](./keymap-drawer/your_keyboard.svg)
