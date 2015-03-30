# The Ultimate temperature controller
I've built a bunch of various temperature controllers and temperature sensor interfaces over the years. This one is to end the suffering. 

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

The device can act as a standalone controller or as a slave / master on RS485 network. 

## Standalone operation

Standalone controller is equiped with a LCD screen, a keypad and a SD card. Files containing temperature profiles can be stored on the SD card. A profile can be selected using the menu system via keypad and LCD interface. PID controller runs on the microcontroller and ensures the precise temperature control.

Power is controlled with a solid state relay. Open collector output is used to turn the SSR on and off. Alternatively an on-board mechanical relay can be used for power controll. 

Controller is powered by internal low power 12V SMPS.

## Slave operation

In slave mode no keypad and SD card is available, controller can be equiped with a more robust 7 segment LED screen for temperature readout. The slave controller sits on a RS485 network and listens for temperature commands from the master controller.

Slave has the same power output options as in standalone mode. 12V supply for the slave can be supplied by either a local SMPS or via UTP cable from the master. 

## Master operation

In case of master operation the master controller scans RS485 network for slaves. SD card is used to store temperature profiles. A profile can be selected via LCD/keypad interface for each of the slaves available on the RS485 network.

Master is not equiped with power switching options, but can provide 12V to slaves.

# The first prototype board

![3d render](https://raw.githubusercontent.com/Miceuz/ultimate-temperature-controller/master/temp-controller v1.0.0.jpg)

