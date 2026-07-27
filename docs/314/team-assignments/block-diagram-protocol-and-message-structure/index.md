---
title: Block Diagram, 
---

***Team Assignment***


## Objectives

The goal of this assignment is to determine and document the manner in which each team member's project will communicate electronically
It is common practice in industry to document the logical flow of software prior to handling implementation-level details like coding. These diagrams make writing code much easier, as well as help to improve the quality of your software design.
This will be accomplished by establishing:

A team-level block diagram highlighting the Subsystems interfacing with the ESP32


## Resources




* [draw.io](https://www.draw.io/) package (compatible with Google Drive) 

<!-- * *(EGR304):* [Simple Activity Diagram Example](https://www.dropbox.com/s/qbphzio2o5mcemx/Simple%20Activity%20Diagram%20Example.pdf?dl=0)
* *(EGR314):* [Activity Diagram with Interrupts](https://www.dropbox.com/s/70hfczjdyusv595/Activity%20Diagram%20Example.pdf?dl=0)
* Example Gameplay Activity Diagram with Interrupts [(pdf)](https://www.dropbox.com/s/70hfczjdyusv595/Activity%20Diagram%20Example.pdf?dl=0)
* [State Machine with Interrupt Example](https://www.dropbox.com/s/1npw6b2gs0il92r/Water%20Heater%20State%20Chart.drawio?dl=0) from TC -->
<!-- * [Uml-diagrams.org](https://www.uml-diagrams.org/activity-diagrams-examples.html) Activity Diagrams example -->

<!-- * [Software Design](https://embedded-systems-design.github.io/software-design/) page on the Embedded Systems Design Resources blog -->
<!--
- What is a [Network Topology](https://www.dnsstuff.com/what-is-network-topology)
-->



<!--
![](image3.png)

*Figure 1:* Example Network Topology, from [dnsstuff.com](https://www.dnsstuff.com/what-is-network-topology)

![](image4.png)

*Figure 2:* Two examples of a team's possible network topology
-->

## Assignment

### Team Block Diagram
<!--
![starting point](/314/project-description/block-diagram.png)
-->
Starting with the example from the project description, as well as your teammates' individual block diagrams, provide a detailed team-level block diagram

1. Your goal is to show:
    1. Subsystem Owner, for each teammate (Each team member must be in charge of 1 Subsystem) 
    1. Sensors connections (I2C, SPI)
    1. Power Connection and Distribution
    1. ICSP or USB Programming Port
    1. Map all pins that will be used by the team to specific gpio / peripheral pins on each microcontroller.
    1. if I2C, what is the address of each "peripheral"?
    1. if SPI, which pins are used for "chip select"?
    1. details of peripheral ICs, such as sensors, actuators, and OLEDs, which must be directly connected to the individual's microcontroller.

<!--
        > **Remember:** these pins must interface with the individual teammate's *microcontroller*, and may not directly connect to their local EUSART, I2C, or SPI network.

1. provide a more detailed block for the ribbon cable connector, showing all pins of the ribbon cable
    1. Map all pins that will be used by the team to specific gpio / peripheral pins on each microcontroller.
    1. if using SPI or I2C to provide high-speed communication between neighbors, provide information such as
        1. which device is the "controller" and which is the "peripheral" or "target"?
        1. if I2C, what is the address of each "peripheral"?
        1. if SPI, which pins are used for "chip select"?
    1. Include power distribution in your block diagram -- make sure the team board can be powered separately and that -- if desired -- how power can be distributed across the whole board(regulator).  
1. You may de-emphasize (by leaving them off or by showing grayed-out blocks) the parts of the individual subsystems that are determined by each teammate, and only accessible by that teammate.  For example:
    1. details of peripheral ICs, such as sensors, actuators, and OLEDs, which must be directly connected to the individual's microcontroller.
    1. ICSP or USB programming ports

<!-- 1. **Draw your team's network diagram.** Include each team member's name, a line indicating the connection between teammates, uni- or bi-directional arrows on each line indicating topic direction, and a label for each line indicating which topic that particular connection uses. If sharing a topic, add a node or vertex for the topic name instead of the connection (as in Figure 2, right). -->

![final example](<team_BlockDiagram_ex.png>)

_Figure: Example team-level block diagram, 

<!--
### Part 2: Sequence Diagram of Team Communication

**Draw a sequence diagram** showing an example of how each team member sends and receives data and how each system board responds via subsequent communication, actuation, and/or output.

* The sequence diagram should match the team's block diagram, in that connections between teammates and message direction should be consistent.
* In the case that the communication is driven by external events (different users inputting sensor data at different times), show an example of one typical use case.
* Show each hop of a message from upstream to downstream neighbors.   
* Show where messages are disposed
* Include expected user interactions from the HMI (Human Machine Interface) *and* from the web-based interface
* Indicate recurring sequences vs event-driven interactions
* Consider using mermaid to code up your sequence diagram directly in markdown.  See links in external resources, above
-->

## Homework Preparation and Submission

This work will be used -- and graded -- in multiple ways. It will be checked for completeness on the date given in Canvas.

### Preparation

Please prepare this assignment as a new page on your team's living report website.  Assemble:

Block Diagram


Assemble this into a new page on your team's website called "Block Diagram

Once completed,

* [x] Create a link to this new page on the datasheet's main landing page.
* [x] Check the link to ensure that it works
* [x] export this new page as a pdf

> The new page representing your assignment should not present as a page of links.  Do not use it to link to other documents *especially living documents*, such as google docs, draw.io drawings, or google sheets.    Rather, contents from other documents should be exported, saved in your repository, and hosted natively in markdown (or if need be html) on the site itself.

### Submission

To submit a complete assignment, please submit:

* [x] A working URL to the new "Block Diagram
* [x] the **exported PDF** for easier review

Both items must be submitted, by the deadline in the Canvas course calendar, in order to receive full credit.  It is your responsibility to ensure that your submission to Canvas was successful. Late Canvas submissions will be graded per the policy in the syllabus.

## Grading

| **Item**              | **Points** |
| --------------------- | ---------: |
| Block Diagram         |         200|

| **Total**             |    **200** |

### Qualitative Assessment

This document will assessed for quality by the teaching team when reviewed during the external design review.  Before then, please engage with the teaching team during office hours and/or classtime to review this document for ways to improve it.  We are happy to provide feedback, which will be your responsibility to integrate and address before the external design review.

Qualitative grading will assess how closely te team follows instructions, for general formatting, layout, organization, and legibility, and to ensure feedback-based updates were applied to all sections. Items above will be graded based on the following scale (please see the syllabus for a full description of each):

* 100% Exceeds Expectations
* 85% Above Expectations
* 70% Meets Expectations
* 55% Below Expectations
* 40% Does Not Meet Expectations
* 0 Missing / Not Submitted

### Subsequent Uses of this Document

This document will be used by your teammates to help make decisions on how to distribute functionality across your teammates.
Additionally, as part of your living report website -- a public website -- this document should be updated and improved throughout the semester in order to reflect your most current design.
It will also be reviewed seen by external reviewers who will be given the opportunity to provide direct and indirect feedback, and as part of your team's final report.


## Checklist

* [x] The page is easy to find 
* [x] The block diagram is clear and well-formatted
* [x] Arrows are shown 
* [x] The team's power plan is shown through the use of connectors and / or jumpers
* [x] Each teammate's role is clearly documented with corresponding Subsystem  



