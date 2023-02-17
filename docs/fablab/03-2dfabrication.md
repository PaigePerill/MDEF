---
hide:
    - toc
---

# February 8th 2023 : 2D Fabrication


**Reflection**

OverView of what we can do with lasercutting technology: 
**Pressfit** is joineries for laser  cutting. Interlocking pattern between the cuts. 
**Stacking** - almost like manual 3D printing because you’re stcking lser cut layers on top of each other. 
**Waffle** - instead of stacking you can mae omnidirectional interlocking parts and use less material. There are speficif software suites to do it. 
**Engraving**  (self explanatory)
**Material Welding** is is using the laser properties to actually weld materials together (eg inflatables) 
**Origami:** the laser can laser the folding patterns 
**Electronics** : You can mark certains areas of the material and fill it with conductive ink - or etch copper 
**Living Hinge** is how to create a flexible material because it’s beeen laser cut in a specific way. 


When we laser cut we have a computer connected to the laser + an extraction system connected via filters to the outside. And then we have compressed air supply to get better results but also avoids materials setting on fire.

Vector files are usually the best files for a laser cutter, but one can also send an image (though it needs to be transformed) 
You can engrave, mark or cut. 

Charts for laser cutting are just guides. You always need to make adjustments - materials can behave differently depending on the humidity, temperature etc. ALWAYS make small tests before you send the whole file. 

Machines work in milimeters - so your files NEED to be in milimeters. 

Save as dxf file if you’re not working in rhino. Or save a rhino file. 

The colors are important. 
Black is for rastering (engraving ) and the rest for vectors.


^^Assignment:Experiment with laser cutting^^

I chose to use the laser cutter to further one of my current projects: Electric Skin. 
My team and I are dropping small amounts of a proteins solution on a biomaterial to generate power. When we do this on a simple alginate sheets, there has been an issue with the material swelling up and creating a mount which interferes with the protein solution staying in place and thus concentrated. So we decided to test what it might mean to laser engrave small wells in the biomaterial to see if it creates better conditions for the proteins to stay in place and dry propserly. 

Step 1 - Draw a simple file in inkscape 
Step 2 - Bring the dxf file to rhino on the iaac cloud, color code the material for rastering (black). Settings: Power : 80, Speed : 100, Hertz : 1000
Step 3 - Place a sample material on laser cutter, focus the beam and launch a test raster. The test is successfull though I see I'll need to run the job a few time to create a well deep enough. 
Step 4 - Place the desired material on the laser, refocus and raster several times until desired depth acheived. Final raster count: 5 passes. 

![](../images//elecskinmov.jpeg)

![](../images//elecskinmov.MOV)

