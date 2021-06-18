# Component Selection

## Processor
Datasheet shown in stream.
* STM32F078VB

## Hub
The hub in the stream is EOL, Picked a different one
* CY7C65621-56LTXC

## Level Shifters
Picked the shifters from glasgow
* SN74LVC1T45DCKR

## USB Mux
* FSUSB73UMX

## PD Chip
* FUSB302

# System Power Flow
![Power Diagram](power-flow.png)

## VIO voltage generation
VIO can be 1.8v The STM32 already runs at 3.3

## Aux PSU IN
Why not make this a second USBC with it's own PD chip?

## Power Switching
* TCK323G
