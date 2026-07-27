---
title: 304 HW2 -- PSoC General-Purpose Input-Output (GPIO)
---

> **This is an individual homework assignment** but you may work with others to determine how to complete the assignment.  All work demonstrated in checkoff must be completed by you on your own board.

## Objectives

To individually demonstrate proficiency in installing and running the Cypress PSoC Integrated Development Environment (IDE) tools to program sample code onto a microcontroller, and to modify that code and surrounding hardware to add additional functionality.

## Resources

* Scherz, P., & Monk, S. (2016). [Practical electronics for inventors, fourth edition.](https://www.amazon.com/Practical-Electronics-Inventors-Fourth-Scherz/dp/1259587541/ref=sr_1_1?s=books&ie=UTF8&qid=1470699914&sr=1-1&keywords=practical+electronics+for+inventors+4th+edition) New York: McGraw Hill. ISBN: 978-1259587542
* [CY8CKIT-042](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042/) [evaluation board](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/) [main page](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042/), which includes the Prototyping Kit Guide, Schematic, and Example Code Installer
* [CY8CKIT-042-BLE evaluation board main page](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/), which includes the Prototyping Kit Guide, Schematic, and Example Code Installer
* [CY8CKIT-142 BLE module main page](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-142/) ([digikey](https://www.digikey.com/en/products/detail/cypress-semiconductor-corp/CY8CKIT-142/5225792))([datasheet](https://www.infineon.com/dgdl/Infineon-CY8CKIT-142_PSoC_4_BLE_Module-UserManual-v01_00-EN.pdf?fileId=8ac78c8c7d0d8da4017d0ef062300159))
* [CY8CKIT-143A BLE module main page](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-143a/) ([digikey](https://www.digikey.com/en/products/detail/cypress-semiconductor-corp/CY8CKIT-143A/5825476?utm_adgroup=Battery%20Products&utm_source=google&utm_medium=cpc&utm_campaign=Dynamic%20Search_EN_Product&utm_term=&utm_content=Battery%20Products&gclid=CjwKCAjw9NeXBhAMEiwAbaY4lhyxt3pAzZqZrBieuURHvkGQ64wU6wWFvsmv4xKdSnfoEH9P3tj8hBoCccQQAvD_BwE)) ([datasheet](https://www.infineon.com/dgdl/Infineon-Quick_Start_Guide-UserManual-v01_00-EN.pdf?fileId=8ac78c8c7d0d8da4017d0efc0f08120a&utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-files))
* [PSoC workshop slides, labs, and templates](https://www.dropbox.com/sh/iwzj4pjj6iwzwon/AABn9jsjRaj-Rx9nui4SWdnca?dl=0)
* [Presentation from Dr. Patrick Kane](https://youtu.be/CVt31tGO92E) *(Infineon)*
* The Embedded Systems Design website
    * [KiCAD](https://embedded-systems-design.github.io/kicad/kicad-schematic-design/) schematic posts:
        * [Symbol Creation](https://embedded-systems-design.github.io/kicad-symbol-creation/)
        * [Schematic Capture](https://embedded-systems-design.github.io/kicad-schematic-capture/)
        * [Common Pin Types and their Meanings](https://embedded-systems-design.github.io/kicad-common-pin-types/)
    * [Cadence](https://embedded-systems-design.github.io/cadence/) posts
        * [Creating a custom library in Cadence](https://embedded-systems-design.github.io/creating-a-custom-library-in-cadence/)
        * [Creating a custom schematic symbol in Cadence](https://embedded-systems-design.github.io/creating-a-custom-schematic-symbol-in-cadence/)
        * [Creating a new project in Cadence](https://embedded-systems-design.github.io/creating-a-new-project-in-cadence/)
* KiCAD [Getting Started](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html) Pages on the KiCAD website:
    * Introduction to KiCAD: [Download and Install](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html#download-and-install-kicad)
    * [Basic Concepts and Workflow](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html#basic_concepts_and_workflow)
    * [Tutorial 1: Project](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html#tutorial_part_1_project)
    * [Tutorial 2: Schematic](https://docs.kicad.org/6.0/en/getting_started_in_kicad/getting_started_in_kicad.html#tutorial_part_2_schematic)
* Canvas discussion board

## Parts Needed

| **Item**                               | **Quantity** | **Detail**                                                                                                                                               |
| -------------------------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CY8CKIT-042 *or* CY8CKIT-042-BLE PSoC | 1            | supplied in class 8/29                                                                                                                                   |
| USB mini B cable                       | 1            | included in PSoC kit                                                                                                                                     |
| LEDs (optional)                        | 2            | (found in your kit)                                                                                                                                      |
| Pushbuttons                            | 2            | (found in your kit)                                                                                                                                      |
| 1/4 Watt Resistors (optional)          | various      | Appropriate for limiting current through the LED (you will use both onboard and offboard LEDs for different parts of the assignment).(found in your kit) |
| Breadboard                             | 1            | (found in your kit)                                                                                                                                      |
| Jumper Wires                           | multiple     | (found in your kit)                                                                                                                                      |

## Prior to Demonstration of Proficiency

*Complete all of the steps below prior to the demonstration of proficiency.*

### 1.0 Getting Started

In this assignment, you may use either the CY8CKIT-042 or CY8CKIT-042-BLE evaluation boards. It is recommended that you lay out the large components prior to wiring to ensure sufficient space on your breadboard.

1. Complete [ICC2 - Hello, World! (PSoC)](/304/304-icc-02-hello-world-psoc/).

### 2.0 Onboard Button, LEDs, and Morse Code

1. Study the following critical information and concepts:

    | **Critical Information and Concepts**                                        | **Importance**                                                                                                                                                                                         |
    | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
    | a.  Which ports on the PSoC the *onboard* LEDs and button are connected to. | Needed in order to control LEDs and read the button in software. Can be found in the Appendix of the Prototyping Kit Guide, or noted on the PSoC board itself.                                         |
    | b.  What International Morse Code is and how it was used.                    | Needed to understand the format and purpose of Morse Code. Summary can be found on [Wikipedia](https://en.wikipedia.org/wiki/Morse_code).                                                            |
    | c.  How to represent your initials in Morse code.                            | Needed in order to program an LED to display your initials in Morse Code. Can be found in this [Introduction on Morse Code](http://students.cs.ucl.ac.uk/schoolslab/projects/PY2/introduction.html). |

1. Connect the CY8CKIT-042 to your computer via USB
1. In PSoC Creator, create a new project for the CY8CKIT-042 (or CY8CKIT-042-BLE) and save it in a new workspace for Homework 2.
1. Create two (2) Digital Output pins and one (1) Digital Input pin in the Top Design.
    1. In the configuration pane, disable the hardware connection for each pin and set "Drive mode" to "Resistive pull up".
    1. In the Design Wide Resources > Pins window, connect the output pins to two different ports that map to LEDs onboard the CY8CKIT-042 (or CY8CKIT-042-BLE).
    1. In the Design Wide Resources > Pins window, connect the input pin to the port that maps to the user switch onboard the PSoC board.
1. Using a [Morse Code Translator](https://morsecode.world/international/translator.html), determine the pattern needed to send your initials (e.g., Dr.Jordan's are SJ) in Morse Code.
1. Open ```main.c``` and add code to the ```for(;;)``` loop that does the following:
    1. Turns the first LED on for 1 second, and then off for 1 second. The first LED should then remain off for steps b - d.
    1. Waits indefinitely for the button to be pressed (**not held**).

        > *Hint:* In the Top Design, right-click on one of the I/O pins and choose "Open Datasheet..." and scroll to the Application Programming Interface section to learn about the code used to read from an input pin. Then, use the code with a ```while()``` loop to wait for the button press.

    1. Turns the second LED on and off as needed to display your initials (first and last) in Morse Code. A "dot" should be 500 ms (so per the [rules of Morse Code](http://students.cs.ucl.ac.uk/schoolslab/projects/PY2/introduction.html), a "dot" would be represented with an LED being on for 500 ms and off for another 500 ms.
    1. Waits for 5 seconds before repeating steps a - d. This sequence should repeat as long as the microcontroller is powered.

## 3.0 Custom PSoC Symbol

1. Create a schematic for the CY8CKIT-143A BLE Module (Same footprint and pinout as the CY8CKIT-142). Following the resources for KiCAD or Cadence above,

    ![Figure: CY8CKIT-143A BLE Module](image3.jpg){style="max-height:200px;"}

    1. Create your own custom symbol for the CY8CKIT-143A BLE Module, including all connections for the 2x10 and 2x12 female headers found on the board. (Your board should include male headers.) **Do not create a symbol for the raw CY8C4248LQI-BL583 IC, you will be using the CY8CKIT-143A BLE module**
        * The symbol should include your initials in the symbol name *so that your **initials are visible** when the symbol is added to schematics.*
        * Pin Names should be identical to the names found in the CY8CKIT-143A manual
        * Pin type should be accurately specified in the symbol definition.<br>*KiCAD:* See [Common Pin Types and their Meanings](https://embedded-systems-design.github.io/kicad-common-pin-types/)
        * Specific pin numbering is not given in the datasheet. Number your pins in a consistent and orderly manner.
        * Save your new symbol into a copy of the custom library you created in HW1. Make sure you add that library to your HW2 project and update the project to have a project symbol table. This can be done in the symbol editor by selecting the library, clicking "Save As..." and saving it to your HW2 project folder. Make sure to "Add new project symbol table" in the process.
        * None of the other (non-header) pins should be added.
    1. Add the BLE module to a schematic.
    1. Add all necessary components for minimum viable circuit. This includes:

        ![Figure](image2.jpg){style="max-height:200px;"}

        * A power connector (e.g., a through-hole barrel jack) so you can connect an external power supply to the board.
        * 0.1 µF [bypass capacitors](https://embedded-systems-design.github.io/bypass-capacitor-basics/) on **every** power pin connecting to the processor module (unless otherwise specified in the datasheet).
        * HEADERx pins (where x is determined by the number of pins required to select the right header length) to connect parts of your teammates' circuits to your microcontroller
        * At least one debugging LED (through-hole or surface mount) with a current-limiting resistor (surface mount) attached to an unused microcontroller I/O pin.
        * At least one [pushbutton with a pull-up resistor](https://embedded-systems-design.github.io/pull-down-resistors/) (through-hole button, surface mount resistor) for debugging.

        > *KiCAD:* Wherever possible, use the "US" version of parts, including "R_US" instead of "R", "C_US" instead of "C", and "C_Polarized_US" instead of "C_Polarized", etc.

    1. Review this [short schematic checklist](https://embedded-systems-design.github.io/schematic-checklist/) to ensure your design isn't missing any common mistakes
1. Export your schematic to PDF and package your files for submission to Canvas

    > *KiCAD:* Follow the instructions for [Packaging KiCAD Files for Submission](https://embedded-systems-design.github.io/packaging-kicad-files-for-submission/)
    >
    > *Cadence:*Follow the instructions for [Packaging Cadence Files for Submission](https://embedded-systems-design.github.io/packaging-cadence-files-for-submission/)

## Individual Demonstration of Proficiency

You must complete a live demonstration individually, either in office hours or in class if time permits. Demonstrations can be done up to the last office hours on the due date noted in Canvas.  **No late demonstrations will be accepted**

1. Compile, download, and demonstrate your solution to Part 2.0 above, where the code should turn on and off an onboard LED, wait for the onboard button to be pressed, and then flash your initials in Morse code. Confirm the pattern using a [Morse Code Translator](https://morsecode.world/international/translator.html).

## Canvas Submission

Submit the items below to Canvas by the deadline given (in Canvas). **Do not submit screenshots.** *Do not submit links to Google documents.* It is your responsibility to ensure that your submission to Canvas was successful. Late Canvas submissions will be graded per the policy in the syllabus. No credit will be awarded for assignments not submitted via Canvas.

### PSoC Creator Files

Submit your packaged PSoC Creator workspace (right-click on the Workspace, select "Archive Workspace/Project..." from the contextual menu, and select a Minimal archive) in ZIP format to this assignment on [Canvas](http://canvas.asu.edu) by the deadline in Canvas. Do not submit links to Google documents.

### Schematic Files

Follow the instructions for packaging your schematic ([KiCAD](https://embedded-systems-design.github.io/packaging-kicad-files-for-submission/))([Cadence](https://embedded-systems-design.github.io/packaging-cadence-files-for-submission/)) to create a PDF and ZIP archive (including all library files) for your project. Submit **both** the PDF and ZIP archive as separate documents to this assignment on [Canvas](https://canvas.asu.edu) by the deadline in Canvas.

## Grading

| **Demonstration Item**                                                                      | **Points** |
| :------------------------------------------------------------------------------------------ | ---------- |
| Onboard button + morse code LED                                                             | 150        |
| PSoC Creator Archive of Workspace                                                         | 25         |
| Updated KiCAD / Cadence custom library included in KiCAD / Cadence Project ZIP file | 25         |
| Custom PSoC symbol added to custom library                                                 | 75         |
| Legible PDF of schematic included in submission                                             | 25         |
| **Total**                                                                                   | **300**    |

You must submit to Canvas **and** demonstrate your solution in order to receive credit. Late submissions and demonstrations will be graded per the policy in the syllabus, based on the last activity (Canvas submission or demonstration).

----------------------

## Frequently Asked Questions

**I can't find my workspace/project in PSoC Creator**

* C files, top design files, etc. are saved in project files
* Project files are saved in workspaces
* Workspaces are saved in the folder "PSoC Creator"
* The PSoC Creator folder can be found in the Documents folder of the user account
* Click ```*.cywrk``` to open a workspace
* Click ```*.cyprj``` to open a project

**How do I read an API?**

* ```void functionName(string descriptiveName)``
    * ```void``` = return value, it can be nothing (```void```) in which case it cannot be set or assigned to a variable, otherwise it will have a datatype such as ```uint8```, which can be stored in a variable of the same type
    * ```functionName``` = the name of the function, in pin and PWM read/writes, the first part (```Pin_*``` or ```TCPWM_*```) must be the name of the pin as defined in the top design (e.g. ```PIN_1``` $\rightarrow$ ```PIN_1_Read()```)
    * ```string``` = expected datatype of the parameter (the value passed into the function), other datatypes but not an extensive list: ```int```, ```uint8```, ```uint16```, ```uint32``
    * ```descriptiveName``` = a variable name describing what the expected value(s) are (e.g. ```*_Write``` has the parameter ```uint8``` value and the function call might be ```PIN_1_Write(50)```)

**What is a ```uint8```?**

* ```u``` = unsigned (only positive numbers)
* ```int``` = integer (only whole numbers)
* ```8``` = number of bits (8 bits =  0 - 2<sup>8</sup>-1)

**Is there an auto-formatter in PSoC Creator?**

* No, you must format your own code

**PSoC Creator can't find my device**

* Unplug the device and plug it back in
* Restart PSoC Creator
* Restart computer
* Try a different USB cable. (The cable that came with your kit is a special USB power + data cable. Many phone charger cables only provide power).
* Try a different computer

**Debug Target does not match/is not compatible with project's selected device**

* Unplug the board
* Find the onboard toggle switch and flip it (it should not be on BLE)
* Plug the board back in to see if it is resolved
* In PSoC Creator, right-click on the project in the workspace explorer and choose "Device Selector". Make sure CY8C4147AZI-S475 is selected. (Or, rebuild your project from scratch making sure to choose the correct device at the beginning).

**I'm missing a window in PSoC Creator/I accidentally closed a pane I needed!**

* In PSoC Creator, go to the Window menu and select "Reset Layout"

**PSoC Creator is building the wrong project!**

* Set your current workspace to default
* Set the active project to the project that needs to be built (right click on the project in the workspace window)

**Symptoms / Remedies**

*Debugging is a process of systematically double-checking your assumptions, because if everything was correct then it would be working. See below for some common symptoms and possible debugging remedies.*

*My PSoC port isn't working*

* Try a different port
* Check that the pin is set up correctly according to the assignment instructions
* The above is correct but still not working? Check the continuity of the pins to ensure the soldering quality is not causing the problem

*My program won't build (Code errors)*

* Does every open curly bracket (```{``) have a closing partner (```}``)?
* Does every statement (not condition or loop) have a semi-colon (```;``)?
* Were the functions called correctly?
* Are the loops/conditional statements written correctly?
* Read the error logs from the earliest error.
* Use the line numbers in the error logs to find out where, and the message to tell what the error might be (missing ```;``,```{``, ```}``, incorrect function name (```PIN_NAME_functionname()```), missing parenthesis around the if condition, missing parenthesis to signify a function, etc.)

*My program won't build (Top Design/Pin setup errors)*

* Are the pins and other components set up as instructed by the assignment?
* Check the connection(s) of components and the PWM module
* Check that the port/pin is able to do PWM through the pin/port setup dropdown

*My onboard LED/Button isn't working*

* Choose a different LED/button
* Ensure components were set up in PSoC Creator as instructed by the assignment
* Did you try the onboard LEDs or the LEDs near the CapSense pads? Either should work
* Test the pieces individually/one at a time (i.e. just the LED blinking, then turn on the LED when the button is pushed/held, etc.) before combining them

*My external LED/Button isn't working*

* Is there power?
* Is the circuit complete?
* Are the pins set up correctly in PSoC Creator?
* Are the anode/cathode of the LED in the correct orientation? (Current flows in the direction of the arrow in an LED).
* Check that there isn't a short in the circuit
* Check the resistor(s) being used are the correct ones
* Use a different external LED
* Use a different external button
* Is a wire broken?
* Try making the onboard LED work with the external button
* Try making the external LED work without the external button
* Try making the button work on its own using an onboard LED
* If none of the above resolve the issue, create a new PSoC project from scratch and redo the part

*My code doesn't work as it should*

* Confirm line by line what makes sense/is supposed to be there
* Swap/flip values (trial by experimentation)
* Try isolating pieces of the code to debug it a little bit at a time (i.e. just the LED flip, then just the dot of the morse code, etc.)
* Read the code aloud to someone even if they don't understand to find tiny human mistakes (see also: rubber ducking)
* Chances are the code does exactly what you tell it. So maybe you're not telling it what to do in the right order, otherwise, check your wiring for external components

*My LED on/off values are inverted?*

* Make sure your LEDs are set up correctly in PSoC Creator

*Nothing works/I've tried everything here*

* Try starting a new project and redo everything (carefully)

**Checklist**

| Item      | Description                                                                                                                                                                                                                          |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Soldering | Is it a good solder joint? (no bubble/balls of solder, solder isn't touching anything but the pin and the pad, can't see through the other side of the pinhole, nothing is loose/wiggling, solder joints are shiny rather than dull) |
|           | Do all pins have continuity? (test with multimeter)                                                                                                                                                                                  |
| Coding    | Is the code readable/well formatted? (makes debugging easier)                                                                                                                                                                        |
|           | Do you know what every line of code does? Does every line of code make sense? (makes understanding behavior easier)                                                                                                                  |
|           | Does every line function as it is intended? (avoid unexplainable behavior)                                                                                                                                                           |
|           | Do the variables have datatypes (make like match with like to avoid warnings and errors)                                                                                                                                             |
|           | Do the loops have entry/break conditions (excluding ```for;;```) (have conscious and complete control of loops)                                                                                                                            |
|           | Use read functions as intended: read, check, or save values                                                                                                                                                                          |
|           | Use write functions as intended: write values to pins                                                                                                                                                                                |
| Circuit   | Do all components function independently (to ensure no broken/dead pieces)                                                                                                                                                           |
|           | Are there any shorts?                                                                                                                                                                                                                |
| PSoC      | Configured pin names match names used in code?                                                                                                                                                                                       |
|           | Using pins that can provide the intended functionality?                                                                                                                                                                              |
|           | Everything is connected where it should be (line to pin, clock to PWM)                                                                                                                                                               |

