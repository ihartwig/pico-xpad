# pico-xpad
Raspberry Pi Pico Xinput focused Macropad / Gamepad

## Hardware


## Firmware

The gamepad hardware supports running the GP-2040 firmware out of the box.

### Compiling custom GP-2040 firmware on MacOS

Steps to build the firmware on MacOS since this is not covered, but similar to, the steps provided in the project user guide for Linux.

```
brew update
brew install --cask gcc-arm-embedded
brew install cmake
brew install node@20
cd ~/repos
git clone https://github.com/OpenStickCommunity/GP2040-CE.git
git clone https://github.com/raspberrypi/pico-sdk.git --branch master
cd pico-sdk
git submodule update --init
cd ../
cd GP2040-CE
mkdir build
cd build
PICO_SDK_PATH=/Users/ihartwig/repos/pico-sdk cmake ..
PICO_SDK_PATH=/Users/ihartwig/repos/pico-sdk make
```

## Credits

Footprints reused from community designs:
* https://github.com/Kozova1/Macropad
* https://github.com/ebastler/kicad-keyboard-parts.pretty/
* https://datasheets.raspberrypi.com/rp2040/VGA-KiCAD.zip
* https://datasheets.raspberrypi.com/rp2040/VGA-PicoW-KiCAD.zip
