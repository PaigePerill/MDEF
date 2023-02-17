---
hide:
    - toc
---

# February 1st 2023 : Electronics and Coding

**Reflection**



This class is a broader view on how to face electronics and how to use electronics for our projects. The more technical parts are up to us to research if we need (we will be given links). 

Why do we need electronics as designers and how do we use them in our projects? 
Normally we prototype and do a proof of concept. 
To prototype electronics we usually use an already made board. But it’s not one we’ll integrate in our final design. Usually we’ll design a schematic or go to someone who knows how to make a schematic that can help us. 

The frontier between microcontrollers and SBCs (single board computers) is very blurry. Normal computers have several board that you assemble. The raspberrypi is a single board computer not a microcontroller. They have different things they can do. The RAM is different. You can still use them in similar ways, the only thing that changes is how you interface them, since computers already have an interface: an operating system. An microcontroller you have to give all the instructions. That’s a really big difference. 

Arduino is kind of a microcontroller, but it’s especially a brand that have many variations. 

The Feather boards are designed by Adafruit in contrast - they are more compatible with the feather ecosystem. 

In MDEF we are using the ESP Feather 32 BUT with Arduino. Because Arduino is also a software ecosystem eg the *milis function* (the graphplot to measure time in miliseconds)  is an Arduino invention. 

Basic Principles of Arduino: ****Freedom to use, understand, modify and share your tools.****

Arduino invest a lot into education so even novices can learn the beasics of electronics. 
They managed to create a community of people who aligh with the same spirit of learning and sharing and spread their knowledge via tutorials for everything and anything; A great body of knowledge has been built around the Arduino ecosystem.



^^Assignment:make some music with your board and a simple buzzer^^

(done with the help of brother and translated back as best possible) 

1. Set up the ESP32 Feather board and connect a buzzer to the board's GPIO pin.
2. Install the necessary software tools, such as the Arduino IDE and the ESP32 board support package.
3. Open the Arduino IDE and create a new sketch.
4. In the sketch, include the necessary libraries for the ESP32 and the buzzer, such as the "toneMelody" library.
5. Define the pin that the buzzer is connected to by using the "tone" function.
6. Write the melody you want the buzzer to play using the "tone" function. Specify the frequency and duration of each note in the melody.
7. Upload the sketch to the ESP32 Feather board and test the buzzer to make sure it is playing the melody correctly.
8. 

 "Happy Birthday" melody using the ESP32 Feather board and a buzzer:
 
#include "pitches.h"

// notes in the melody
int melody[] = {
  NOTE_G4, NOTE_G4, NOTE_A4, NOTE_G4, NOTE_C5, NOTE_B4, 
  NOTE_G4, NOTE_G4, NOTE_A4, NOTE_G4, NOTE_D5, NOTE_C5,
  NOTE_G4, NOTE_G4, NOTE_G5, NOTE_E5, NOTE_C5, NOTE_B4, NOTE_A4,
  NOTE_F5, NOTE_F5, NOTE_E5, NOTE_C5, NOTE_D5, NOTE_C5
};

// note durations: 4 = quarter note, 8 = eighth note, etc.
int noteDurations[] = {
  4, 4, 4, 4, 4, 2,
  4, 4, 4, 4, 4, 2,
  4, 4, 4, 4, 4, 4, 2,
  4, 4, 4, 4, 4, 2
};

void setup() {
  // set the buzzer pin as an output
  pinMode(2, OUTPUT);
}

void loop() {
  // iterate over the notes of the melody
  for (int i = 0; i < sizeof(melody) / sizeof(melody[0]); i++) {
    int duration = 1000 / noteDurations[i];
    tone(2, melody[i], duration);
    delay(duration * 1.3); // add a pause between notes
    noTone(2); // stop the tone
  }
}


In this code, the "pitches" library provides the frequency values for each note. 

We define the notes and note durations for the "Happy Birthday" melody, and then iterate over the notes to play them using the "tone" function. It's also necessary to add a delay between notes to create a pause, and use the "noTone" function to stop the tone after each note. 

Finally, upload the code to the ESP32 Feather board and the buzzer should play the melody.