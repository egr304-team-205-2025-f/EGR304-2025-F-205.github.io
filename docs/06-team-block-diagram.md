---
title: Team Block Diagram
---

## Introduction

This project consists of four interconnected boards that work together to create a motion and audio activated lighting system. Each board features its own microcontroller and either a sensor or actuator. One board detects loud sounds using a microphone and op-amp, sending a digital signal to the input/output board. The motion board uses an ultrasonic sensor to detect motion and also sends a signal to the input/output. The input/output board acts as the central hub, processing inputs from both sensor boards and deciding when to activate the lighting. A separate board controls the lights based on the command received from the input/output board. The boards are connected as shown using 8-pin ribbon cables, with shared ground and assigned signal lines for efficient communication.

We structured the block diagram by dividing the system into each PCB, Input/Output, Sound, Motion, and Lights, each containing its own microcontroller to simplify development and improve reliability. This design supports hands-free operation through motion and audio sensors, while also providing manual controls for user convenience. The clear separation and standardized connectors ensure compactness and easy integration, meeting our previously defined product requirements.


## Overall Block Diagram

![image caption](https://github.com/egr304-team-205-2025-f/EGR304-2025-F-205.github.io/blob/main/docs/image/hubdiagram.drawio.png?raw=true)

The source file for the following block diagram can be found [here](https://github.com/egr304-team-205-2025-f/EGR304-2025-F-205.github.io/blob/main/docs/image/hubdiagram.drawio).
