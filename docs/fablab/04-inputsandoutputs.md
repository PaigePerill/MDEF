---
hide:
    - toc
---

# February 9th 2023 : Inputs and Outputs 


**Reflection**

"We can measure almost anything if we have something that reacts to the change. We can then measure that reaction"

For this class we focused deeply on inputs and outputs, especially the various sensors that exist and how they work. This was extremely useful becuase it was also about learning how to select a sensor for a specific task

This topic was interesting because the group is working on a project involving grey water, and they wondered if a Smart Citizen Kit, which is used to measure water quality in the ocean, could be adapted to measure tap or grey water quality. The group discussed the potential benefits and drawbacks of this idea, such as increasing citizen knowledge and trust in the water system, or empowering them to take action and question the system

. The group then worked with two boards to practice connecting different inputs and outputs. The first board involved connecting a LED and a button to make the LED light up when the button is pressed, and the second board involved experimenting with a Photo Cell sensor to detect light. They encountered some challenges with the resistors and the LED, which they will need to address before connecting the boards.

^^Assignment:try to use a sensor and and actuator to communicate^^


For the homework I worked in a group, I played with the the LDR light sensor in order to measure the the rooms' luminosity.  We tweaked to the code  so that the sensor could detect either light or dark instead of a range of light. However, there were some challenges with getting the sensor to detect in the right timing. To address this, I experimented with different resistor ohm amounts because the ESP32 board was 3v VS 5v. In the end the sensor was able to detect various levels of light from dim to bright. We collaborated to create another board that had a switch to turn the LED on and off. Although we encountered issues running the code on different computers and getting them to connect, the boards functionned independently.

