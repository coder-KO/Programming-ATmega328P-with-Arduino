# Programming ATmega328P using 8MHz crystal

## Initial Connections
This basic setup will power up your IC and you'll be ready for bootloading.

![Initial Connections](/Circuit-Diagrams/Initial-Connections.png "Initial Connections")

|   ATmega328P      |                   on Breadboard                           |
|-------------------|-----------------------------------------------------------|
|Pin 1              |Vcc via 10K resistor                                       |
|Pin 7 and Pin 20   |Vcc                                                        |
|Pin 8 and Pin 22   |Gnd                                                        |
|Pin 9 and Pin 10   |8 MHz Crystal Oscillator                                   |
|Pin 9 and Pin10    |Gnd via 22pF Capacitors each                               |
|Pin 19             |Gnd Via a series combination of 220 Ohm resistor and LED   |


## Bootloading

Microcontrollers are usually programmed through a programmer unless you have a piece of firmware in your microcontroller that allows installing new firmware without the need of an external programmer. This is called a bootloader.

![Bootloading](/Circuit-Diagrams/Bootloading.png "Bootloading")


**IMPORTANT** - This will be a one time process.

To upload the bootloader, we'll make some extra connections to the basic power connections.

|Atmega         |   Arduino UNO     |
|---------------|-------------------|
|Pin 1          |    D10 (RESET)    |
|Pin 17         |    D11 (MOSI)     |
|Pin 18         |    D12 (MISO)     |
|Pin 19         |    D13 (SCK)      |

Now open Arduino IDE

1) Go to `File > Examples > ArduinoISP`

2) Go to `Tools > Board > Arduino UNO`

3) Select port from the `Tools > Port`

4) Upload the `ArduinoISP` sketch to your board

5) After successful uploading of the code go to `Tools > Board > and select Arduino Pro or Pro Mini`

6) Go to `Tools > Processor > and select ATmega328P (3.3V, 8MHz)`

7) Go to `Tools > Programmer > and select Arduino as ISP (Not ArduinoISP)`

8) Go to `Tools > Burn Bootloader`

This may take a while, and you'll be shown *Done Burning Bootloader*.

At this moment the LED on your breadboard and the default Arduino UNO LED will start blinking in sync.


## Programming the IC

You are now ready to Program your ATmega328P IC just like your arduino.

**IMPORTANT** - After bootloading, remove the ATmega chip form the Arduino UNO because now we will be using the Arduino board just as an ISP Programmer (In System Programmer).

![Programming](/Circuit-Diagrams/Programming.png "Programming")


Now remove all the 4 connections made in the bootloading process and do the following connections

|ATmega     |   Arduino     |
|-----------|---------------|
|Pin 1      |   RESET       |
|Pin 2      |   D0 (Rx)     |
|Pin 3      |   D1 (Tx)     |

Now, go to `Tools > Programmer > and select AVRISP mkll`

Go to `File > Examples > Basic > Blink`

Upload change the delays as you wish and upload the Sketch

You are now ready with your Minimal Arduino, you can now integrate whatever you want with your Microcontroller and make Custom Arduinos and reduce the size and cost of your projects.

*Also, while uploading sketches remember to use Arduino Pro or Pro Mini as the Board with Processor as ATmega328P (3.3V, 8Mhz) rather than Arduino UNO as we have used Pro Mini's bootloader because we have connected a 8MHz crystal.*

You can also checkout my instructable regarding the same [here](https://www.instructables.com/id/Programming-ATmega328-With-Arduino-IDE-Using-8MHz-/)
