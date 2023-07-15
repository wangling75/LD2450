ESPHome [LD2450](https://aliexpress.com/item/1005005584857890.html) mmWave Radar Sensor Custom Component

Edited yaml from: https://github.com/tsunglung/esphome-ld2450 for ESP32 to use the internal pull up resistors
Added Presence Sensor and Number of detected targets

## Installation
Set wifi_ssid and wifi_password in your esphome's secrets.yaml first

1. Place ld2450_uart.h into the custom_components of your esphome configuration folder
2. Create new device with the yaml in this repository

## Wiring
ESP32  | | LD2450
---------|-|-------|
5V      |<->| VCC
GND     |<->| GND
GPIO22  |<->| RX
GPIO21  |<->| TX

## Notice
1. Need to upgrade to firmware 1.2.23051810 - Bluetooth OTA available through [HLKRadarTool](https://www.pgyer.com/Lq8p) app
