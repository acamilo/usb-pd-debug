# Component Selection
![Block Diagram](block-diag.png)
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

## LDO
Can handle 20v. Can output 1.8 and 3.3 and 5v

Still not sure if I should chain these or have them all hang off of VBUS
When the bus is 5v, the 5v LDO will output around 4.5v?
* NCP718BSNADJT1G

## Power Switching
* TCK323G

# System Power Flow
![Power Diagram](power-flow.png)

## VIO voltage generation
VIO can be 1.8v The STM32 already runs at 3.3
We can switch between 3.3 and 1.8 using a resistor and a GPIO line connected to FB resistor network or just have VIO be a fixed 1.8v and switch between 3.3 and 1.8 by choosing to use or bypass the level shiftet.

## Aux PSU IN
Why not make this a second USBC with it's own PD chip?
The existing mac charger becomes a programmable PSU we can ask for power.





