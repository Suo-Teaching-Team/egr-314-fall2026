---
title: EGR 304/314 Course Sequence Requirements
---

_and Topic Coverage_

> Note: All requirements are subject to change

In addition to the engineering design specifications defined by your team, the design and fully-functioning prototype must meet the included below. **Exceptions to requirements are only allowed with your professor's prior written approval.** All projects developed by teams in the class will be demonstrated and graded live at the end of the semester.

## Project Requirements

### Maximum Project Budget

| 304              | 314              |
| ---------------- | ---------------- |
| \$60/team member | \$60/team member |

_Note_: Does not include development kits, components or PCBs from PRLTA, components acquired for free, or components purchased out of pocket.

### ECAD software

Each member of a team must use the same ECAD tool for team-based work.  This must be decided at the beginning of the semester, once teams are formed.

| 304                | 314                |
| ------------------ | ------------------ |
| Kicad _or_ Cadence | Kicad _or_ Cadence |

<!-- \* Altium is not available on ASU owned equipment. -->

### Components and Board Mounting

| 304                          | 314               |
| ---------------------------- | ----------------- |
| Thru-hole _or_ Surface Mount | Surface Mount$^1$ |

$^1$: Surface-mount components are ALWAYS required for ICs, passive elements (resistors, capacitors, etc), and discrete active components (transistors, etc). For resistors and capacitors, size [0805](https://eepower.com/resistor-guide/resistor-standards-and-codes/resistor-sizes-and-packages/#) or larger is recommended.  Mechanical connections to PCBs make terminal blocks, connectors, fuse terminals, etc, more robust and are permitted. Other exceptions are allowed with prior _written_ approval from your professor.

<!--
Transistor Technology 

| 304           | 314           |
| ------------- | ------------- |
| not specified | not specified |
-->

<!--
Digitally-switched actuator load minimum requirements[^8]

| 304 | 314 |
| --- | --- |
|     |     |

Analog Output  

| 304 | 314 |
| --- | --- |
|     |     |
-->

### Programming Language

| 304         | 314                     |
| ----------- | ----------------------- |
| C (MPLabX), | C (MPLabX), MicroPython |

### Final Printed Circuit Board

| 304                                   | 314                                             |
| ------------------------------------- | ----------------------------------------------- |
| Working board manufactured in Peralta | Working board manufactured by Peralta or JLCPCB |

### Maximum Board Dimensions

| 304       | 314       |
| --------- | --------- |
| 100x100mm | 100x100mm |

### Daughter Boards

> Daughter Boards are **not permitted** in EGR304.  [What is a daughterboard?](https://www.technipages.com/what-is-a-daughterboard/)

Please see the 314 Project Description for info on what daughterboards are permitted.

### Required Microcontrollers for Individual Homeworks

| 304                                                     | 314                            |
| ------------------------------------------------------- | ------------------------------ |
| Microchip PIC 18F57Q43 Curiosity Nano Development Board | Microchip PIC 18F47Q10 & ESP32 |

### Interrupts

| 304          | 314                                       |
| ------------ | ----------------------------------------- |
| not required | Interrupts (PIC) or Asyncio (Micropython) |


## Team Project

| **Item**                         | **304**             | **314**             |
| -------------------------------- | ------------------- | ------------------- |
| Team Composition                 | instructor-selected | self-selected       |
| Microcontroller Selection        | instructor-selected | team-selected       |
| Breadboarding                    | required            | required            |
| Interrupts                       | not introduced      | required            |
| Discussion Board                 | Canvas Discussions  | Canvas Discussions  |
| Project Management: File sharing | GitHub              | GitHub              |
| Project Management: Reporting    | GitHub              | GitHub              |
| Final Demonstration              | In-Class            | Innovation Showcase |

<!--
| Design Review                    | in-person           | in-person           |
### Individual Checkoffs & Homeworks

#### 304

+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| ##  | **Theme**                                    | **ICC**                                                              | **HW**                                          |
+=====+==============================================+======================================================================+=================================================+
| 1   | Basic Circuits                               | Adjustable Power Supplies,                                           | Create a Schematic of your Power Supply Circuit |
|     |                                              |                                                                      |                                                 |
|     |                                              | Multimeter                                                           |                                                 |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| 2   | Hello World (PSOC)                           | Get PSoC Programmed                                                  | Morse Code HW                                   |
|     |                                              |                                                                      |                                                 |
|     |                                              | Flash LED                                                            | Create a Symbol for PSOC and add to schematic   |
|     |                                              |                                                                      |                                                 |
|     |                                              | Add digital input                                                    |                                                 |
+-----+----------------------------------------------+----------------------------------------------------------------------$^*$+-------------------------------------------------+
| 3   | Digital Switching with Loads                 | Transistors(MOSFETS),                                                | PWM & H-Bridge from PSoC                        |
|     |                                              |                                                                      |                                                 |
|     |                                              | Back EMF & Diodes,                                                   | Add motor & H-Bridge to Schematic               |
|     |                                              |                                                                      |                                                 |
|     |                                              | H-Bridge                                                             |                                                 |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| 4   | Analog Amplification and Signal Conditioning | Analog I/O in PSoC                                                   | Op-Amps (inverting, noninverting)               |
|     |                                              |                                                                      |                                                 |
|     |                                              | Analog Sensors                                                       | Signal Generator                                |
|     |                                              |                                                                      |                                                 |
|     |                                              | Add analog to schematic                                              | Oscilloscope                                    |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| 5   | Filters and their applications in switching  | Passive Filters                                                      | Convert ICC parts to selected parts             |
|     |                                              |                                                                      |                                                 |
|     |                                              | Signal Generator                                                     | Design PCB of your selected subsystem           |
|     |                                              |                                                                      |                                                 |
|     |                                              | Oscilloscope                                                         | add UART breakout to schematic                  |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| 6   | Communication                                | PSoC UART                                                            | scanf and printf                                |
|     |                                              |                                                                      |                                                 |
|     |                                              | PSoC BLE                                                             | Web App Demo                                    |
|     |                                              |                                                                      |                                                 |
|     |                                              | https://youtube.com/playlist?list=PLIOkqhZiy83FM8mrUeyC4ESNMVkMQjj1r |                                                 |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+
| 7   |                                              |                                                                      |                                                 |
+-----+----------------------------------------------+----------------------------------------------------------------------+-------------------------------------------------+

### 314

TBD...

-->

### Concepts

#### Microcontroller

| **Item**                                            | **304**     | **314**                   |
| --------------------------------------------------- | ----------- | ------------------------- |
| GPIO                                                | introduced  | not explicitly covered    |
| ADC                                                 | introduced  | not explicitly covered    |
| PWM                                                 | introduced  | not explicitly covered    |
| DAC                                                 | introduced  | not explicitly covered    |
| UART bidirectional communication and string parsing | introduced  | refreshed (w/ interrupts) |
| SPI                                                 | not covered | introduced                |
| I$^2$C                                              | not covered | introduced                |
| Timers                                              | not covered | introduced                |
| Interrupts                                          | not covered | introduced                |

#### Circuits

| **Item**         | **304**             | **314**                               |
| ---------------- | ------------------- | ------------------------------------- |
| Voltage Dividers | introduced          | refreshed                             |
| Power Supplies   | linear              | switching                             |
| Passive Filters  | introduced          | not explicitly covered                |
| MOSFETS          | introduced          | refreshed (low-voltage discussion)    |
| BJTs             | introduced          | introduced (low-voltage applications) |
| Comparators      | discussed, not used | introduced                            |
| Op-Amps          | introduced          | not explicitly covered                |

#### Coding

| **Item** | **304**     | **314**    |
| -------- | ----------- | ---------- |
| C        | introduced  | expanded   |
| Python   | not covered | introduced |

#### Communication

| **Item**  | **304**     | **314**    |
| --------- | ----------- | ---------- |
| UART      | introduced  | refreshed  |
| SPI       | not covered | introduced |
| I$^2$C    | not covered | introduced |
| Bluetooth | not covered | introduced |
| WiFi      | not covered | introduced |

---------------------

## Permitted Analog Sensors

At least one analog sensor must meet the following two requirements in order to be approved to meet the sensor project requirement:

1. Does the device sense something in the outside world and output an analog signal?
2. Does the device require a custom-designed non-trivial hardware signal conditioning circuit (specifically, an active filter or amplifier circuit)?

Examples of **acceptable** analog sensors:

Underlying Technologies:

* Capacitive Sensors
    * Capacitive [_Pressure sensors_](https://en.wikipedia.org/wiki/Pressure_sensor), [_Proximity/Displacement Sensors_](https://en.wikipedia.org/wiki/Capacitive_displacement_sensor)
    * LC inductive/capacitive sensors (that use AC-domain signals), see the [_theremin_](https://en.wikipedia.org/wiki/Theremin) for an example
* Resistive sensors
    * Load-cells & wheatstone bridges (requires amplification and filtering)
* Inductive sensors
    * [_Linear Variable Differential Transformers_](https://www.te.com/usa-en/industries/sensor-solutions/insights/lvdt-tutorial.html) (LVDTs)
    * Coil-based electromagnetic field sensing solutions (like metal detectors)
* Piezoelectric Sensors (vibration, sound, high-frequency signals)
* Microphone with amplifier circuit
* Transistor-based sensors (with active op amps for filtering)
* EM-Domain Sensors (loops, coils, antennae)

Contexts / Applications:

* Microphones (piezoelectric, electret, condenser, etc) (usually need gain and filtering)
* Time of Flight Sensors (with custom circuitry, **no off-the shelf ultrasonic**)
* Single-IC sensor systems which require one or more external components to operate
* Analog accelerometers
* Temperature Sensors (thermocouples, thermopiles)

Examples of **unacceptable** analog sensors:

* Push button switches (too simple)
* Keypads (too simple)
* Sensors connected to a comparator (this produces a digital signal, not analog)
* Force-sensitive resistors or photocells utilizing a second fixed resistor to form a voltage divider as the only "signal conditioning" stage
* Potentiometers (already full range, no amplification or filtering typically needed)
* Sensors that need no additional amplification or filtering, such as Hall Effect sensors.
* Sensors with amplification gain less than or equal to 1 (don't need amplification.)
* Pre-packaged IR distance sensors with built-in daughter boards or signal conditioning built in, like [_this_](https://www.adafruit.com/product/1031). You may use plain IR emitter-detector pairs (like [_this_](https://www.amazon.com/Infrared-LED-Emitter-and-Detector/dp/B000TLSPNO/ref=sr_1_4?crid=W8JLMUDBYH8N&keywords=infrared+emitter+detector&qid=1641695477&sprefix=infrared+emitter+detector%2Caps%2C110&sr=8-4) or packages that are not signal conditioned, like [_this_](https://www.digikey.com/en/products/detail/onsemi/QRE1113/2175990?utm_adgroup=General&utm_source=google&utm_medium=cpc&utm_campaign=Shopping_Supplier_onsemi&utm_term=&utm_content=General&gclid=Cj0KCQiAieWOBhCYARIsANcOw0xdnn_-hsCLI8TEaz7LOPg2ZB5r_ynU5lt9dzH0909YG40jNiZTUV0aAmDvEALw_wcB) or [_that_](https://www.digikey.com/en/products/detail/tt-electronics-optek-technology/OPB742/374792)).

Note that you only need one acceptable analog sensor to meet the project requirement (meaning that you can still use push buttons, etc. but they won't count toward the analog sensor project requirement).

> See your professor if you are unsure whether your analog sensor is acceptable.

## Permitted Serial Sensors

At least one sensor must meet the following two requirements in order to be approved to meet the sensor project requirement:

1. Does the device sense something in the outside world?
2. Does the device communicate with the PIC via the approved serial protocol (eg SPI, I$^2$C, or UART)?

Examples of **acceptable** serial sensor subsystems:

* Digital temperature sensor
* Digital accelerometer
* Digital pressure sensor
* A number of identical sensors connected to a chain of [_parallel in, serial out (PISO) shift registers_](https://www.electronics-tutorials.ws/sequential/seq_5.html) (e.g., a number of individual buttons) (I$^2$C or SPI interface)

Examples of **unacceptable** sensor subsystems:

* Individual pushbutton switches
* Parallel interface keypad (unless it is interfaced through a [_PISO shift register_](https://www.electronics-tutorials.ws/sequential/seq_5.html))
* RFID reader (comes on a daughter board)
* GPS receiver (comes on a daughter board)
* Touch screen (comes on a daughter board)

Note that you only need one acceptable serial sensor subsystem to meet the project requirement (meaning that you can still use individual pushbuttons, etc. but they won't count toward the serial sensor subsystem project requirement).

> See your professor if you are unsure whether your serial sensor is acceptable.

## Permitted Actuators

At least one actuator must meet the following requirements in order to be approved to meet the actuator project requirement:

1. Does the device create motion in the outside world?
2. Does the device require a custom-designed non-trivial interface circuit, and/or a filtered analog output in order to connect with a microcontroller?
3. Does the control software do more than turn a single digital pin on and off?

Examples of **acceptable** actuators with complex control:

* Motors (brushed, brushless, stepper), linear actuators, or devices that use an electromagnetic field to move or change shape, _**connected to a complex motor driver IC**_ (including L298 and L293(D) family controllers)
* Speakers connected via a DAC or PWM through an amplification and filtering stage.
* A number of identical actuators connected to a chain of [_serial in, parallel out shift registers_](https://www.electronics-tutorials.ws/sequential/seq_5.html) (e.g., a number of individual LEDs, laser diodes, or vibrating motors)

<!-- - _**(304 only)**_ An analog RGB LED strip with 3 individually-controlled channels (**not** an individually-addressable LED strip) -->

Examples of **unacceptable** actuators:

* RC servos or other actuators that are controlled solely with a PWM signal (internal daughter board)
* Vibratory motors (no need for bidirectional control)
* Buzzers (simplistic control)
* Heating elements (no motion)
* Individual LEDs, light bulbs, and indicators, LCD screens or serial individually-addressable LED strips (no motion)

Note that you only need one acceptable actuator to meet the project requirement (meaning that you can still use RC servos, individual LEDs, etc. but they won't count toward the actuator project requirement).

> See your professor if you are unsure whether your actuator is acceptable.

<p></p>

> $^*$ **(304 Only)** Please see your instructor if you would like to consider using a motor for power generation rather than to create motion.

## Frequently Asked Questions

**Q:** When are we allowed to use commercial or breakout boards (e.g., from Sparkfun, Adafruit)?  
**A:** **IN EGR304**, You may _**not**_ use commercial or breakout boards in _**any**_ parts of the project that are graded per the specifications above. You are encouraged not to use commercial or breakout boards as an engineering student, but may do so if they are not part of the graded assignment. **Any Exceptions** must be made with prior approval from your professor (e.g., for components only available in a tiny surface mount package).

**Q:** Can we spend our personal money to go above the prototype budget, as long as we don't submit more than the maximum for reimbursement?  
**A:** Yes

**Q:** If part of our circuit uses a non-professor-approved commercial board (e.g., a motor controller), will we get any credit for our custom printed circuit board?  
**A:** See the EGR314 Project Description for more details.

**Q:** **(314 only)** Can we use more than one ESP32 in our system?  
**A:** Yes, absolutely!
