---
title: Message Compliance Verification
---

***Individual Assignment***

## Introduction

> An application programming interface (API) is a connection between computers or between computer programs. It is a type of software interface, offering a service to other pieces of software. A document or standard that describes how to build such a connection or interface is called an API specification. A computer system that meets this standard is said to implement or expose an API. The term API may refer either to the specification or to the implementation.
>

> \- [Wikipedia](https://en.wikipedia.org/wiki/API)

The purpose of this assignment is to verify that your subsystem meets the compatibility requirements for communicating with your team's system

## Resources

* [Project Description](/314/project-description/)
* [Protocol Specification](/314/project-description/protocol/)
* [Mini-Lecture on Class Message / UART Protocol](https://www.dropbox.com/scl/fi/e4jec3opauc0kxooictwy/messaging-protocol-in-c.html?rlkey=536hb66s9z4jmbuck9i48xrpq&st=ub4db1b7&dl=0)
* [Serial Communication Lecture](https://www.dropbox.com/scl/fi/pgetfj7qn1xksz3riu3sl/Serial-Communication.pptx?rlkey=3beddm5g8cg7yzivt1tt6npqh&st=tzoykio4&dl=0)

## Preparation

### Individual Datasheet Update

1. Make a new page on your individual "datasheet" website called "API"

1. From your team's "Block Diagram, Process Diagram, and Message Structure" assignment, identify the messages that you must send or receive and copy them to your datasheet.  This includes:

    * messages you send to someone else (or broadcast to everyone)
    * messages sent to you
    * messages broadcast from someone else to the whole team that you will act on in some way.

1. For each message, review the message table defined by your team in that team assignment.  Does it include all the data required to process that message?  Was something missed?
1. For each message, expand the information provided.  Provide
    * the number of bytes
    * the data type (if you are using micropython, you must state/use the corresponding C data type)
    * the variable name
    * the smallest number you will recognize in your code (must be greater than or equal to the limits imposed by your data type)
    * the largest number you will recognize in your code (must be less than or equal to the limits imposed by your data type)
    * An example of valid message data

    > **Reminder:** You cannot just update your own message types in a vacuum.  This will require coordination from your teammates, and you will need to make sure the team report webpage is updated to match your necessary changes.  Any teammates that share message types will also have to ensure their message structures match yours.

    Example: Message Type 64 -- Motor Speed Setpoint

    |               |       Byte 1       |     Byte 2     |      Byte 3       |
    | ------------- | :----------------: | :------------: | :---------------: |
    | Variable Name | ```message_type``` | ```motor_id``` | ```motor_speed``` |
    | Variable Type |   ```uint8_t```    | ```uint8_t```  |   ```int8_t```    |
    | Min Value     |         0          |       1        |       -100        |
    | Max Value     |         9          |       5        |        100        |
    | Example       |         1          |       3        |        -30        |

    > **Clarification:**  These messages fit INSIDE the class messaging protocol, in the "message data" area of each packet (bytes 4-61).  You DO NOT need to include the prefix, suffix, sender, or receiver in this table, as these are constant across the whole class.  Your messages fit INSIDE that [specification](/314/project-description/protocol/).

### Handling Code

You will next need to implement and expand the Message Protocol examples shared in class and available in the [resources](#resources) links above

Your job will be to:

* Implement a message receiver that:
    * handles all messages sent in over the daisy chain UART network
        * passes on messages intended for someone else
        * processes messages intended for you.
        * trashes messages sent from yourself that have made it back to you
        * ignores messages larger than your buffer size
    * anticipates and handles mal-formed messages by ignoring them.  For example:
        * ignores characters sent outside of a message frame
    * handles each message type intended for you
        * must provide a unique acknowledgement of the message and the data received, whenever a correctly-formatted message is received.
        * This does not have to connect to your final system functionality yet, but should be differentiable based on the message type and message data received
* Implement a message sender that
    * sends an example of each message type, properly formatted, with time-varying data (can be valid data or "dummy" data for now).
        * easily modifyable based on the instructor's request (see below)
    * ensures that data you send is properly formatted
        * contains proper prefix and suffix
        * is properly addressed by you, and properly addressed to someone on your team.
        * ensures that message data does not contain message prefix and suffix codes.
        * cannot send data that is longer than the specification.
        * any other other reasonable formatting mistakes are prevented.
        * prioritizes passing on messages received by you before sending your own messages.
        * ensures a maximum rate of sending messages determined by a specified variable, and implemented using programming best practices, such as interrupts, timers, and non-blocking code.

## Individual Demonstration of Proficiency (not required Spring 2025)

> This part of the assignment has been deferred.  It will now be checked during the team system verification assignment.

Checkoff will be completed in class over the course of several classes, and must be completed before you can officially join your team's system.

> Demonstrations may be completed through the date noted in Canvas. Your grade will be documented in a spreadsheet and later uploaded to the Canvas gradebook. Late demonstrations will be graded per the policy in the syllabus.

1. You will plug both 8-pin ribbon cable connectors into your final PCB, (or a breadboard if it is not complete), matching the specification provided in the Project Description and Protocol Description documents.  The other end will be connected to an instructor's evaluation board to create a two-member daisy chain.
1. You will provide a demonstration of each message received and how you handle it.
1. Instructors will look at your API page and ask you to send a variety of commands based on your API, to various team members, to ensure you send messages that match the protocol.
1. You will then walk instructors through a demonstration of sending the message asked for, and the instructors will check it for formatting and validity.

### Preparation

Please prepare this assignment as a new "API" page on your github webpage (your individual "datasheet").

* [x] Ensure your message types match your team's
* [x] Ensure you have provided a full message specification for each message type, as described above
* [x] Zip up your software and provide a link
    * In MPLabX, this can be done by right-clicking on your project name in the Projects window and select "Package".

  Once completed,

* [x] Create a link to this new page on your individual datasheet's main landing page.
* [x] Check all links to ensure that they work
* [x] export the new API page as a pdf

> Do not link to *living documents*, such as google docs, draw.io drawings, or google sheets.   Rather, contents the .pdf and .zip documents should be exported, saved in your repository, and hosted on the github site itself.

### Submission

To submit a complete assignment, please submit:

* [x] A working URL to the new "API" page.
* [x] the **PDF of the API webpage** for easier review

Both items must be submitted, by the deadline in the Canvas course calendar, in order to receive full credit.  It is your responsibility to ensure that your submission to Canvas was successful. Late Canvas submissions will be graded per the policy in the syllabus.

## Grading

| **Item**                                                 | **Points** |
| :------------------------------------------------------- | ---------: |
| Initial Submission (completeness)                        |         25 |
| Demonstration (percentage of messages handled correctly) |        ~~200~~ || Final Report (quality)                                   |         75 |
| **Total**                                                |    **~~300~~ 100** |
