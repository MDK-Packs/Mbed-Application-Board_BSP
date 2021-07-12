# Mbed Application Board

## Overview

The Mbed Application Board board is designed for prototyping all sorts of devices, especially those including Ethernet, USB, and the flexibility of lots of peripheral interfaces. It carries a small DIP form-factor module ([Mbed LPC1768](https://github.com/MDK-Packs/Mbed-LPC1768_BSP) or [L-Tek FF-LPC546XX](https://github.com/L-Tek/FF-LPC546XX)) and offers various hardware interfaces for prototyping.

## Pinout

![Mbed Application Board Pin-Out](./lpc1768_pinout.png "Mbed Application Board Pin-Out")

| Socket Pin | Interface          | Function     |
|------------|--------------------|--------------|
| GND        |                    | Ground       |
| VIN        | DC IN              | 6 V - 9 V    |
| VB         | DC IN              |              |
| nR         |                    | nRESET       |
| P5         | LCD                | SPI MOSI     |
| P6         | LCD                | RESET        |
| P7         | LCD                | SPI SCK      |
| P8         | LCD                | A0           |
| P9         | ZigBee             | TX           |
| P10        | ZigBee             | RX           |
| P11        | LCD                | nRESET       |
| P12        | Joystick           | Down         |
| P13        | Joystick           | Left         |
| P14        | Joystick           | Center       |
| P15        | Joystick           | Up           |
| P16        | Joystick           | Right        |
| P17        | Analog In          | Analog In    |
| P18        | Analog Out         | Analog Out   |
| P19        | Potentiometer (l)  | AnalogIn     |
| P20        | Potentiometer (r)  | AnalogIn     |
| P21        | Servo motor header | PWM2         |
| P22        | Servo motor header | PWM1         |
| P23        | RGB LED            | Red          |
| P24        | RGB LED            | Green        |
| P25        | RGB LED            | Blue         |
| P26        | Speaker            | PWM Out      |
| P27        | Accel./TempSens    | SCL          |
| P28        | Accel./TempSens    | SDA          |
| P29        | ZigBee             | Status       |
| P30        | ZigBee             | nRESET       |
| D+         | USB                | USB D+       |
| D-         | USB                | USB D-       |
| TD+        | MagJack            | Ethernet TD+ |
| TD-        | MagJack            | Ethernet TD- |
| RD+        | MagJack            | Ethernet RD+ |
| RD-        | MagJack            | Ethernet RD- |
| IF+        |                    |              |
| IF-        |                    |              |
| VU         | USB                | 5 V USB Out  |
| VOUT       |                    | 3.3 V Out    |

## Schematics

- [Mbed Application Board schematic](./mbed-014.1_b.pdf)

## CMSIS-Drivers

This board support pack contains a CMSIS-Driver for the [VIO](https://arm-software.github.io/CMSIS_5/develop/Driver/html/group__vio__interface__gr.html) interface. This is a virtual I/O abstraction for peripherals that are typically used in example projects. The **Blinky** example uses this interface to create a running light with the four LEDs mounted on the board.

| VIO Signal | Board Connection |
|------------|------------------|
| vioLED4    | LED Red          |
| vioLED5    | LED Green        |
| vioLED6    | LED Blue         |

Refer to the [schematics](#schematics) for board connection information.
