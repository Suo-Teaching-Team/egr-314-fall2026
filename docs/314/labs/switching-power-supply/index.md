---
title: "Lab: Switching Power Supply"
---

> This assignment is a ***paired in-class checkoff***. An **individual** live demonstration is required. You may work in pairs (**one** partner), but must individually demonstrate your working breadboard.

## Objectives

In this assignment, you will learn how to use a datasheet to properly design a switching voltage regulator. This voltage is one of the most common for embedded systems, and will be used in upcoming assignments as well as required for your project.

You must demonstrate with your partner proficiency in:

1. Designing switching voltage regulator circuits.
1. Using an oscilloscope to measure the no-load output voltage of a regulator.
1. Using an oscilloscope to measure regulator output voltage under load.

> This In-class checkoff requires advance work in order to complete it within one class period. Please read through all datasheets and prepare your circuits as much as possible.

Overview video provided by Sai Charan.  Thanks!

<iframe width="560" height="315" src="https://www.youtube.com/embed/uVkoz7sn10Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Resources

- Scherz & Monk, Chapter 11: Voltage Regulators and Power Supplies
- Scherz & Monk, Chapter 7: Hands on Electronics
    - Oscilloscopes Section <!--TODO-->
- Oscilloscope manuals for Peralta 103 <!--TODO-->
-   [BK Precision Triple-Output 30V, 5A Digital Display DC Power Supply (Model 1671)](https://www.bkprecision.com/products/power-supplies/1671A-triple-output-30v-5a-digital-display-dc-power-supply.html) ([manual](https://bkpmedia.s3.amazonaws.com/downloads/manuals/en-us/1671A_manual.pdf))

## Parts

| Part                              | Quantity | Details                                                                                          |
| --------------------------------- | -------- | ------------------------------------------------------------------------------------------------ |
| LM2575T-3.3G                      | 1        | ([datasheet][lm2575_datasheet]) / ([digikey][lm2575_digikey])                                    |
| 1N5819 Schottky Diode             | 1        | [digikey](https://www.digikey.com/en/products/detail/nte-electronics-inc/1N5819/11644402)        |
| 100uF, 50V Electrolytic Capacitor | 1        | [digikey](https://www.digikey.com/en/products/detail/nte-electronics-inc/NEV100M50DD/11651306)   |
| 330uF, 10V Electrolytic Capacitor | 1        | [digikey](https://www.digikey.com/en/products/detail/w%C3%BCrth-elektronik/860020273010/5727147) |
| 220uH Inductor                    | 1        | [digikey](https://www.digikey.com/en/products/detail/bourns-inc/RLB9012-221KL/1969608)           |

[lm2575_datasheet]: https://www.dropbox.com/s/1hda23itui68268/LM2575D2T-005.PDF?dl=0
[lm2575_digikey]: https://www.digikey.com/en/products/detail/onsemi/LM2575T-3-3G/1476700

## Prior to Demonstration of Proficiency

| **Critical Information and Concepts**                                                        | **Importance**                                                                                                                                                                                  |
| -------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| What is the minimum and maximum supply voltage                                               | Helps determine the operating limits of the device as well as the upper limit for *safe* operation of the device                                                                                |
| What is the Design procedure for a switching regulator? (see page 8 of the LM2575 datasheet) | The selection of inductance and capacitance plays a large role on the "startup" and "ripple" of your output.                                                                                    |
| What is the appropriate inductor for my application? (See page 13 of the LM2575 datasheet)   | See above explanation.                                                                                                                                                                          |
| What is the maximum current of my inductor (See the inductor datasheet)                      | "Exceeding an inductor’s maximum current rating may cause the inductor to overheat because of the copper wire losses, or the core may saturate." (Explained on page 17 of the LM2575 datasheet) |
| What is the correct diode to use? (Explained on page 10 of the LM2575 datasheet)             | "Since the diode maximum peak current exceeds the regulator maximum load current, the catch diode current rating must be higher than the maximum load current                                   |
| What is the correct voltage rating of my output capacitor?                                   | Output ripple in switching regulators can impact the minimum required voltage of your capacitor                                                                                                 |

1. Open the voltage regulator datasheet (link in the parts list) and construct the "Typical Application Circuit" shown on page 2 on your breadboard. 
3. Add an additional load resistor between output and ground. *This is simply shown as "load" in the datasheet's application example.*

    > We have selected a 220uH inductor, 100uF and 330uF Capacitor for this exercise.  Please check their ratings yourself to ensure they match with the assignment.

    <p></p>

    > **Alert:** please make sure that the power supply is disconnected from your breadboard before turning on power. You don't know what the last person set the voltage or current limit to, and this could damage the circuit when you power it up

4. Turn on the oscilloscope and set it up to 1) read the voltage of your input power supply, and 2) read the output of the voltage regulator.
5. Turn the ***disconnected*** BK Precision DC power supply on and turn the current control knob all the way down, and then back up a little bit. Set the voltage to within the allowable range you found previously.

    > *The current control feature is helpful to control the amount of current going into a circuit (see [page 8 of the manual](https://bkpmedia.s3.amazonaws.com/downloads/manuals/en-us/1671A_manual.pdf)). Allowing too much current into an incorrect circuit can cause physical damage to PCBs and ICs.*

6. Connect the oscilloscope probes to the power supply probes and confirm that the voltage read on the DMM matches the voltage on the power supply display. Note any discrepancies.
7. **Turn off the power supply.**
8. Now, connect the power supply to your breadboard along the selected power and ground rails.
9. You can now turn the power supply back on. Check the current and the over-current indicator. Is it in an over-current condition? Adjust the current dial until the over-current indicator turns off.

    > *The power supply itself should draw almost no current (less than 20mA). The resistors you have selected should also draw very little current.*

10. For the voltage regulator circuit constructed above, complete the following design and circuit verification steps:
    1. Measure the input voltage to the voltage regulator with the oscilloscope.

    > *This reading confirms that the power supply is outputting the correct voltage.*

    1. Measure the small-load output voltage of the voltage regulator with the oscilloscope.
    1. **Turn off the power supply**
    1. Connect a 5.1Ω power resistor from the output of the voltage regulator to ground, in parallel with the other resistor.
    1. **Turn on the power supply.**
    1. *Briefly* measure the voltage across the resistor with your multimeter. **Be careful, the components will get hot.**
        > *This reading tells you how well the voltage regulator works under load. Note how this voltage changes when you gently increase the current limit of the power supply.*
    1. **Turn off the power supply.**

## Part 2. Individual Demonstration of Proficiency

In class, demonstrate the following **live** to a member of the Teaching Team by the end of class:

1. Your breadboard fully constructed with regulator circuit
2. Oscilloscope measurement of the output voltage of the regulator circuit delivering 3.3V under no-load conditions.
3. Oscilloscope  measurement of the output voltage of the regulator circuit delivering 3.3V under 5.1Ω load.

**A live demonstration by the end of class is required. No late demonstrations will be accepted.**

## Canvas Submission

**No Canvas submission is required.**

## Grading

| **Demonstration**                            | **Points** |
| -------------------------------------------- | ---------- |
| Completed breadboard                         | 40         |
| 3.3V no-load output oscilloscope measurement | 40         |
| 3.3V loaded output oscilloscope measurement  | 10         |
| **Total**                                    | **100**     |
