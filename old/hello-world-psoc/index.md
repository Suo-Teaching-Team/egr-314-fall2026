---
title: 304 ICC2 -- Hello, World! (PSoC)
---

> This assignment is a ***paired in-class checkoff***. An **individual** live demonstration is required. You may work in pairs (**one** partner), but must individually demonstrate your working breadboard.

## Objectives

To individually demonstrate proficiency in installing and running the Cypress PSoC Integrated Development Environment (IDE) tools to program sample code onto a microcontroller, and to modify that code to add additional functionality.

> This in-class checkoff requires advance work in order to complete it within one class period. Please read through the ICC, read all datasheets and prepare your circuits as much as possible.
## Resources

* Videos
    * [Video Walkthrough of ICC2](https://youtu.be/2vDoY1uVJ-M) *(Thanks to Jacob S)*
    * [Presentation from Dr. Patrick Kane](https://youtu.be/CVt31tGO92E) *(Infineon)*
* Scherz & Monk, Sections 3.3, 5.3, 7.3, 13.5
* [PSoC workshop slides, labs, and templates](https://www.dropbox.com/sh/iwzj4pjj6iwzwon/AABn9jsjRaj-Rx9nui4SWdnca?dl=0)
* [Canvas](https://canvas.asu.edu) discussion board
* [Demonstration](https://www.youtube.com/watch?v=0Mo9ACC5YW0&t=122s&ab_channel=FutureElectronics) of similar lab by Cypress/Infineon
* Embedded Systems Design Website Tutorials
    * [Connecting to the PSoC](https://embedded-systems-design.github.io/connecting-to-the-psoc/)

## Parts Needed

| **Item**                              | **Quantity** | **Detail**                |
| ------------------------------------- | ------------ | ------------------------- |
| CY8CKIT-042 *or* CY8CKIT-042-BLE PSoC | 1            | distributed in class |
| USB mini B cable                      | 1            | included in PSoC kit      |

## Completed Prior to Class

*Complete all of the steps below prior to the demonstration of proficiency.*

Note: You may use either a [PSoC 4 Pioneer Kit](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit) or a [PSoC 4 BLE Pioneer Kit](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit) to complete this assignment. You will be using the BLE Pioneer Kit for your team project.

1. If you don't have a PSoC 4 Pioneer Kit (BLE or regular), you can check one out from PRLTA 109, or buy one from Cypress ([BLE](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit), [regular](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit)).
1. If you have not completed it already, follow the instructions in the [EGR 304 Software Install](https://embedded-systems-design.github.io/egr304-software-stack/) page on the Embedded Systems Design website to download the full software stack, including PSoC Creator, the IDE for the PSoC microcontroller

    > *If you do not have a laptop that you can bring in for demonstration, you can use one of the computers in PRLTA 103*

## Completed in Class

1. Complete the [PSoC Hello World Lab](https://embedded-systems-design.github.io/psoc-hello-world/).
1. Practice measuring the supply voltage for the Pioneer Kit using an Agilent benchtop (not handheld) multimeter.<br> *Hint:* Check the Pioneer Kit Guide on the main product page on the Cypress website for information on where the power pins are.
    
    Next, you will modify the project to make a button enable or disable the blinking of the LED.

    > *Note:* The LED should blink at the same frequency as it did above, but only when the button is pressed.

1. Duplicate the project and add a Digital Input Pin connected to ```P0[7] SCB1:SPI:SS0, WAKEUP```. This is connected to ```SW2 P0[7]``` on the Pioneer Kit. On the BLE Pioneer Kit, ```SW2``` is connected to ```P2[7]```. Make sure the Drive mode of the input pin is set to ```Resistive pull up``` so

    > *Note:* Workspace explorer will have two projects open now, make sure you are in the correct project for pins, main.c etc. To select the appropriate project, navigate to it in the workspace explorer and select "activate project"

1. Finish modifying the project so that the LED blinks only when the button is pressed. For an example project that uses ```SW2```, see the element14 [oscilloscope project](https://community.element14.com/products/devtools/psoc4pioneerkit/f/forum/21143/psoc-4-pioneer-kit-community-project-17---2-channel-oscope-with-graphicslcd). To better understand how switches work and ways to mitigate "bouncing", learn about [switch debouncing](https://www.allaboutcircuits.com/technical-articles/switch-bounce-how-to-deal-with-it/).

## Individual Demonstration of Proficiency

In class, demonstrate the following **live** to a member of the Teaching Team by the end of class:

1. Connect the Pioneer Kit (or Pioneer BLE Kit) to your computer and launch PSoC Creator. Open your first Blinking LED project, compile, and download it to the Pioneer Kit.
1. Demonstrate your first Blinking LED project working correctly.
1. Open your second Blinking LED + Button project, compile, and download it to the (BLE) Pioneer Kit.
1. Demonstrate your second Blinking LED + Button project working correctly.

**A live demonstration by the end of class is required. No late demonstrations will be accepted.**

## Canvas Submission

**No Canvas submission is required.**

## Grading

| **Demonstration Item**                                  | **Points** |
| :------------------------------------------------------ | :--------- |
| 1. Successful download of project 1                     | 10         |
| 2. Successful demonstration of Blinking LED             | 10         |
| 3. Successful download of project 2                     | 10         |
| 4. Successful demonstration of Blinking LED with button | 20         |
| **Total**                                               | **50**     |

## Devices

| ![](image8.jpg)    | ![](image10.jpg) | ![](image7.jpg) |
| ------------------ | ---------------- | --------------- |
| Digital Multimeter | Oscilloscope     | Power Supply    |
| (optional)         | (Not Used)       | (optional)      |

| ![](image2.jpg)    | ![](image5.jpg)    | ![](image4.jpg) |
| ------------------ | ------------------ | --------------- |
| Function Generator | Waveform Generator | Soldering Iron  |
| (Not Used)         | (Not Used)         | (Not Used)      |

### Probes

| ![](image3.jpg) | ![](image6.jpg)    | ![](image1.jpg) |
| --------------- | ------------------ | --------------- |
| Oscilloscope    | Digital Multimeter | Soldering Iron  |
| (Not Used)      | (optional)         | (Not Used)      |

## Frequently Asked Questions

**Q:** May I use the [PSoC 4 BLE Pioneer Kit](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit) instead of the [PSoC 4 Pioneer Kit](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042/?utm_source=cypress&utm_medium=referral&utm_campaign=202110_globe_en_all_integration-dev_kit)?

**A:** Yes. If you are using the BLE Pioneer Kit, the LED pins are: Red = ```P2[6]```, Blue = ```P3[7]```, Green = ```P3[6]```. The switch is on ```P2[7]```.

**Q:** How do I choose the correct PSoC when creating a new project? The interface is slightly different from the tutorial.s

**A:** Click the "Target Device" radio button and choose "<Launch Device Selector...>" from the drop-down menu. Then, choose the part number that matches with your specific PSoC. (Hint: The part number of the microcontroller is written on the top of the chip, and is sometimes written near the chip on the printed circuit board in the silkscreen).

**Q:** How do I change the target device for a PSoC project that I already created?

**A:** In PSoC Creator, right-click on your project in the Workspace Explorer and choose "Device Selector...". Select the new device to match the part number printed on the circuit board.

**Q:** Something is wrong with my PSoC. I have followed the PDF instructions and videos online, but my LED still won't blink and PSoC Creator can't find a target to program. What should I do?

**A:** Try the following:

1. Borrow a classmate's PSoC and see if it works on your computer. If it does, you may have a bad PSoC

1. Come into office hours so the teaching team can help you debug.
