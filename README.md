# Arduino-Due-CAN-shield
My version of Arduino shield to control EV appliances with. 

V3 now includes 2x CAN bus chips with EEPROM chip to store configuration. There are 2x relays that control charger or DCDC with option of disabling vehicle when charging. 
There is now sensing of EVSE PP pin added with DUE pulling CP signal to correct resistance.
There are 2x analog inputs for use with either Hall current sensors or throttle signal. 
Various outputs with open collector signal can be used to control relays or LEDs.
I also added pins to source PWM outputs.
I added pads for power supply to use either a diode from 12V direct or use a stable 12V regulator.

V4 includes 12V relays. I figured poor arduino 5V regulator was overheating and DUE was sometimes tripping out. This way i removed the greatest load and DUE power is stable.
Also from V3 i noticed 2nd CAN bus transciever tx was connected to wrong pin.
On the CP input i fitted mosfet transistor to pickup the PWM signal from EVSE and count pulses and duty for DUE. This way it is possible to measure duty from EVSE and set charger power correctly.
