# wearable_cape_v02

Second version of a wearable sensing/actuating cape for the Augmented Attention Lab (June 2019)

## Changes from v01
- fixed wiring errors from filter circuits to minijack outputs
- removed unused resistors from filter design (two in final stage, one in input stage)
- swapped out resistor-based voltage divider for a dedicated 1.8V reference (MAX6100)
- breakout header for analog inputs
- widen power rail traces from battery to 11.1V source to amplifiers

# 23 MAY 2019 ~ WARNING! First Boards Ordered from Eurocircuits have wiring mistakes!
There was a serious wiring error in these boards, where the 10-pin row of headers that
connect downward into the Bela's analog inputs row and analog outputs row are reversed!
These headers do not correctly match up to the pins on the Bela and thus need to be
sliced and re-routed on the capelet board.

The pin ordering is flipped. So for example, on the Bela, the ground header for analog inputs is
on the bottom. But on the capelet it's at the top.

Likewise, on the Bela the analog outputs ground is on the right, on the capelet it's on the
left.

Possible Solutions (other than making new boards!):

1. Make a pin header/wire adapter that reverses the connections
2. Cut n rewire the capelet

See images/REV2.1_wiring_mistake for more info on the wiring issue...

## More errors
The mode select and halt switches are misnamed on the board, and potentially miswired to the breakout board header.

The actual wiring of the status header on the v2 board is...

1 ~ GND
2 ~ STATUS_LED
3 ~ D11
4 ~ SW_HALT
5 ~ D8
6 ~ MODE_SEL1 / 3v3
7 ~ D9
8 ~ MODE_SEL2



## ToDos (future work)
- Add bypass capacitors to the active filters
- silkscreen labels for switch functionality and outputs
- breakout capability of mode switch, reset switch, & status LEDs
  - user leds, see: http://beaglebone.cameon.net/home/using-the-user-leds
- add additional 2-channel output for full access to all output channels
