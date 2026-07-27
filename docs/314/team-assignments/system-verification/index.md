---
title: Team System Verification
---

***Multi-Part Team Assignment***

## Objectives

To demonstrate how your project's components work independently and with each other across each team members' final PCBs. This assignment will help you plan your verification strategy and communicate what needs to be tested to instructors.



> Note: Due to the number of teams,  Your team must be prepared to demonstrate each of the required checkoff components. 



## Preparation

Please update your team's website with the following information:


   

    > It is your responsibility to ensure that your website update is successful.


    

> **Important:** Verification must occur on your team's final full combined PCB, not on breadboards, perfboards, protoboards, or individual subsystem PCBs.

1. Come early and prepare your hardware and software to demonstrate in advance so that the evaluation can begin promptly at the starting time.

   

1. On your team's combined PCB, demonstrate the following functionality:
    1.  data to/from the web interface (MQTT, ESPnow, ESPmesh) 
    1. A feedback-controlled response, in which changes in your sensor result in a reasonable change in a serial log or LED indicator.
    1. Actuators such as LED Subsystems breathing through PWM or Motors with bi directional control. 
    1. Power Distributed to your board. The Regulator present on your board must step voltage to 5V or 3.3V. (in some cases if you need to step up from a lower voltage please demonstrate the stepped up voltage and the input voltage)
                                           
                                           
                                           
                                           
                                                                                                               |


System Verification will be done by the teaching team. The teaching team will be looking for two things on each subsystem Power distribution across your subsystem does (for example does your sensor have a 3.3V reading across the power pins) and its overall functionality criteria for functionality is described above.

We understand that teams will have a different amount of subsystems depending on the number of people on the team. To account for the amount of subsystems for each team, the teaching team devised a way to calculate the teams grade for system verification. if you have less subsystems on your pcb, you will have less TotalChecks to account for as described above (power, functionality).

TotalChecks = 2 * SubsystemAmount

TeamGrade = (PassedChecks/TotalChecks) *400

As an Example Team 320 has a total of 4 subsystems 

TotalChecks = 2 * 4 
Team 320 will have to verify 8 total checks, 2 per subsystem.

Team 320 was able to verify 7 of their 8 checks with the teaching team.

TeamGrade = (7/8)*400

TeamGrade = 350


