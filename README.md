# USBCRP2040MIN
Modified version of the Raspberry Pi (Trading) Ltd. RP2040 Minimal design 
example.

The original USB (B) Micro receptacle has been replaced with a USB C receptacle. 
KiCAD 6.0 has a foot print for the DX07S016JA1R1500 from JAE, and was used here. 
This receptacle breaks out the CC1, CC2, SBU1, and SBU2 pins, but only has the 
D+ and D- pins for USB 1.1 or USB 2.0 data rates. 

SBU1 and SBU2 are broken out, via bridged jumpers, to GPIO1 and GPIO0. CC1 
and CC2 are tied to ground via 5.1k Ohm resisters as required of a UFP for the 
USB C spec, and are also connected, again via bridged jumpers, to GPIO21 and GPIO22.

VBUS, as well as GND are routed to a second 1x2 .1 inch pitch header.

This is intended to be used for prototyping micro controller to micro 
controller communication over the SBU1 and SBU2 pins on the USB C receptacle. 
This does not impliment proper USB C DRP signaling, and may have problems 
acting as a host for other USB devices