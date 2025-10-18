# Garmin Autopilot module
The module is designed for use with Mobiflight or similar software.  
PCB schematic and STL files are not distributed at the moment.  

## Etsy product link:
https://www.etsy.com/listing/4380274006/flight-sim-garmin-autopilot-module-usb-c

## PCB layout 
- 74x4067 multiplexer for 14 buttons inputs (12 hardware buttons + 2 encoder buttons)
- Two 74hc595 8-bit shift registers chained together for 16-bit output (12 LEDs)
- Three rotary encoders for HDG, ALT and Wheel inputs
- SMD LED lights and resistors for a compact footprint
- 2.54mm 1-line connector line can be soldered directly or used with pin header

## Arduino Nano board pinout
D2-D5   -> S0..S3 signals for 74x4067 MUX  
D6 -> Shift register LATCH  
D7 -> Shift register CLOCK  
D8 -> Shift register DATA  
D9/D10  -> HDG rotary encoder  
D11/D12 -> WHEEL rotary encoder  
A0/A1   -> ALT rotary encoder  
A2 -> Data pin for 74x4067 MUX  
D13, A3-A7 -> Unused  

