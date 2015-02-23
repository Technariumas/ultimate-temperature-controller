# ultimate-temperature-controller
I've build a bunch of various temperature controllers and temperature sensor interfaces over the years. This one is to end the suffering. 

![3d render](https://raw.githubusercontent.com/Miceuz/ultimate-temperature-controller/master/ultimate-temp-controller.png)

Features:
 * Arduino compatible
 * Thermocouple input via MAX31855
 * Output to LCD via I2C interface
 * Relay output
 * Open collector output
 * RS485 interface 
 * 4 key keypad interface
 * SD card

The device can act as a standalone controller or as a slave / master on RS485 network. In case of standalone or master operation SD card is used to store temperature profiles. A profile can be selected via LCD/keypad interface. PID controller runs on the microcontroller and ensures the precise temperature control.
