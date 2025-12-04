# Garmin G507 Autopilot module
The module has two hardware versions:  

a) **Nano version**: full functionality  
   has to be paired with Mobiflight or similar software.  
   
b) **Pro Micro version**: no LEDs, less flexibility  
   this version can be used as a stand-alone joystick version, no extra software needed.  
   It can be flashed to work with MobyFlight, but the joystick functionality will be lost.  
   *Later purchases of full version can be equipped with Pro Micro in Mobiflight mode*

PCB schematic and STL files are not distributed at the moment.  

## Etsy product link:
https://www.etsy.com/listing/4380274006/flight-sim-garmin-autopilot-module-usb-c

## Folder layout
- *Mobiflight* folder contains files to use in Mobiflight mode (both versions)  
- *Joystick* folder contains files for use with joystick version:  
  a) joystick definition file for X-Plane 11+  
     plug and play, copy the file into   
     <XPlane_root>\Resources\joystick configs  
  b) suggested configuration for MSFS - screenshot  

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

## Arduino Pro Micro board pinout
D0, D1 - unused  
D2..D5 - Multiplexer lines S0..S3  
D6,D7,D8 - Shift Register Latch,Clock,Data  
D9,D10 - HDG encoder  
D14,D16 - WHEEL encoder  
D15,A0 - ALT encoder  
A1 - Multiplexer In/Out  

## Joystick buttons layout
All the buttons are momentary buttons.  
Regular buttons are used as-is, each click of wheel movement is translated to corresponding button ON-OFF cycle.  

**Buttons 1..12**  
HDG APR NAV TRK AP FD LVL YD IAS VNAV VS ALT  

**Buttons 13,14**   
HDG-push, ALT-push  

**Buttons 15-20**  
HDG-left, HDG-right, WHEEL-up, WHEEL-down, ALT-left, ALT-right  


