---
title: Product Requirements
tags:
- tag1
- tag2
---

## Project Objective

This project aims to develop a sound-actuated automatic lighting system that will respond to specific audio cues to turn lights on and off. Using audio detection will create a convenient hands-free experience for users, allowing for more enhanced lighting across various environments, such as homes, offices, and other workspaces. It will also feature brightness detection to keep the light off if the area is already bright, improving energy efficiency while maintaining effectiveness and simplicity. It will be designed to be easy to install and interact with, allowing users with limited technical experience to operate and benefit from the product.

## Stakeholders

- **Primary Users** Individuals in environments where hands-free lighting solutions would improve accessibility and convenience.
- **Users With Mobility Limitations** Users who may not be able to reach or activate standard light switches due to physical limitations.
- **Installers** Those who install, set up, or troubleshoot the device. The device should remain relatively simple and user friendly for configuration purposes.
- **Technical Support** Team assiting users with any issues that may be encountered.
- **Marketing and Retailers** Able to cater the product to a wide range of audiences for various different solutions. 


## Use Cases

**User Case #1: Emily**

Emily is a multitasking parent who often enters dim hallways or rooms with her hands full, carrying groceries, laundry, or managing her kids. She frequently finds herself in positions where she cannot easily reach a switch on a wall, leading her to rely on a system that responds quickly and reliably to a simple sound cue such as a clap or short vocal signal. She comes home one day, her hands full with grocery bags. By simply whistling once, she activates the light in her dark kitchen, allowing her to see her counterspace to know where to put her things. The light stays on when the door slams shut behind her, as it wasn't loud enough to trigger the light again. The quick response of the light allows her to see the items in the room and safely navigate around the space to start putting her things away.

**User Case #2: Bill**

Bill has limited mobility and is in a wheelchair, however, the lightswitch in his workshop is on the other end of the room and can take him a while to reach. He claps his hands upon entering the room to trigger the lights, letting him trigger the audio response of the lights. Bill frequently works with louder machines in his workshop, but the threshold at which the light is set to trigger at does not pick up these noises, allowing his work area to remain lit and keep him safe. One day he enters the workshop, clapping his hands as usualto turn the lights on. It is during the day, and the natural light that enters the room is detected by the system and the lights remain off to conserve energy. However, Bill needs more than just the natural light to see his work, so he uses an override button to turn the lights on, regardless of the lighting already in the room.

## Aspects

The new product design will be based on that of typical sound-activated automatic lighting systems with improvements based on the following requirements. The **P1 - P10** is the "code" to indicate the priority of the requirement, from low to high.

 **Hardware/Product Design**

   * 1.1 The product shall be easy to recognize as a high quality and highly practical lighting solution for various different applications (P10)
   * 1.2 The product shall remain compact and robust to function continously without performance degradation (P8)
   * 1.3 The components within the device will not break or deteriorate (P8)
   * 1.4 The product shall have simple design and have various mounting solutions on the back of the product. (P6)
   * 1.5 The system shall remain usable during power fluctuations without user confusion. (P5)
   * 1.6 The enclosure will protect electronics from environmental conditions if it is to be used outside (P4)

  
 **Software/Functionality**

   * 2.1 The product shall incorporate external buttons for immediate control. (P10)
   * 2.2 The product shall detect an external cue to trigger the light. (P10)
   * 2.3 Sensors within the product shal respond instantly with no delays. (P9)
   * 2.4 The product shall consider current light conditions to conserve energy. (P8)
   * 2.5 The system will be able to avoid false triggers of its sensors. (P8)
   * 2.6 The product will have an "idle" scanning mode to conserve energy. (P6)
   * 2.7 The product shall turn off after a set period which can be adjusted by the user. (P5)

     
**Interactivity and User Experience**

   * 3.1 The product will be usable by consumers of varying degrees of mobility. (P10)
   * 3.2 The product shall have visual indicators to communicate system status with users, such as active listening mode, sensor activation, or light activation. (P9)
   * 3.3 The product shall be easy and intuitive to set up and use (P7)
   * 3.4 The product shall be easy to troubleshoot. (P5)
   
**Customization**
   * 4.1 Users shall be able to adjust sensitivity of both the sound and brightness detection subsystems. (P7)
   * 4.2 The product will allow users to configure the duration for which the light remains active. (P6)
   * 4.3 Users shall be able to adjust the brightness of the light when it is on. (P6)

**Manufacturing**

   * 5.1 Major subsytems within the device will remain modular for testing and replacment. (P9)
   * 5.2 Any mechanical configuration to be done by users will remain simple and straightforward. (P6)
   * 5.3 Subsytems within the product shall fail independently (if at all) to maintain maximum operation. (P4)
   * 5.4 The design shall utilize components available from multiple suppliers to prevent shortages. (P5)
   * 5.5 The product will be designed to operate quietly to improve user experience and avoid false triggers. (P6)

**Safety**

   * 6.1 The product shall operate under 5V to avoid potential overheating and other electrical hazards. (P10)
   * 6.2 The system shall remain stable under continuous operation without mechanical hazards (P10)
   * 6.3 The product shall have an enclosure to protect users from any exposed electrical contacts using proper enclosure design (P7)
   * 6.4 Any system movement shall avoid creating pinch points or mechanical hazards. (P6)

## Requirement Criteria Specifications

   * 1.2.1 The product shall operate for 24 hours continuously with no functional degradation.
   * 1.3.1 The system shall maintain full functionality after 1,000 power cycles.
   * 1.4.1 At least two simple mounting solutions will be available.
   * 1.5.1 No unintentional light activation may occur during voltage dips above a certain voltage.
   * 2.1.1 Button response shall occur within 100 ms of activation.
   * 2.3.1 Sensor to light activation time shall be within 150 ms.
   * 2.4.1 Light shall not activate when ambient light exceeds a defined threshold.
   * 2.7.1 Adjustable timer range shall span 10–60 seconds.
   * 3.2.1 Indicators shall be visible from 3 meters and refresh status within 250 ms of system change.
   * 4.3.1 Brightness range shall span 40–100% of maximum output (test).
   * 5.1.1 No individual subsystem shall require removal of unrelated components for replacement or inspection.
   * 5.3.1 Failure of one board shall not disable unrelated subsystems
   * 6.2.1 No components shall detach or loosen after 100 hours of operation.



## Open Questions

* Can we move towards a recyclable and repairable product, for example, with ZIF connectors and glue-free assembly?
* Can we improve on lighting a room from a single sorce?
* How customizable should the user interface be, and what level of adjustability is required to support all user types while maintaining simplicity?
* How will the product handle long term and constant use?
* Should the product integrate with or communicate with other smart-home devices or multiples of the same product?
