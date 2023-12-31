## This repo will no longer be maintained since there is a [PR](https://github.com/esphome/esphome/pull/5674) for native support in esphome and a better [library](https://github.com/uncle-yura/esphome-ld2450) till the PR to be merged

ESPHome [LD2450](https://aliexpress.com/item/1005005584857890.html) mmWave Radar Sensor Custom Component

![https://aliexpress.com/item/1005005584857890.html](https://ae01.alicdn.com/kf/S7be2047a5aa647a4b34e61f1c6df960e4/Radar-Sensor-Module-HLK-LD2450-Human-Presence-Motion-Radar-Sensor-Module-Non-Contact-Monitoring-Detector-Sensor.jpg)

Modified the yaml from [tsunglung](https://github.com/tsunglung/esphome-ld2450) for ESP32 to use the internal pull up resistors
Added Presence Sensor and Number of detected targets

## Installation
Set wifi_ssid and wifi_password in your esphome's secrets.yaml first

1. Place ld2450_uart.h into the custom_components of your esphome configuration folder
2. Create new device with the esphome-ld2450.yaml from this repository

## Wiring
ESP32  | | LD2450
---------|-|-------|
5V      |<->| VCC
GND     |<->| GND
GPIO22  |<->| RX
GPIO21  |<->| TX

## Dashboard Card
![image](https://github.com/Chreece/LD2450-ESPHome/assets/68458228/1b16a4a3-5386-4dca-a77c-c7864f38d9fe)

From HACS download the auto-entities, layout-card and Ploty Graph Card (all Frontend integrations)
Copy the code from dashboard_example.yaml into a new empty card in Home Assistant to grab all the LD2450 targets and present them in seperate cards (for title, the area of the device is used)

## Notice
1. Need to upgrade to firmware 2.04.23101915 - Bluetooth OTA available through [HLKRadarTool](https://www.pgyer.com/Lq8p) app
