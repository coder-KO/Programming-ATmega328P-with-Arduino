# Programming-ATmega328P-with-Arduino

In this repo I'll be covering a step by step guide of programming an ATmega328P IC (The same micro-controller present on Arduino UNO) using Arduino IDE and an Arduino UNO as a programmer to make yourself a custom Arduino, to make your projects more scalable and cost-effective.
I will cover two scenarios for Programming ATmega328P
1) Using external 16 MHz Crystal
2) Using external 8 MHz Crystal (Recommended for Low Power Application)

Here you can also read some basic information regarding the ATmega328P Microcontroller

# ATmega328P
**********
 ATmega328P is a high-performance Microchip picoPower (this is what the P stands for) 8-bit AVR RISC-based microcontroller combines 32KB ISP flash memory with read-while-write capabilities, 1024B EEPROM, 2KB SRAM, 23 general purpose I/O lines, 32 general purpose working registers, three flexible timer/counters with compare modes, internal and external interrupts, serial programmable USART, a byte-oriented 2-wire serial interface, SPI serial port, a 6-channel 10-bit A/D converter (8-channels in TQFP and QFN/MLF packages), programmable watchdog timer with internal oscillator, and five software selectable power saving modes. The device operates between 1.8-5.5 volts.


By executing powerful instructions in a single clock cycle, the device achieves throughputs approaching 1 MIPS per MHz, balancing power consumption and processing speed.


## Parametrics

|Name                               |Value                          |
|-----------------------------------|-------------------------------|
|Program Memory Type                |Flash                          |
|Program Memory Size(KB)            |32                             |
|CPU Speed (MIPS/DMIPS)             |20                             |
|CPU Speed (MIPS/DMIPS)             |20                             |
|SRAM (B)                           |2,048                          |
|Data EEPROM/HEF (bytes)            |1024                           |
|Data EEPROM/HEF (bytes)            |1024                           |
|Digital Communication Peripherals  |1-UART, 2-SPI, 1-I2C           |
|Capture/Compare/PWM Peripherals    |1 Input Capture, 1 CCP, 6PWM   |
|Timers                             |2 x 8-bit, 1 x 16-bit          |
|Number of Comparators              |1                              |
|Temperature Range (°C)             |-40 to 85                      |
|Operating Voltage Range (V)        |1.8 to 5.5                     |
|Pin Count                          |32                             |
|Low Power                          |Yes                            |

[Source: Microchip](https://www.microchip.com/wwwproducts/en/ATmega328P)