---
hide:
    - toc
---

# March 1st 2023 : Interfaces



**Reflection**

The topic of today's lesson was Interfaces.

 Instead of lectures, we had a hands-on lesson where we used an ESP32 Feather, a breadboard, and a LED light to experiment with different ways to control the LED light. We started by using basic code in the Arduino IDE and changed the LED pin to LedPin 14 so that the LED wouldn't use the LED on the Feather board. This allowed us to control the LED by making it blink within a specific time frame. Using this method, I was able to understand the code more deeply and how it controlled the FeatherBoard.

We then experimented by adding different messages to the code to see how the LED light would respond. Starting with simple commands like "blink twice" and "blink twice slowly", I was able to understand how changing the code affected the LED light's behavior. We then used the JLed library to make the LED light do animations like breathing, which made the LED light light up slowly and fluidly.

Eventually we turned off the light in the classroom and viewed our mini collective installation together. 

We also deepened our knowledge about MQTT, a protocol which is used to trigger things or retrieve information from sensors. We crafted our own "network" during class and sent each other message like "hello". MQTT is seemingly simple. An MQTT broker server can sense things, publishers that could be any sensors or devices, and subscribers that listen to the broker and wait for instructions on what to do. It is an important concept central to  the Internet of Things (IoT).











