# wearable_cape_v02

Second version of a wearable sensing/actuating cape for the Augmented Attention Lab (June 2019)

## Changes from v01
- fixed wiring errors from filter circuits to minijack outputs
- removed unused resistors from filter design (two in final stage, one in input stage)
- swapped out resistor-based voltage divider for a dedicated 1.8V reference (MAX6100)
- breakout header for analog inputs
- widen power rail traces from battery to 11.1V source to amplifiers


## ToDos
- Add bypass capacitors to the active filters
- silkscreen labels for switch functionality and outputs
- breakout capability of mode switch, reset switch, & status LEDs
  - user leds, see: http://beaglebone.cameon.net/home/using-the-user-leds
- add additional 2-channel output for full access to all output channels
