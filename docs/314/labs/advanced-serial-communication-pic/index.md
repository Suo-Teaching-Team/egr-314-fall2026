---
title: "Lab: Advanced Serial Communication"
---

> This assignment is a ***paired in-class checkoff***. An **individual** live demonstration is required. You may work in pairs (**one** partner), but must individually demonstrate your working breadboard.

## Overview

The purpose of this assignment is to build up a knowledge of serial communication involving either I$^2$C or SPI.  This assignment is intentionally vague because of the broad number of serial devices you can use to check off with, across two different protocols.

*An individual live demonstration is required. You may work within pairs (**one** partner), but should individually demonstrate your working breadboard.*

> ***This In-class checkoff requires advance work in order to complete it within one class period. Please read through all datasheets and prepare your circuits as much as possible.***

## Parts List

You will be working with one of the following devices:

| Part                                             | Digikey URL                                                                     | Datasheet                                                                                             |
| ------------------------------------------------ | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| AS5600-ASOM Hall Effect Sensor                   | [link][link1]                                                                   | [datasheet][link4]                                                                                    |
| TC74A4-3.3VCTTR Temperature sensor               | [link][link2]                                                                   | [datasheet][link5]                                                                                    |
| IFX9201SGAUMA1 Motor Driver                      | [link][link3]                                                                   | [datasheet][link6]                                                                                    |
| other$^1$                                        | -                                                                               | tbd                                                                                                   |
| Resistor                                         | various                                                                         | -                                                                                                     |
| ESP32 |                                                                                 | [datasheet](https://docs.espressif.com/projects/esp-hardware-design-guidelines/en/latest/esp32/esp-hardware-design-guidelines-en-master-esp32.pdf) |
|                              |  |


$^1$ if you would like to substitute your own serial device for project reasons, please see instructors for special approval.

> **Note:** A DIP-compatible surface mount carrier board was provided previously

## External Resources

- Tutorials on the ESP32
    - [ESP32 I2C communication information](https://randomnerdtutorials.com/esp32-i2c-communication-arduino-ide/)
    - [ESP32 SPI Communication Info](https://randomnerdtutorials.com/esp32-spi-communication-arduino/)
- TI I$^{\text{2}}$C Pullup Calculation [Application Report][pullupref]
- Programming
    - C programming tutorial on [pointers](https://www.tutorialspoint.com/cprogramming/c_pointers.htm)
    - [Serial Communication mini lecture][minilec]

- ESP32 documentation
    - [Hardware User Guide](https://docs.espressif.com/projects/esp-hardware-design-guidelines/en/latest/esp32/esp-hardware-design-guidelines-en-master-esp32.pdf)
    - [Design References](https://docs.espressif.com/projects/esp-idf/en/v4.2.4/esp32/hw-reference/index.html)
    - [Schematic](https://docs.espressif.com/projects/esp-hardware-design-guidelines/en/latest/esp32/schematic-checklist.html)
    - [Print Function](https://realpython.com/python-print/)

<!--
    - content/tutorials/pic/temp-and-humidity-sensor.md
-->

## Instructions


1. Browse the tutorials [above](#external-resources) to understand the basic flow of setting up communication.
1. If applicable, surface-mount solder your integrated circuit (IC) to a DIP compatible carrier board.
1. Use a breadboard to connect your IC to the ESP32 on the pins that support I$^2$C or SPI on each chip.

    > If implementing I$^2$C, ensure you have selected and are correctly using pull-up resistors.  This [reference][pullupref] is useful.
    
    > Be sure to reference the communication details needed for your selected sensor to aid in coding

1. Research your chip's communication protocol in its datasheet to understand at a minimum how many bytes must be exchanged, and in what order, in order to read a sensor value or activate an output.

    - If implementing SPI, you may need to ensure that input pins are connected to output pins for Ex. MOSI is connected MISO
    - If Implementing SPI, make sure you have selected and set up at least one pin for the "enable" lines to each device on your SPI network.  Remember that pins may be defined as "active low" ($\bar{\text{En}}$) or "active high" ($\text{En}$).  For more information about SPI data flow options, see the [Serial Communication mini lecture][minilec]



## Programming

1. If using I$^2$C, identify your chip's address and hard code it with a ```#define``` for quick reuse.
1. Research your chip's communication protocol in its datasheet to understand at a minimum how many bytes must be exchanged, and in what order, in order to read a sensor value or activate an output.
1. Research in the datasheet your chip's byte format representation for numbers, so that you can convert sensor values to more human-readable scales, such as Farenheit, Celsius, etc, or achieve a full range output (0-100%) of your actuator.
1. make sure to import any libraries used at the top of the file.
1. Add a variable used for holding either your sensor's current value or for storing your motor driver's command setpoint
1. Demonstrate how you can read from or command to your peripheral chip from the terminal or PuTTy by setting or reading this variable

    > If implementing SPI, remember to set enable active (is it "active low" or "active high"?) before you command the SPI functions, and to reset it when complete.


## Demonstration of Proficiency

*You must complete the demonstration individually, either in office hours or in class if time permits.*

1. Connect your ESP32 to a computer via USB. Open your VSStudio or Thonny project (NO Arduino IDE). Compile the program, and program your board.
1. If you have a sensor, demonstrate the following:
    1. that the sensor value shows up in your terminal or PuTTY
    1. that the value is properly scaled.
    1. that the reading changes when the stimulus changes

    or, if you have a motor driver

    1. That the motor driver responds to a change in the command variable
    1. that a value you write to your command variable is interpreted as a fractional change in the PWM value in one direction or (at least) as a binary change in a two-directional mode
    1. that a new value you write to your command setpoint variable translates to a change in state of the motor driver AND actuator.

## Grading

| **Demonstration**                                                        | **Points** |
| ------------------------------------------------------------------------ | ---------- |
| 2a. Reading Sensor or Commanding Actuator via debug variable             | 40         |
| 2b. Properly formatted current value (sensor) / command setpoint (motor) | 30         |
| 2c. Change in state registers correctly                                  | 30         |
| **Total**                                                                | **100**    |

[link1]: https://www.digikey.com/en/products/detail/ams-osram/AS5600-ASOM/4914332
[link2]: https://www.digikey.com/en/products/detail/microchip-technology/TC74A4-3-3VCTTR/443268
[link3]: https://www.digikey.com/en/products/detail/infineon-technologies/IFX9201SGAUMA1/5415542
[pullupref]: https://www.ti.com/lit/an/slva689/slva689.pdf?ts=1610914453139&ref_url=https%253A%252F%252Fwww.google.com%252F
[minilec]: https://www.dropbox.com/s/dhweh10xuvj2ofu/Serial%20Communication.pptx?dl=0
[link4]: https://www.digikey.com/htmldatasheets/production/1647438/0/0/1/as5600-datasheet.pdf
[link5]: https://ww1.microchip.com/downloads/en/DeviceDoc/21462D.pdf
[link6]: https://www.infineon.com/dgdl/Infineon-IFX9201SG-DS-v01_01-EN.pdf?fileId=5546d4624cb7f111014d2e8916795dea&ack=t
