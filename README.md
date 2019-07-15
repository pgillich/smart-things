# smart-things
Smart things is a project to make a Smart Home connecting to Internet of Things.

## Concept
Sensors/actuators --> WiFi microcontroller --> IoT gateway --> IoT

## IoT Gateway
The heart of Iot Gateway is Domoticz running on Raspberry Pi.

### Install RPi
Below description is related to RPi 3 B+. More info about install:
* https://www.raspberrypi.org/downloads/raspbian/
* https://www.raspberrypi.org/documentation/installation/installing-images/README.md
* https://www.balena.io/etcher/

Install steps using Windows:
1. Download and install Etcher (on Windows)
1. Download Raspbian zip file (on Windows)
1. Flash Raspbian zip file to SD card, using Etcher (on Windows)
1. Remove SD card from Windows and put into RPi
1. Power on RPi
1. Connect PRi to Internet

### Install Domoticz
Below description is related to RPi 3 B+. More info about install:
* https://www.domoticz.com/wiki/Raspberry_Pi

Install steps on RPi:
* `curl -L https://install.domoticz.com | bash`

