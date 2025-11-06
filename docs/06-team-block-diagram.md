---
title: Team Block Diagram
---

## Introduction

This project consists of four interconnected boards that work together to create a light level and audio activated lighting system. Each board features its own microcontroller and either a sensor or actuator. One board detects loud sounds using a microphone and op-amp, sending a digital signal to the input/output board. The Night Sensor board uses an photo resistor sensor to detect light level and also sends a signal to the input/output. The input/output board acts as the central hub, processing inputs from both sensor boards and deciding when to activate the lighting. This board also uses a motor to pivot the sensor boards to act like a radar. A separate board controls the lights based on the command received from the input/output board. This board also uses a speaker to notify the user that the light is on or off. The boards are connected as shown using 8-pin ribbon cables, with shared ground and assigned signal lines for efficient communication.

We structured the block diagram by dividing the system into each PCB, Input/Output, Sound, Light Sensor, and Lights, each containing its own microcontroller to simplify development and improve reliability. This design supports hands-free operation through motion and audio sensors. The clear separation and standardized connectors ensure compactness and easy integration, meeting our previously defined product requirements.


## Overall Block Diagram

![image caption](image\Team 205 Egr304.drawio.png)

The source file for the following block diagram can be found [here](https://app.diagrams.net/#G1p7TDof-kBIDls-BMGx75dPDWvmFWUAvf#%7B%22pageId%22%3A%22D7A3hRXi8sjnXgM3Vncy%22%7D).


|        Connector #   |      From        |       To        |     Short Description                        |   Type of Signal  |
| :------------------: | :--------------: | :-------------: | :------------------------------------------: | :---------------: |
| Connector 3:2          |   Sound Board    |    Hub Board    |  Triger for light      |        DC         |
| Connector 1:5          |   Night Sensor    |    Hub Board    |  Tiger for light       |        DC         |