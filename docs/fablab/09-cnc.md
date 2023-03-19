---
hide:
    - toc
---

# February March 1st 2023 : CNC 



**Reflection**

This class covered the topic of CNC (Computerized Numerical Control), which is a highly precise, adaptable and automated method of digital manufacturing suitable for various design purposes. CNC machines available can have three axes or more. These machines are generally heavy and use coolant liquids for heat reduction. CNC machines have two types of motors - a router motor (less expensive) and a spindle motor (quieter, with more power). To prevent material from breaking while milling, a lubricating substance is necessary, which can either be applied manually (less expensive, cleaner, and weaker) or automatically (costly, dirty, and powerful). Milling requires special attention to aspects such as the kerf tolerance and material "bounce back." Additionally, sharp edges are not achievable at the end of the milling process; instead, the edges are rounded or require a t-bone or dog bone shape to ensure support in the middle.

To fabricate with CNC, one must first create a 3D model and then export it to a g-code while adjusting the machine and material settings. Two different bits can be used for CNC machines, mills for milling (flat), and drills for creating holes (round). Moreover, there are different types of rotations such as straight, up, down, and compression. The chip load, which refers to the amount of material removed by each cutting tool revolution, must also be set up before milling. Milling can be done from either the top or the bottom for better accuracy, and attachments such as vacuum, T-slot, double-sided tape, screws, or taps can be used to ensure accuracy.


I did the CNC Homework as part of my Microchallenge week. 
Below is the process I followed: 

# InterspeciesTarot


**Boxset Making Instructions**


This documentation describes the making of a box for holding a deck of cards and a booklet. 
When the box opens, a Voice will describe the context of the object and why it needs to exist. 

The deck of cards and booklet are tied to my Project with Carolina called the Interpecies Tarot. It is a tarot deck that illustrates and poses the crucial questions we need to ask ourselves when working with other species to act more in alignment. By using the tarot format, we can go into detail about each concept card in the booklet, while the cards remain evocative images. This works well for the project because we can expand on complex subjects in written form including a mix of scientific concepts, poetic storytelling and references, yet stay engaging and playful.

Because the content is not entirely ready yet, the voice recording part of this project  (which was Daphne's idea) is a good addition, since it can be a placeholder until the content is ready (cards+booklet), yet still intrigue and inspire the audience. 

The inspiration for the booklet is the Dali Tarot Boxset: 

![](https://i.imgur.com/bCycgJm.jpg)



- [ ] Step 1: 

Define how the box will be made. 

I had orginally thought of laser cutting various pieces of plywood with the lasercutter and assembling them together, however Eduardo suggested I instead CNC the slots shapes into a large block of wood. We went to see the available wood in the scrap pile and found a thick piece of white oak wood that fit the brief perfectly. 



- [ ] Step 2: 
Sketch the file and get feedback. 
I sketched heavily on Eduardo's initial sugggestion drawing including a thin slot for the booklet, a deeper slot for the cards in the middle of the booklet slot and a round slot for the speaker in the top left. 

![](https://i.imgur.com/OlH0zeq.jpg)


- [ ] Step 3: 

Model the file. This is not not my skillset, so I asked Ahmed's help. We used Rhino to create a file. Operations included scaling, extruding and booolean differences. The end result had a different dimensionality that the sketches but made more sense.

![](https://i.imgur.com/97bLTpJ.jpg)


See file tarotbox.3dm



- [ ] Step 4: 
Transform the Rhino file into 2D for readability by the CNC Machine. Here Adai helped me to think through the logic of the machine and how to change the settings so the file would succesfully engrave when sent to the machine. 

![](https://i.imgur.com/X0UYdcm.jpg)




- [ ] Step 5: 
Cut out a piece of white oak from the larger piece. This we did with the circular saw. It was important to measure right angles properly so we could slot it in the machine well afterwards. 


- [ ] Step 6: 
Eduardo double checked the files and for the last part of the operation which is cutting out the final piece of wood from the larger block, he suggested we use a longer drill bit for the last operation (cuting out the rectangle our of the larger piece of wood) since drilled bits cannot go down more than half their lenght. We then transformed the files to G-Code format and sent them to the printer.

- [ ] Step 7: fix the Oak Piece on the CNC machine in between slots of plywood. Define origin for X Y and Z axes. 
![](https://i.imgur.com/7NbipgO.jpg)


- [ ] Step 8 : Launch job. There were 3 seperate jobs. 
The first one was the back side with the slot for electronics. The second one was the front side with the slots for the booklet, the cars and the microphone. The third one was cutting out the right size out of the larger block - and this is the one we has to change the drill bit. 

![](https://i.imgur.com/Ujp0hGR.jpg)



- [ ] Step 9: 
Sanding the edges and bridges and then thinking about the aesthetics. I had orginally thought I would create a book cover that woul be covered in bacteria-died silk, but in the end the colors did not match quite right so I decided to keep the box open and focus on the aesthetics of the booklet. 







