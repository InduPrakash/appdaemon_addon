# appdaemon_addon
This addon is based on https://github.com/hassio-addons/addon-appdaemon out of a need to apply local customizations to the official appdaemon package.

## Setup

1. Checkout this repository.
2. Download appdaemon's source code from https://github.com/AppDaemon/appdaemon/ and then copy `appdaemon-dev` here. If you name the folder anything 
else, then adjust the same in Dockerfile.
3. Manually apply the 2 patches from `rootfs\patches` folder.
4. Copy the entire folder to HomeAssistant's addons folder, a new addon named `AppDaemon 4 (modified)` should appear.

## Differences from the "Home Assistant Community Add-on: AppDaemon 4"

`Home Assistant Community Add-on: AppDaemon 4` installs `appdaemon` as a requirement, this addon instead installs the requirements of the `appdaemon` package.

Since the patches are being applied manually so that step has been removed from Dockerfile.

The Dockerfile has a new step to install appdaemon from the source using `python3 setup.py install`.
