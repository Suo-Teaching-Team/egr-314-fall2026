---
title: 304 ICC7 -- Bluetooth with PSoC
---

> This assignment is a ***paired in-class checkoff***. An **individual** live demonstration is required. You may work in pairs (**one** partner), but must individually demonstrate your working breadboard.

## Introduction

The purpose of this ICC is to introduce students to the PSoC's capabilities at interacting with smartphones and PCs using the CySmart windows app and AIROC Bluetooth Connect App or Lightblue BLE phone app.

> This in-class checkoff requires advance work in order to complete it within one class period. Please read through the ICC, read all datasheets, and prepare your circuits as much as possible.

## Resources

* Videos
    * [Video Walkthrough](https://www.youtube.com/watch?v=rz6e8Ih1Sq0) (Thanks Christian!)
    * [Presentation from Dr. Patrick Kane](https://youtu.be/CVt31tGO92E) *(Infineon)*
* [AIROC Bluetooth Connect App - Mobile App](https://www.infineon.com/cms/en/design-support/tools/utilities/wireless-connectivity/airoc-bluetooth-connect-app-mobile-app/)
    * [Apple App Store](https://apps.apple.com/us/app/airoc-bluetooth-connect-app/id6443702288) version
    * [Google Play Store](https://play.google.com/store/apps/details?id=com.infineon.airocbluetoothconnect) version
* LightBlue Phone App *(optional)*:
    * [Apple App Store](https://apps.apple.com/us/app/lightblue/id557428110) version
    * [Google Play Store](https://play.google.com/store/apps/details?id=com.punchthrough.lightblueexplorer&hl=en_US&gl=US) version
* [AIROC CySmart 1.3](https://www.dropbox.com/s/ktxzxiipkfyypls/airoccysmart_1.3_Windows_x86-x64.exe?dl=0) (Windows program for bluetooth development / debugging)
* [PSoC 4100S Plus Datasheet](https://www.cypress.com/file/396611/download)
    * [Apple App Store](https://apps.apple.com/us/app/airoc-bluetooth-connect-app/id6443702288) version
    * [Google Play Store](https://play.google.com/store/apps/details?id=com.infineon.airocbluetoothconnect) version
* [CY8CKIT-042-BLE evaluation board main page](https://www.infineon.com/cms/en/product/evaluation-boards/cy8ckit-042-ble-a/), which includes the Prototyping Kit Guide, Schematic, and Example Code Installer
* [PSoC workshop slides, labs, and templates](https://www.dropbox.com/sh/iwzj4pjj6iwzwon/AABn9jsjRaj-Rx9nui4SWdnca?dl=0)
* Canvas discussion board
* Embedded Systems Design Website Tutorials
    * [Connecting to the PSoC](https://embedded-systems-design.github.io/connecting-to-the-psoc/)
    * [Bluetooth Tutorial I - Thermometer](https://embedded-systems-design.github.io/bluetooth-tutorial-1/)
    * [Bluetooth Tutorial II - Find Me](https://embedded-systems-design.github.io/bluetooth-tutorial-2/)
    * [Bluetooth Connection Issues](https://embedded-systems-design.github.io/psoc-bluetooth-connection-issues/)

## Parts Required

| **Item**                                                  | **Quantity** | **Detail**           |
| :-------------------------------------------------------- | :----------- | :------------------- |
| CY8CKIT-042-BLE-A PSoC 4 Prototyping Kit with BLE Dongle | 1            |                      |
| USB mini B cable                                          | 1            | included in PSoC kit |

## Prior to Class

1. Install the LightBlue phone app and AIROC Bluetooth Connect phone app, and the CySmart Windows app.

## Prior to Demonstration of Proficiency

### Part I: Sending data from the PSoC to a phone via Bluetooth

Complete [Bluetooth Tutorial I - Thermometer](https://embedded-systems-design.github.io/bluetooth-tutorial-1/) on the Embedded Systems Design website, with the following differences:

1. Before downloading your PSoC code, you will need to make some changes to the BLE functionality:
    1. In the Top Design, click on the BLE Block to open it.
    1. Navigate to the "Gap Settings" tab and replace "Thermometer" with "Thermometer XYZ" **where XYZ are your initials.**
1. In the ```main()``` function within ```main.c``` identify the function that measures temperature.
    1. From the menu select Edit → Find and Replace → Find in Files
    1. Find where that function is **defined.**

        > *Functions are often "declared" in ```.h``` files, so that other source files can find and reuse the same function. This usually consists of a "function prototype" where the name is declared, along with the variables it accepts and the type of data it returns, with a semicolon at the end.*
        >
        > *Functions are often "defined" in ```.c``` files. Function definitions are where the actual code goes, this time in curly braces ```{ }```.*

    1. Open up the file where it is defined, and read through the function. Identify the location where the temperature is converted from Celsius to Farenheit. Modify the code so that the BLE value returned is a constant value you define.

### Part II: Controlling your PSoC from a phone via Bluetooth

Complete [Bluetooth Tutorial II - Find Me](https://embedded-systems-design.github.io/bluetooth-tutorial-2/) on the Embedded Systems Design website, with the following differences:

1. Before downloading your PSoC code, you will need to make some changes to the BLE functionality:
    1. In the Top Design, click on the BLE Block to open it.
    1. Navigate to the "Gap Settings" tab and replace "Find Me Target" with "Find me XYZ" **where XYZ are your initials.**
1. On the Pins page in the Workspace Explorer, identify the name of the pin responsible for controlling the alert level of the LED
    1. From the menu select Edit → Find and Replace → Find in Files
    1. Search for the name of that pin within your current project.
    1. Identify the location where the pin is set. Look for ```MYPINNAME_Write(``` to see where the output is actually changed, using the name you found in the pins page in place of ```MYPINNAME```.

        > The pin is written within a ```switch``` statement. What are the three states, and what value determines how rapidly the pin flashes?

    1. Change the value that determines how long the LED flashes so that it flashes twice as fast as the default.

## Demonstration of Proficiency in Pairs

1. Demonstrate connecting to the "Thermometer" Module with your initials **from your PC** and subscribing to temperature alerts using [Bluetooth Tutorial I - Thermometer](https://embedded-systems-design.github.io/bluetooth-tutorial-1/).
1. Demonstrate connecting to the "Thermometer" Module with your initials from the **AIROC app** or the **LightBlue app** and subscribing to temperature alerts **with your custom temperature value**.
1. Demonstrate connecting to the "Find Me" module with your initials **from your PC** and changing the alert level from [Bluetooth Tutorial II - Find Me](https://embedded-systems-design.github.io/bluetooth-tutorial-2/).
1. Demonstrate connecting to the "Find Me" module with your initials **from the AIROC app** or the **LightBlue app** and changing the alert level from [Bluetooth Tutorial II - Find Me](https://embedded-systems-design.github.io/bluetooth-tutorial-2/).
1. Demonstrate that the PSoC LED flashes more rapidly with your code changes applied.

**A live demonstration by the end of class is required. No late demonstrations will be accepted.**

## Canvas Submission

**No Canvas submission is required.**

## Grading

| **Demonstration** | **Points** |
| :---------------- | :--------- |
| Demonstration 1   | 10         |
| Demonstration 2   | 10         |
| Demonstration 3   | 10         |
| Demonstration 4   | 10         |
| Demonstration 5   | 10         |
| **Total**         | **50**     |
