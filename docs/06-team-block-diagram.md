---
title: Team Block Diagram
---

## Introduction

This project consists of three interconnected boards that work together to create a light level and audio activated lighting system. Each board features its own microcontroller and either a sensor or actuator. One board detects loud sounds using a microphone and op-amp, sending a digital signal to the input/output board. The Night Sensor board uses an photo resistor sensor to detect light level and also sends a signal to the input/output. The input/output board acts as the central hub, processing inputs from both sensor boards and deciding when to activate the lighting. This board also uses a motor to pivot the sensor boards to act like a radar. This board also controls the lights based on the data received from the night sensor and sound detection boards. The boards are connected as shown using 8-pin ribbon cables, with shared ground and assigned signal lines for efficient communication.

We structured the block diagram by dividing the system into each PCB, Control, Sound, Light Sensor, each containing its own microcontroller to simplify development and improve reliability. This design supports hands-free operation through motion and audio sensors. The clear separation and standardized connectors ensure compactness and easy integration, meeting our previously defined product requirements.


## Overall Block Diagram

![Figure 1](https://github.com/egr304-team-205-2025-f/EGR304-2025-F-205.github.io/blob/main/docs/image/hubdiagram.drawio.png?raw=true)


The source file for the following block diagram can be found [here](https://github.com/egr304-team-205-2025-f/EGR304-2025-F-205.github.io/releases/download/blockdiagram/hubdiagram.drawio).


|        Connector #   |      From        |       To        |     Short Description                 |   Type of Signal  |
| :------------------: | :--------------: | :-------------: | :-----------------------------------: | :---------------: |
| Connector 1:1          |   Night sensor |    Hub Board    |  indication status if light/dark      |        GPIO         |
| Connector 1:7          |   Hub          |    Night Sensor |  5v power                             |        I/O         |
| Connector 1:8          |   Hub          |    Night Sensor |  Ground                               |        GND         |
| Connector 2:2          |   Sound        |    Hub Board    |  indication of sound trigger          |        GPIO         |
| Connector 2:7          |   Hub          |    Sound        |  5v power                             |        I/O         |
| Connector 2:8          |   Hub          |    Sound        |  Ground                               |        GND         |


**Message Structure Design**

Our team designed the message structure between the three interconnected boards to prioritize simplicity, reliability, and real-time responsiveness. Each sensor board sends a dedicated digital trigger signal to the central Input/Output board via fixed pins on an 8-pin ribbon cable, eliminating the need for complex communication protocols. Shared ground and regulated power lines maintain signal integrity, while asynchronous, event-driven signaling allows the Input/Output board to react immediately to sensor inputs without constant polling. This clear, modular approach ensures efficient communication, easy troubleshooting, and future scalability.

**5 Biggest Changes to Software Design Since Proposal**

1. We changed from sending an analog audio signal to the control board to sending a simple digital high/low trigger from the audio board. This reduces processing complexity on the control board and improves signal reliability by clearly indicating when a sound event occurs.

2. We implemented fine motor control, including directional control, an emergency stop, and a full system debug mode. These additions were necessary for the central board to meet the product specifications.

3. We revised the sensor input hierarchy so that the motor only operates when the room is dark, and the light activates only when the room is dark and a trigger sound is detected.

4. We removed the need for environmental calibration on the devices. During testing, calibration caused delays in functionality and did not realistically fit within the scope of the revisions we were able to complete in the limited time remaining.

5. Unfortunately, due to unforeseen personal circumstances, one of our teammates had to withdraw from the course, requiring us to restructure our code. As a result, the output board was removed, and its logic is now handled directly by the central input/output board.
