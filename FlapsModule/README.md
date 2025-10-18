# Flaps handle and indicator module
The module is designed for use with Mobiflight or similar software.  
PCB schematic and STL files are not distributed at the moment.  

## Etsy product link:
https://www.etsy.com/listing/4369657950/flaps-module-for-flight-sim-msfs-x-plane

## PCB layout 
- SMD LED lights and resistors for a compact footprint
- 2.54mm 1-line connector line can be soldered directly or used with pin header
- Multi-color LEDs for easy visual indication: 1x Green, 4x White, 2x Blue

## Arduino Nano board pinout
D2    -> Green LED (Power)  
D3/D4 -> White LEDs (1st notch of flaps)  
D5/D6 -> White LEDs (2nd notch of flaps)  
D7/D8 -> Blue LEDs (Full flaps)  
D10/D11 -> Up/Down hardware switch

## ToDo
Product improvement plans/ideas:

### Switch to different hardware
 - Arduino ProMicro (supports Mobiflight and Joystick firmware)
 - ESP32 S2/S3 (only supports Joystick firmware)

### Create joystick-style firmware: 
- No drivers needed
- No addtional software needed for Flight Sim integration
