# 8_channel_relay_ps2keyboard
arduino 8 channel relay module w/ ps/2 keyboard controller 

this project converts an uninterruptable power supply (ups) into an 8 channel relay box that is controlled by a ps2keyboard with an arduino uno.

hardware:

the battery & charging circuit is removed from a dead ups.

two sets of cold, hot & ground rails remain along with a thermal reset & a power cord.

the cold rails are segmented between the ac outlets.

a wire is solderd to each segment.

each wire connects to a relay depending on how you want it to work - no (normally open) or nc (normaly closed).

the cold wire from the thermal reset is desoldered from it's rail.

the cold wire is extended to reach one of the relays from an 8 relay module.

short wires connect the other side of the relays together in series.

corresponding pins from the relay module connect to arduino's 5v, grd & digital pins 4-11.

ps2keyboard jack is mounted on ups case & connects to 5v, grd & digital pins 3 (clk/irqpin) & 12 (data).

usb extender is mounted on ups case & connects to arduino usb.

9v power supply powers the arduino & 5v power supply connects to jd-vcc & grd on relay module (optoisolated side).

software:

arduino ide

ps2keyboard library included in arduino ide http://playground.arduino.cc/Main/PS2Keyboard.

flipRelay variable used to turn on & off the relays. 
