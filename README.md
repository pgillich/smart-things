# smart-things
Smart things is a project to make a Smart Home connecting to Internet of Things.

## Concept
Sensors/actuators --> WiFi microcontrollers --> IoT gateway --> IoT

## IoT Gateway
The heart of Iot Gateway is Domoticz running on Raspberry Pi.

### Install RPi
Below description is related to RPi 3 B+. More info about install:
* https://www.raspberrypi.org/downloads/raspbian/
* https://www.raspberrypi.org/documentation/installation/installing-images/README.md
* https://www.balena.io/etcher/

Install steps, using Windows:
1. Download and install Etcher (on Windows)
1. Download Raspbian with desktop and recommended software zip file (on Windows)
1. Flash Raspbian zip file to SD card, using Etcher (on Windows)
1. Remove SD card from Windows and put into RPi
1. Power on RPi
1. Connect PRi to Internet

### Install Domoticz
Below description is related to RPi 3 B+. More info about install:
* https://www.domoticz.com/wiki/Raspberry_Pi

Install steps on RPi:
* `curl -L https://install.domoticz.com | bash`

## WiFi uC
Below description is related to ESP8266. The selected firmware is: https://www.letscontrolit.com/wiki/index.php/ESPEasy

### Harware Variants
There are a lot of HW variants for ESP8266. Suggested variants:
* https://wiki.wemos.cc/products:d1:d1_mini for sensors and low voltage actuators (4GB, with direct USB flashing)
* https://www.letscontrolit.com/wiki/index.php?title=Sonoff_basic or similar for high voltage actuators (1GB, external serial flaser is needed, flasher pins must be soldered)

### Supported Sensors and Actuators
ESPEasy supports below sensors and actuators:
* https://www.letscontrolit.com/wiki/index.php?title=Devices

Sensors and actuators on top of WeMos D1 mini:
* https://wiki.wemos.cc/doku.php#d1_mini_shields

### Flash Firmware
More info about install:
* https://www.letscontrolit.com/wiki/index.php/ESPEasy#Get_started
* https://www.letscontrolit.com/wiki/index.php/ESPEasy#Loading_firmware
* https://github.com/letscontrolit/ESPEasy

More info about USB-serial drivers:
* WeMos D1 mini has built-in CH341 USB-serial adapter, dirver: https://wiki.wemos.cc/downloads
* FT232 is a cheap USB-serial adapter, driver: https://www.ftdichip.com/Drivers/VCP.htm
* CP2102 is another cheap USB-serial adapter, driver: https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers

Firmware flash steps, using Windows:
1. Download and install USB-serial driver
1. Configure Windows driver options by Driver Manager, if needed (for example: 115,200 baud)
1. Discover USB-serial COM port number by Driver Manager
1. Download and extract selected firmware zip
1. Run `flash.cmd`, set COM port, size, build num
1. After flashing, disconnect USB (power) cable


