# Smart Things

Smart Things is a project to make a Smart Home connecting to Internet of Things.

## Concept

Sensors/actuators --> WiFi microcontrollers --> IoT gateway --> IoT

## IoT Gateway

The heart of Iot Gateway is Domoticz running on Raspberry Pi.

### Install RPi

Below description is related to RPi 3 B+. More info about install:
* https://www.balena.io/etcher/
* https://www.raspberrypi.org/downloads/raspbian/
* https://www.raspberrypi.org/documentation/installation/installing-images/README.md
* https://www.raspberrypi.org/documentation/configuration/wireless/desktop.md

Install steps, using Windows:
1. Download and install Etcher (on Windows)
1. Download Raspbian with desktop and recommended software zip file (on Windows)
1. Flash Raspbian zip file to SD card, using Etcher (on Windows)
1. Remove SD card from Windows and put into RPi
1. Power on RPi
1. Basic configuration
1. Connect PRi to Internet
1. Update Raspbian

### Install Domoticz

Below description is related to RPi 3 B+. More info about install:
* https://www.domoticz.com/wiki/Raspberry_Pi

Install steps on RPi:
* `curl -L https://install.domoticz.com | bash`

### Configuration

Below description is related to RPi 3 B+. More info about configuration:
* https://www.domoticz.com/DomoticzManual.pdf
* https://www.raspberrypi.org/documentation/configuration/wireless/

1. Set RPi as WiFi Access Point (not needed: DHCP server, dnsmasq, DNS server, bridge)
1. Set Domoticz retention config

## WiFi microconroller

Below description is related to ESP8266. The selected firmware is: https://www.letscontrolit.com/wiki/index.php/ESPEasy

### Harware Variants

There are a lot of HW variants for ESP8266. Suggested variants:
* https://wiki.wemos.cc/products:d1:d1_mini for sensors and low voltage actuators (4MB, with direct USB flashing)
* https://www.letscontrolit.com/wiki/index.php?title=Sonoff_basic or similar for high voltage actuators (1MB, external serial flaser is needed, flasher pins must be soldered)

### Supported Sensors and Actuators

ESPEasy supports below sensors and actuators:
* https://www.letscontrolit.com/wiki/index.php?title=Devices

Sensors and actuators on top of WeMos D1 mini:
* https://wiki.wemos.cc/doku.php#d1_mini_shields

### Flashing Firmware

See: [Flashing Firmware](doc/flashing.md)
