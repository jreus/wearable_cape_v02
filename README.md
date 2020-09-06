# wearable_cape_v02

Second version of a wearable sensing/actuating cape for the Augmented Attention Lab (June 2019)

## Changes from v01
- fixed wiring errors from filter circuits to minijack outputs
- removed unused resistors from filter design (two in final stage, one in input stage)
- swapped out resistor-based voltage divider for a dedicated 1.8V reference (MAX6100)
- breakout header for analog inputs
- widen power rail traces from battery to 11.1V source to amplifiers

# 23 MAY 2019 ~ WARNING! First Boards Ordered from Eurocircuits have wiring mistakes!

_IMPORTANT_
There was a wiring error in these boards, where the 10-pin analog inputs
and analog outputs headers on the capelet do not match the pins of the Bela.

The pin ordering is flipped. On the Bela A-INS ground is at the bottom,
on the wearable capelet it's at the top.

On the Bela A-OUTS ground is on the right, on the capelet it's on the
left.

Temporary Solution: make a little pin header wire connector with the wiring reversed



## ToDos (future work)
- Add bypass capacitors to the active filters
- silkscreen labels for switch functionality and outputs
- breakout capability of mode switch, reset switch, & status LEDs
  - user leds, see: http://beaglebone.cameon.net/home/using-the-user-leds
- add additional 2-channel output for full access to all output channels
