# Arduino-Due-CAN-shield
My version of Arduino shield to control EV appliances with. 

V3 now includes 2x CAN bus chips with EEPROM chip to store configuration. There are 2x relays that control charger or DCDC with option of disabling vehicle when charging. 
There is now sensing of EVSE PP pin added with DUE pulling CP signal to correct resistance.
There are 2x analog inputs for use with either Hall current sensors or throttle signal. 
Various outputs with open collector signal can be used to control relays or LEDs.
I also added pins to source PWM outputs.
I added pads for power supply to use either a diode from 12V direct or use a stable 12V regulator.
