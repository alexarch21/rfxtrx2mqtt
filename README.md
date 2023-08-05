# rfxtrx2mqtt

RFXTRX2MQTT is an MQTT bridge driver for the RFXCOM rfxtrx433 RF modem written in NodeJS and using the NODE-RFXCOM library.

## Install

First make sure NodeJS is installed. You can install NodeJS on a Raspberry Pi (or on other Debian-like systems) using the instructions here: https://pimylifeup.com/raspberry-pi-node

Clone this repository and run:

`npm install`

## Configuration

The driver is configured using a file called `configuration.yaml` that must be present in the directory of the driver. An example configuration is provided. Customize it as needed.

## Running

To start the driver go into the install directory and run:

`npm start`

## Scanning for RF devices

Calling `node ./rfxcom.js --scan` will scan the 433MHz band for devices with a supported protocol and will list the results as they come in. Adding the `--new` flag will only list devices that are not yet defined in your current configuration.yaml.

Calling `node ./rfxcom.js --stream` will show a realtime stream of RF devices as they communicate with the RFXCOM. This will also show command names for remote controls and switches, as well as device RSSI.

## Supported devices

TODO. 

Right now a lot of temperature, humidity, rain, wind and integrated weather station sensors (including Oregon Scientific). Also lighting2 protocol switches, remotes and relays (DIO, CHACON, KlikAanKlikUit, HomeEasy, etc) and lighting5 protocol (OTIO, Conrad RSL). More to come.
