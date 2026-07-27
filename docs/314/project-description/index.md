---
title: EGR314 Spring 2025 Project Description
subtitle: Wildfire Response
---

> **Attention:** This is a living document, and will change over the course of the semester, with appropriate notice.

## Project Description

This semester, student teams will design and prototype embedded systems with sensing,
IoT, and microcontroller technologies to enhance wildfire detection and mitigation. These
systems will be integrated into either unmanned aerial vehicle (UAV) platforms or ground
based mini weather stations, addressing diverse sensing needs for real-time fire detection, long-term risk assessment, and emergency response support
.
<!--
## Daisy Chain Layout

![daisy chain block diagram](block-diagram.png)

Your team will be communicating over a custom UART daisy chain network as seen above.  All teams will use a 8-wire ribbon cable for power and communication between boards, with a common 2x4 IDC female header connected on both ends.  The following pinouts will be used across all boards.

For more details about the protocol, see the new [protocol page](protocol)

## Project Management
-->
### Individual Repositories

Individual team members will share their full subsystem design on Github and keep it updated throughout the semester.  This will consist of one or more public repositories consisting of the following:

* code
    * microcontroller code
    * code or setup files for PC or phone for connecting to their subsystem (if applicable)
* PCB design files
    * symbol library
    * footprint library
    * schematics
    * PCB layout
* a "datasheet" for their subsystem in the form of a website.  This will consist of:
    * a block diagram
    * schematic
    * software layout
    * Function Description.
    * other requirements listed in upcoming assignments

> Individual datasheets must be checked and verified for software and hardware functionality before individuals can connect their boards to their teammates' boards.

### Team Repositories

Each team will also create a team organization on Github for collecting and sharing team files.  This will consist of

* A Team report created and shared as a website consisting of the following pages
    * Introduction and Executive Summary
    * Design overview
    * team-level block diagram
    * Individual schematics, PCB designs
    * software implementation
    * links to individual teammates' Datasheets
    * other requirements listed in upcoming assignments

### PCB Design Software

Each team will be required to select a common ECAD tool across the team. This year, we will permit students to use either Cadence, Altium, Siemens Xpedition, although Altium is not currently supported on ASU-owned equipment.  **KiCAD is not permitted** on any individual or team designs in EGR314

> At this point we highly encourage teams to use Cadence or Xpedition. 

<!-- This semester we will be producing systems that can respond to the environment using serial sensing and actuation in your system for a mobile weather station. Each team will also broadcast their environmental data to the internet over WiFi using the MQTT protocol. -->

<!-- Your system must sense at least 2 of the following environmental conditions via at least at least 2 separate serial sensors: -->

<!-- - temperature
- humidity
- atmospheric pressure
- wind speed
- other modalities with instructor approval -->

<!-- In addition, you will need at least one motor controlled by a motor controller communicating over the I2C or SPI-based protocol. -->

<!-- > All sensing and actuation this semester will be accomplished using either I2C or SPI -->
<!--
## Daughter boards

In the Spring semester, we will permit daughter boards for peripherals for which a suitable surface mount version does not exist.  _It is your responsibility to obtain written instructor approval for all daughter boards used in your design._
-->
## Surface Mount Components

You are **required** to use surface mount components (or obtain written instructor approval if an exception is needed) for the following:

* Microcontrollers
* Voltage Regulators
* Passive Components (resistors, capacitors, inductors)
* Simple active components (LED's, transistors, op-amps, etc)

The following components _are not required_ to be surface mount, and **don't** need approval:

* Connectors (thru hole parts provide a better mechanical connection)
* Fuse holders

The following components _are not required_ to be surface mount, but  **need approval**:

* Daughter boards (see note above)

## Modular Individual Subsystems

Each individual is required to design, build, and verify their own subsystem as a standalone PCB.  The typical system will consist of four subsystems (one individual board per teammate in a 4 person team).
You will produce a modular, individually-designed system that can connect to your teammates' subsystems using a standards-based approach.  Individual subsytems will consist of:

* A 3.3V Switching regulator
    * Barrel Jack adapter for your 9V power supply
    * You are required to include two jumpers:
        * one to connect/disconnect "bus power" to your regulator
        * one to connect/disconnect your board-mounted barrel jack adapter to bus power


* In Circuit programming circuitry, compoents, and adapters for either:
    * ESP32: USB connector
   
* One of 3 individual functionalities:
    * sensing
    * actuation
    * bidirectional internet communication

    > you are not permitted to replicate functionality (subsystems) within a team.  Special subsystems require written approval from your instructor.  Subsystems must be materially different, using different chips, design processes, and accomplishing different functions

### UART Communication  

Individual subsystems are required to implement the communication protocol specified above (and in subsequent homework assignments).  It is up to the team to determine what data to pass and to whom, but a teammate will be required to demonstrate basic connectivity and data passing capabilities before being able to connect their device to  their team's daisy chain network.

## Team-Level Required Functionality

### Sensor Subsystem

At least one sensor that uses serial communication (SPI or I2C) to communicate to that subsystem's microcontroller is required.  
Please see the section at the bottom of the course sequence requirements page regarding permitted permitted [serial sensors](/3x4/course-sequence-requirements/#permitted-serial-sensors)

### Actuator Subsystem

At least one actuator that uses serial communication (SPI or I2C) to communicate to that subsystem's microcontroller is required. The actuator must be able to demonstrate **bidirectional control ability**.
Please see the section at the bottom of the course sequence requirements page regarding permitted [actuators](/3x4/course-sequence-requirements/#permitted-actuators).  For example, RC Servos, are **not permitted** in EGR314.
<!-- 
### Controller (Sensor and Actuator Subsystems)

A focus of this semester will be the implementation of a controlled response between the team's sensor(s) and actuator(s) subsystems. Possible applications for your controller could include position tracking applications, speed control applications, or more complex robotic interactions.

> We suggest using the extra peripheral pins on the class-wide modular connector for establishing high-speed communication between neighboring sensor and actuator subsystems.

### Human Machine Interface (HMI)

Your team will be responsible for developing a user interface that interacts with the whole system, using pushbuttons and a small OLED screen.  You will be required to permit a user to:

* View all sensor data in text and graphical form
* Control your actuator in a "direct-drive" mode
* Modify setpoints and parameters controlled on individual boards, including the system "controller"
* Toggle system GPIO debug pins (such as LEDs) across **ALL** individual subsystem boards.
* other functionality required in subsequent assignments throughout the semester.
-->
### Internet Communication

Your team will also be responsible for communicating with the internet over chosen Internet protocol.  

\* if your team has experience and interest to use a different protocol (such as http, websockets, etc), please obtain written approval from your instructor

### Team Definition

The team will be responsible for layout of their system-level plan, including

* decisions about what the system will be and do.
* decisions about overall sensing, actuation, and interfaces.
* overall software architecture defining system level messages and subsystem interactions

While individual teammates will implement these decisions in their own system.

### Individual Contribution

Each teammate will be responsible for developing a "datasheet" for sharing with their teammates.  It will becomposed of the following elements (details provided in individual assignments):

* Block Diagram
* Component Selection
* Schematic
* Bill of Materials and Hardware Order
* Software Description







Teams will separately verify both their system level software and hardware functionality.  Verification must be completed on finalized hardware to receive credit.

## Innovation Showcase

Your final project will be demonstrated at the Innovation Showcase, which is May 2, 2025. Your project will be evaluated both for functionality and for meeting specific requirements that will be shared with you through the Final Demonstration assignment.

> **UPDATED:** Please plan on being available 10am - 1pm for your team's final demonstration and the Showcase itself.


## Other Course Requirements

In addition to the engineering design specifications defined by your team, the design and fully-functioning prototype **must also** meet the budgetary, design, and instructor-defined requirements found in the following links. Exceptions to specifications are allowed with your professor's prior written approval.

* [Course Sequence Requirements](/3x4/course-sequence-requirements/)
* [Syllabus](/314/syllabus/)

> **Note:** Your project cannot be a replica of existing projects described on Instructables, Make Magazine, etc. nor the same concept discoverable via Google
