---
title: Individual -- Subsystem Verification
---

"Testing can show the presence of errors, but not their absence"  
\- Edsger Dijkstra, computer scientist (1930-2002)

> **This is an individual homework assignment** but you may work with others to determine how to complete the assignment.  All work demonstrated in checkoff must be completed by you on your own board.

## Objectives

In this assignment, you will test your subsystem design for the individual subsystem(s) assigned to you on the block diagram for your team project. You must individually demonstrate proficiency in:

1. Powering up your board and circuit
1. Demonstrating valid wiring and power for 8-pin team daisy-chain headers.
1. Showing your circuit functioning in the way it is intended

## Resources

* [PCB Fabrication Process](https://embedded-systems-design.github.io/asu-pcb-fabrication-process/) on the Embedded Systems Design Resources Blog
* [Peralta 103 Resources](https://embedded-systems-design.github.io/peralta-103-resources/) on the Embedded Systems Design Resources Blog (includes links to manuals for the oscilloscopes and function generators in PRLTA 103)
* [Soldering and Desoldering Tips and Tricks](https://embedded-systems-design.github.io/soldering-and-desoldering-tips-and-tricks/) on the Embedded Systems Design Resources Blog
* [The "Soldering Is Easy" Complete Comic Book](https://mightyohm.com/blog/2011/04/soldering-is-easy-comic-book/)
* [Soldering Tutorial for Beginners Five Easy Steps](https://www.youtube.com/watch?v=8lq85feAiLM) video
* Canvas discussion board

## Prior to Demonstration of Proficiency

*Complete all of the steps below prior to the demonstration of proficiency.*

> You must complete this assignment using a custom PCB designed by you from the individual **PCB Design** assignment. **You may not use a breadboard, perfboard, or evaluation board.**

1. Update your schematic and board design to match any changes which occurred prior to or after board manufacturing. *All documents must be up-to-date, easy to read, and must be consistent with each other.*
1. Solder all headers and connectors to your subsystem PCB.
1. Solder your power connector and any associated components (e.g., voltage regulator, bypass capacitor) to your PCB.
1. **Do not solder or connect expensive components (e.g., your microcontroller) until you have verified power and ground are going to the correct pins on the PCB.** Connect power to the PCB and verify the following using a multimeter (handheld or benchtop).
    1. Correct voltage is coming into the PCB as expected.
    1. If your PCB includes a voltage regulator, the correct voltage is coming out of the regulator.
    1. Looking at your schematic, confirm that the correct power supply voltage is going to all of the correct pins on the PCB.
    1. If any mistakes are discovered, modify the PCB by cutting traces and soldering jumper wires until the design is correct. Update the schematic and/or PCB design in Cadence accordingly to account for these issues.
1. Solder one set of subsystem components to the PCB. If you have multiple subsystems on a single PCB, pick one to start with.
1. Verify the functionality of a subsystem. See demonstration of proficiency below for the tests you must run to confirm functionality of each subsystem.
1. Repeat steps 5 and 6 for each section/subsystem of your PCB design
1. If your board doesn't have your name etched in the copper, write your name in Sharpie somewhere in a blank area of your board. **This is required for verification.**

## Individual Demonstration of Proficiency

*You must complete the demonstration individually, either in office hours or in class if time permits.*

> You must complete this assignment using a custom PCB designed by you from your individual **PCB Design** assignment. **You may not use a breadboard, perfboard, or evaluation board.**

1. Open and talk through the block diagram and schematic for your subsystem PCB. *All documents must be up-to-date, easy to read, and must be consistent with each other.*
1. Show in the team block diagram assignment which subsystems have your name on them. These are the subsystems that you are responsible for.
1. Power up your physical subsystem PCB and show with a multimeter that the correct regulated voltage is connected to **all** of the correct pins (e.g., all of the VCC pins on the microcontroller) on the PCB
1. Demonstrate that your board has your name on it.
1. Demonstrate the correct functionality of your assigned subsystems on your PCB.
<a name="verification"></a>

    * PIC / ESP32
        * [x] Demonstrate using the MPLAB SNAP (PIC) or USB(ESP32) to successfully program your main microcontroller soldered to your PCB.
        * [x] Verify the 8-pin ribbon connectors are configured correctly
            * Pin 1 is unregulated power
            * Pin 8 is ground
            * Pin 2 is RX from upstream and TX to downstream

    * **One** of the following sets of tests:
        * Serial Sensor
            * [x] Demonstrate that the serial sensor is powered from the power supply.
            * [x] *(for chips with dual analog/serial functionality)* Verify that serial data is being sent to the microcontroller (using an oscilloscope if necessary)
            * [x] Demonstrate that changing sensor values can change the state of an output  (using a debug LED, debugger, or print statements for example)

        * Serial Actuator
            * [x] Demonstrate how the serial actuator is powered from the power supply.
                * Verify logic power going to actuator periperals.
                * Verify motor drive power going to actuator peripherals.
            * [x] *(for chips with dual analog/serial functionality)* Serial data is being sent from the microcontroller to the serial actuator's drive chip  (using an oscilloscope if necessary)
            * [x] Demonstrate that a changing input (e.g. from a debug pushbutton, SNAP debugger, or python command line) can change the state of an output.
                * For a DC motor, confirm bidirectional operation.
                * For a stepper motor, confirm the stepper can move a specified number of steps *or* at a specified rate. -->

        * OLED
            * [x] Verify the OLED is powered and can display a user-defined HMI screen.
            * [x] Verify that local user input  (e.g. from a debug pushbutton, SNAP debugger, or python command line)  changes the HMI screen state

        * Web Interface (MQTT)
            * [x] Verify that the ESP connects to the MQTT server and sends heartbeat messages.
            * [x] Verify that user input from the MQTT server is received by the ESP32 (using a debug LED, debugger, or print statements for example)
            * [x] Demonstrate that a changing input (e.g. from a debug pushbutton) publishes a message to the MQTT server.

        * Other
            * [x] Develop a custom plan with your professor in advance

<!-- * [x] Following successful ICSP, demonstrate your main microcontroller soldered to your PCB making an output change state (using a debug LED, for example -->
<!-- * [x] Following successful ICSP, demonstrate your main microcontroller soldered to your PCB making an output change state based on reading an input (using a debug pushbutton, for example) -->

<!-- > you may demonstrate all three at the same time -->

<!-- * [ ] send current sensor values as a data message over your daisy chain UART protocol. -->
<!-- * [x] Verify that a message sent from someone else over the daisy chain network changes the state of the actuator, according to its type
<!-- * [x] sends a message over the daisy chain network -->
<!-- * [x] Verify that a message sent from someone else over the daisy chain network updates the HMI appropriately. -->

## Canvas Submission

Please prepare this assignment in the following ways:

* [x] Follow the [Packaging a Cadence Schematic Project for Submission to Canvas](https://embedded-systems-design.github.io/packaging-cadence-files-for-submission/) instructions to create up-to-date PDFs of both your schematic and your PCB layout.
* [x] Add links to those pdfs to the schematic page of your "individual datasheet" github website.
* [x] Add (or update) .png or .jpg images of both your schematic and PCB design (top and bottom layer) to your schematic design page.
* [x] Use the "print to pdf" feature of your browser to create a pdf of your "schemtic design" page of your individual datasheet, showing these updates
* [x] Zip up the code used to verify your subsystem hardware functionality
    * In MPLabX, this can be done by right-clicking on your project name in the Projects window and select "Package".

> Your schematic and PCB PDFs must be legible in order to be graded. Rasterized (pixelated) images will receive a 0 if they are illegible.

Once completed,

* [x] submit your microcontroller code to Canvas.
* [x] submit the pdf of your updated schematic design page
* [x] submit an up-todate URL of your updated schematic design page

> Do not link to *living documents*, such as google docs, draw.io drawings, or google sheets.   Rather, contents the .pdf and .zip documents should be exported, saved in your repository, and hosted on the github site itself.

## Grading

| **Item**                        | **Points** |
| ------------------------------- | ---------- |
| Project Code                    | 50         |
| Microcontroller Programmability | 50         |
| Ribbon Cable Check              | 50         |
| Subsytem Checks                 | 150        |
| **Total**                       | **300**    |

## Frequently Asked Questions

**Q:** I discovered an error in my PCB. May I re-spin (re-manufacture) it?  
**A:** Generally, no. Most mistakes can be fixed by cutting traces and soldering wires onto your existing board. Please see the professors or TAs for help in reworking your PCB. Also, it is recommended that you still fix your design in Cadence so that it is ready for the Full PCB assignment later in the semester.

**Q:** Do we have to fabricate separate PCBs for each team member? Or could we submit a single PCB since they will be located in the exact same place and be connected together (with other team members schematics/blocks) anyways?  
**A:** Each team member needs to submit their own subsystem on a separate PCB. This is to ensure that every student has this skill (a learning outcome of the course). Breaking the board into subsystems also assists in the debugging process. You will combine your debugged subsystems into one final board for your team project.

**Q:** Is it possible to submit a video demonstration of our subsystem to canvas?  
**A:** No. We require live (non-video) demonstrations in order to confirm your proficiency with the entire process.

**Q:** As I was testing and putting the board together I found that somewhere, the voltage input was in contact with ground. I have made several big manual fixes to the board including drilling out a hole to make room for a connector. But just from what I can actually see, there are no solder bridges there. How do I fix this?  
**A:** Unfortunately PCBs are tough to debug without seeing live (or virtually). I highly recommend taking advantage of office hours. Having said that, places where you've manually modified the board after manufacturing are a common place where continuity problems occur. Using the continuity tester isn't helpful for locating shorts, so I'd recommend using the ohmmeter and look for a spot with lower resistance to get an idea of where the issue might be.

**Q:** Will taking a knife and manually isolating the pads work to fix continuity problems?  
**A:** Yes, you can use an exacto knife to isolate the pads, but I would only do that once you've eliminated other possibilities. A TA should be able to help more in office hours.

**Q:** I have soldered all my components and am now having a continuity problem. Now what?  
**A:** The best way to eliminate continuity problems is to test your before you have soldered on components, and then to test continuity after adding each component so you can trace the problem to your most recent action. Otherwise you will have to methodically desolder components from the board until the short goes away.

Also, sometimes incorrect footprints will cause shorts through the microcontroller. To protect your microcontroller and PCB, attach your microcontroller without power and check for shorts between power and ground. Only then should you power up the board.
