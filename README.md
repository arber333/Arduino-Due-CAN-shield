# Arduino-Due-CAN-shield
My version of Arduino shield to control EV appliances with. 

V3 now includes 2x CAN bus chips with EEPROM chip to store configuration. There are 2x relays that control charger or DCDC with option of disabling vehicle when charging. 
There is now sensing of EVSE PP pin added with DUE pulling CP signal to correct resistance.
There are 2x analog inputs for use with either Hall current sensors or throttle signal. 
Various outputs with open collector signal can be used to control relays or LEDs.
I also added pins to source PWM outputs.
I added pads for power supply to use either a diode from 12V direct or use a stable 12V regulator.

V4 includes 12V relays. I figured poor arduino 5V regulator was overheating and DUE was sometimes tripping out. This way i removed the greatest load and DUE power is stable. Relay 2 can now transmitt 12V or GND signal. 
Also from V3 i noticed 2nd CAN bus transciever tx was connected to wrong pin51. This is now connected to pin53.
On the CP input i fitted mosfet transistor to pickup the PWM signal from EVSE and count pulses and measure duty on D7 pin. This way it is possible to count duty from EVSE and set charger power correctly.

Main points with latest V4.1.
I have corrected the issue with CAN chip 3V3 power supply.
I added B2P-VH header for CAN1 output which is more robust header. It will hold 3.96mm pitch connectors with wires up to 1mm2.
I have routed 12V power to relay contacts and provided solder points to connect either to GND or 12V. Also i power relais with 12V. This releases poor Arduino 5V regulator which had difficulties to cope with increased demand from 5V relay. 
I added 4 mosfets to PWM outputs and connected 3 of them to 12V. The last one on D2 port is conneced to 5V. So now i can directly connect PWM signal to drive chargers, DCDCs or car fans with that signal.
I also eliminated position for 12V regulator as a diode can perform some voltage aleviation as long as we use ordinary 3A diode. 

