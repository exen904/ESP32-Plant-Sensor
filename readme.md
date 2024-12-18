# ESP-32 Plant Sensor for ESP-Home and HomeAssistant

This is a simple PCB to attach 6 capacitive moisuture sensors to a ESP32 for plant monitoring in HomeAssistant. The available MiFlora and Tuya clones with Zigbee were to expensive to purchase for all of my plants, so I chose this way. 

The PCB works with both V1.2 and V2.0 sensors and applys 5V as working voltage to make it compatible with either one. Connection to the sensors is made via JST 2.0 connectors. 

## Update
PCB has been updated to accomodate larger tolerances on the ESP footprint THT holes. My first protoytpe showed no errors, but I could confirm, that the tolerances on the THT holes are extremely tight. I adjusted this in the current version, so if you did not order PCBs, please use the current version. If you ordered PCBs from the first revision, you can take a chance at drilling the holes up but I dont really recommend that, as you can also break traces during that. 

## ESP Pinout
Please refer to my KiCad Footprint of the ESP I used for the pinout, as there are so many different ESP Devkits available. 

![Pinout](https://github.com/exen904/ESP32-Plant-Sensor/blob/master/Pictures/pinout.png)

## BOM
- 1x ESP32 Devkit with the correct pinout
- 6x JST B3B-XH-A (2.0mm vertical) connectors
- 4x M2x4 screws for securing the PCB in the bottom case

## Software
I run these with ESPHome, see my code in the code folder. Calibrate the values under `calibrate_linear` for each state of sensor dry and sensor 100% (sensor partly emerged underwater).

For the HomeAssistant side of things, I created a configuration.yaml entry, which ties each sensor to a plant entity. Example also linked in the code folder. Please do yourself a favour, and name your sensors in ESPHome better than I did.

## Pictures
![PCB render](https://github.com/exen904/ESP32-Plant-Sensor/blob/master/Pictures/ESP%20Plants.png)
![soldered PCB](https://github.com/exen904/ESP32-Plant-Sensor/blob/master/Pictures/plant4.jpg)