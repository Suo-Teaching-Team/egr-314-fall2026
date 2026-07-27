---
title: "Lab: ESP-NOW and ESP-MESH"
---



## Introduction

In this lab, we will explore ESP-NOW and ESP-MESH, two wireless communication protocols designed for the ESP32 platform. ESP-NOW enables fast, low-power, peer-to-peer data exchange between ESP32 modules without requiring a Wi-Fi connection or router, making it ideal for simple sensor-to-controller communication. ESP-MESH builds on Wi-Fi to create a self-organizing, multi-hop mesh network, allowing multiple ESP32 devices to connect over longer distances and relay data through each other. By connecting two ESP32 modules, we will compare these approaches and observe how devices can communicate directly as well as form part of a larger, scalable network.


> To Demonstrate ESP-now you need to work with another student. To Demonstrate ESP-mesh you can work in a group where one student will be a host.

## Resources

* Github Repositories
    <!-- - ESP32 Simple UART Echo [Repository](https://github.com/embedded-systems-design/code_esp32_simple_uart_echo) -->
    * ESP32_MQTT [Repository](https://github.com/embedded-systems-design/code_esp32_mqtt)
* Required Software:
    <!-- * MPLABX -->
    * Python with Thonny (installation found in the [ESP32 section of the course website](https://embedded-systems-design.github.io/tutorials/esp32/))
    * [PuTTY Client](https://www.chiark.greenend.org.uk/~sgtatham/putty/)
    * [MQTT Explorer](https://mqtt-explorer.com/) (Windows/Linux/Mac) or [IoT MQTT Panel](https://play.google.com/store/apps/details?id=snr.lab.iotmqttpanel.prod) (Android)

* The [Embedded Systems Resources](https://embedded-systems-design.github.io/) 
# Platform IO extension
*   Open Vscode and on the left pane, click on the extensions tab

*   Search for Platformio in the search and install the extension. 

*   You will then perform the instructions under each of the demonstrations to get the checkoffs. 

*   If you have any trouble building or uploading see the section labeled Debugging ESP-NOW and ESP-MESH

# Demonstration 1
Send a message through ESP-NOW.
*   You will work with a partner to demonstrate communication between two ESP-32 boards. 

*   Clone the following [ESP-NOW repository](https://github.com/bao1311/ESP-NOW), Open in VScode. 

*   Modify the code to send a message to your partner. the message must include the senders name. 

*   Both partners must send a message. You will take turns being on the receiving end, each partner must send a message to the receiver to get checked off for demonstration 1. 

# Demonstration 2
Connect to an ESP-Mesh host and send a message.
*   you can work in a group for this demonstration. 

*   clone the following [ESP-MESH repository](https://github.com/bao1311/ESP-MESH) open in VSCode 

*   You must share a message in the ESP-Mesh the message must contain your name to recieve a check off


# Debugging ESP-NOW and ESP-MESH 

If PlatformIO is not programming because of dependency errors then please follow these steps to fix.

*    Delete the .platformio folder located in c:/users/username/.platformio

*    Restart vscode and click the vscode extension for platformio

*    Open project through platfromio, click on import project --> Select ESP32 devkit and look for your cloned repository, make sure the folder you select has an .ini file

*    Build the code then upload 

*    Can you see the output on the serial monitor? 


### Grading

| Item            | Points |
| :-------------- | -----: |
| Demonstration 1 |     20 |
| Demonstration 2 |     20 |
| Total           |     40 |
