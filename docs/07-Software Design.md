---
title: Software Design
---

## Introduction

As seen in Figure 1, this page is dedicated to demonstrate how we run our code. We will use the sensor boards to read their respective sensors (light and sound) to then send a determined value to the control board, communicating the status of each. Within the control board, there are user input controls that will also affect the light and motor status, along with the information gathered from the sensor boards. Once the central board determines the input, it will output on to the LEDs and motor to respond a certain way, depending on the information that the board is being sent. 

The software was set up to separate sensing, control, and output across each board for clarity and reliability across the entire system. The modular design of our system makes it easier to maintain and ensures it meets the hands-free lighting design requirement by automatically responding to detected motion or sound without manual user input.

A direct link to the source file of the following block diagram can be found [here](https://github.com/egr304-team-205-2025-f/EGR304-2025-F-205.github.io/releases/download/softwareproposal/Software.Proposal.drawio).


## UML Activity Diagram

![Figure 1](image/Software%20ProposalUpdated.drawio.png)


## Structure Decision Making Process

The structure of the software diagram was chosen to clearly separate the responsibilities of each board and to ensure that the system operates in a predictable, linear sequence. It aims to visually show how each board functions and interacts. The Sound Board and Night Board each handle their own sensing, convert those readings into simple high/low signals, and send only the analyzed data to the Control Board. This allows us to reduce computation within the Control Board and to avoid noise-prone analog communication lines. Similarly, the Control Board software was structured to receive inputs first, then make decisions, and then trigger outputs such as stopping the motor or activating the light. Each board operates on a continuous loop to be able to continuously read, update, and analyze data being detected from the sensors. The use of decision blocks, object flows, and separate columns in the diagram reflects a structured, modular software approach where each board behaves independently yet contributes to the larger system logic. It provides a simple, straightforward, and effective solution for coordinating sensor inputs and controlling the lighting behavior based on real-time environmental conditions.

## How it Meets Product Requirements

As seen in the figure below, each subsystem was designed to support product requirements through a modular sensing, decision, and output workflow. The sensor boards continuously monitor environmental data and send high/low signals to the control board, ensuring hands-free operation and automatic responses to triggers with minimal user involvement. The threshold based structure of our sensors minimizes false positives and ensures quick response times. This directly supports our aforementioned requirements for efficiency, reliability, and user convenience. The control board evaluates sensor data and user settings before acting, ensuring the motor only stops and the light only turns on when both darkness and sound are detected, fulfilling needs for energy conservation. By isolating sensing, control, and output functions, the software becomes easier to maintain and more robust under varying conditions, as well as safer for continuous operation. The use of digital communication between boards enhances usability, simplifies manufacturing and testing, and ensures the system functions consistently. Overall, the software structure meets key requirements for safety, usability, reliability, and hands-free automation across the product’s full operating conditions.

## Version 2.0

If we were to develop a second version of the software design, several improvements could be implemented by revisiting key components of the software and hardware. 
One of the most significant limitations of the current design is that each sensor board outputs only a simple high/low digital signal to the control board. While doing so simplifies communication and reduces noise issues, it also restricts the software’s ability to interpret sensor data or adapt its behavior based on environmental variation. By adding support for analog signal communication, the software could dynamically adjust thresholds and better differentiate between background noise and intentional triggers. It would improve sound detection reliability and reduce reliance on fixed thresholds, which would be more difficult to tune for different environments and may not perform as reliably.

The motor control section could also benefit from a more advanced motor driver with built-in current sensing, thermal shutdown, and improved flyback protection to protect electronics and extend the product's lifespan. Feedback mechanisms could also be added to allow software to detect jams, overloads, or unsafe conditions. This would enhance safety, enable smarter control, and make the device more robust.

Overall, Version 2.0 of the system would benefit from hardware upgrades that give the software more information, more control, and more efficiency. By improving sensor interfaces, motor control hardware, and communication methods, the software could evolve from a basic threshold-driven approach into a more intelligent and adaptive design that better supports long-term reliability and performance. 
