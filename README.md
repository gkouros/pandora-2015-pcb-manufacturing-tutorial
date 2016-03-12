## Welcome to P.A.N.D.O.R.A. PCB Design And Manufacturing Tutorial

![pandora-logo](https://github.com/gKouros/pandora-2015-pcb-manufacturing-wiki/blob/master/images/pandora-logo.png)

![pandora_pcbs.jpg](https://github.com/gKouros/pandora-2015-hardware-wiki/blob/master/images/pandora_pcbs.jpg)

#####In this tutorial we will look into the manufacturing process of printed circuit boards (PCBs). We will go through the process, step by step, from designing to manufacturing, while examining and comparing the different methods and techniques, to find the optimal solution.

##Quick Overview of PCB Design using CadSoft EAGLE PCB Design Software
Before we begin, consider taking a look at [P.A.N.D.O.R.A. PCB Design](https://github.com/klpanagi/Pandora_Wiki/wiki/PCB-Design), to familiarize yourself with EAGLE, why we use it and how to install it, as well as read some helpful material on electronic circuits and PCB design.

The process of PCB design in CadSoft EAGLE, basically involves the following steps:

1. Create a new project
2. Design the schematic of the circuit board using the schematic editor
3. Arrange and route the board, using the board editor
4. Check the board for errors using the Design Rule Check (DRC) and Electrical Rule Check(ERC)

If you would like to delve deeper into the mysteries of PCB design, you could take a look at some PCB design tutorials, by following the links below:

- [Draw Electronic Schematics with CadSoft EAGLE](http://www.instructables.com/id/Draw-Electronic-Schematics-with-CadSoft-EAGLE/)
- [Turn your EAGLE Schematic into a PCB](http://www.instructables.com/id/Turn-your-EAGLE-schematic-into-a-PCB/)
- [Using EAGLE: Board Layout from Sparkfun](https://learn.sparkfun.com/tutorials/using-eagle-board-layout)
- [Getting started with CadSoft EAGLE video tutorial](https://www.youtube.com/watch?v=R4DYztYB6d4)
- [CadSoft EAGLE video tutorials from Jeremy Blum](https://www.youtube.com/playlist?list=PL868B73617C6F6FAD)

## Exporting the PCB Artwork
So, we designed our circuit board and all is well, but, what do we do with it?
We have two choices. We, either, generate gerber files and send them off to a "fab house", or we print the design and fabricate the PCB ourselves. 

For the easy (but expensive) way out, click on the following link: [**I am a disgrace to my family**](https://learn.sparkfun.com/tutorials/using-eagle-board-layout#generating-gerbers), to learn how to produce gerber files.

Moving on...

Before we export the PCB artwork, we need to select the layers that will be visible on the artwork.
So, click on **View > Layer** settings and select **Pads, Vias** layers as well as **Top** layer for the top side or **Bottom** layer for the bottom side
(Also if you are making a double sided PCB, it'd help to select the *Dimension* layer as well, since it makes the matching of the two sides easier)

In order to export the artwork for printing, we have the following choices:
- Export as pdf
    - Click **File > Print**
    - Select Print to File, Scale Factor=1 and check Black and Solid (and Mirror for TOP layer)
- Export as image
    - **File > Export > Image**
    - Write image name, check Monochrome, select Resolution=300/600 dpi and click ok

Each exporting choice has its pros and cons. The good thing with the first choice is that you create a pdf file with the PCB artwork, which you can print immediately, but the downside is that you can print only one board at a time, which is a waste of paper and money for small boards. In contrast, the second exporting method, needs more work, but is more efficient, since you can populate a single sheet with as many boards, as you want, by copying and pasting the image in a word document and later exporting it as pdf. Plus, with the second option you can process the artwork in an image editor (eg. paint.net for windows and pinta or gimp for linux etc) and make corrections, add sketches, signatures, the story of your life and anything you can imagine, that is not possible in EAGLE.


## Printing the PCB Artwork
Printing, as simple as, it sounds, is actually fairly complicated.

First and foremost, it is of grave importance, that the PCB artwork is printed on scale. A little smaller or larger and the components will not fit. So, whether you are printing it or getting it printed in a store, ensure that the artwork is printed on scale 100%.

Secondly, not all printers are up for the task. You should only use Laser printers, and always select highest quality printing.

Last, but not least, we need to select a suitable kind of paper for the task. This, however, depends on the PCB manufacturing method, we choose. So, for the **toner transfer method** we can use *glossy paper, magazine paper, or photo paper*, while for the **uv exposure method** we can only use *transparencies*. 

## PCB Artwork Transferring Methods
In this tutorial we examine two of the most common PCB Artwork Transferring Methods:
- the **Toner Transfer Method** and
- the **UV Exposure Method**

### Toner Transfer Method


What you will need:
- An iron
- Acetone
- Paper Towels
- A plastic container with warm soapy water
- A copper board
- The PCB Artwork printed on glossy, magazine or photo paper
- Scissors

PCB Artwork Transferring Steps:

1. First clean the copper board thoroughly using the acetone and paper towels. If the surface is not clean enough, the toner will not stick to the copper.
2. Cut the PCB Artwork same size as the copper board for single sided PCB and larger than the copper board for double sided PCB.
3. For single sided PCB put the artwork on top of the copper side of the board with the toner facing the copper. For double sided PCB, align the bottom to the top side of the artwork, with the toner sides facing each other and hold them together with masking tape. Don't forget to leave an opening, to insert the copper board.
![toner_transfer_copper_and_artwork.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/toner_transfer_copper_and_artwork.jpg)
4. Preheat the iron to the maximum setting.
5. Put a paper towel on top of the board and iron the board for about 3 minutes (on each side for double sided boards), while applying constant firm pressure. Towards the end, press every inch of the board with the corner of the iron.
![toner_transfer_ironing.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/toner_transfer_ironing.jpg)
6. Leave the iron aside, and let the ironed board to cool.
7. Soak the board in warm soapy water for at least 20 minutes.
8. Start peeling the paper on the board, by rubbing it with your fingers (no nails) or a toothbrush, until only the toner artwork remains on the copper.
9. Put it aside to dry.
10. The board is ready for etching!

### UV Exposure Method


The UV Exposure Method is more complicated, than the toner transfer method, requires more specialized equipment and a lot of trial and error to master, but is more reliable and offers greater accuracy and detail.

What you will need:
- A UV Exposure Box
- Photo-positive PCB
- PCB Artwork printed on transparency paper (x2 for each side)
- A plastic container
- Gloves
- Sodium Hydroxide (NaOH - main ingredient in most drain cleaners you can find on supermarkets)


PCB Artwork Developing Steps:

1. Check the artwork on the transparency under strong light, to see if light goes through the toner. If it does, simply glue together two transparencies with the same artwork.
2. Peel off the blue protective cover of the photo-positive PCB.
![photopositive_pcb.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/photopositive_pcb.jpg)
3. Put the transparency with the PCB artwork on the PCB and use masking tape to hold them together.
![pcb_with_transparencies.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/pcb_with_transparencies.jpg)
4. Put the PCB with the transparency in the UV exposure box. Put something heavy on top to hold the transparency flat and pressed on the copper board.
![uv_exposure_box.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/uv_exposure_box.jpg)
5. Expose the board to UV light. Optimal exposure time depends on the exposure system and needs some experimentation to perfect, in order to avoid overexposure and underexposure. In our UV exposure system, which uses UV LEDS, about 10cm away from the PCB board, we found 7 minutes, to be optimal.
6. Mix 300ml of water with half of a teaspoon of NaOH(drain cleaner) and stir the solution until the NaOH crystals are dissolved in the water.

   ![drain_cleaner.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/mr_muscle.jpg)

7. Remove the transparencies from the copper board.
8. While wearing gloves, hold the board inside the NaOH solution and shake it until the artwork is developed clearly. Don't leave it inside, for too long, or the artwork will dissolve too.
9. Remove the board from the NaOH solution and rinse it with water.
10. The board is ready for etching!


## PCB Etching and Finishing Touches
The process of PCB Etching involves the use of chemicals to strip the, unprotected from toner/film, copper areas, of the PCB. There are several chemicals you can use, but the process is pretty much the same for all of them. In this tutorial we will use a solution of hydrogen peroxide and hydrochloric acid, although you can, also, look into other common etchants, such as ferric chloride or sodium persulfate.

What you will need:
- A copper board with artwork printed on it
- 2 plastic containers large enough to fit your PCB
- Gloves
- A bottle of hydrochloric/muriatic acid (deep orange bottle found at supermarkets). 15% concentration will do, but if you can get higher (eg. 30%), go with it.
- A bottle of 3% hydrogen peroxide, found in all pharmacies.
- Acetone
- Paper Towels
- A soldering iron/station
- Solder
- Flux
- Solder Pump
- A dremel or a tabletop drill press + drill bits(0.5mm to 3mm)

Etching Steps:

1. Fill one of the plastic containers with water 
2. Wear Gloves.
3. Pour, on the other container, 2/3 hydrogen peroxide and 1/3 hydrochloric acid.
![pcb_ethant.jpg](https://github.com/gKouros/pandora-hardware-wiki-2015/blob/master/images/F1HIQARGZLW97JY.LARGE.jpg)
4. Put the board in the solution.
5. Shake the container, constantly, until the unwanted copper dissolves. If the solution turns light blue, add more acid. If turns dark green, add more peroxide.
6. After the etching is complete, remove the board from the solution and throw it in the water container to stop the etching.
7. Remove the board from the water and let it dry.
8. Pour some acetone on a paper towel and rub the board, to remove the leftover toner or film, so that only the conductive copper is left.
9. Drill the PCB vias, pads and holes using either a dremel or a tabletop drill press and different sizes of drill bits, depending on the hole size.
![pcb_drilling.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/pcb_drilling.jpg)
10. Place the components, one or two at a time, before soldering them.
    - Always solder the shortest components first.
    - Use rivets, resistor legs or headers for vias.
    - Use a third hand tool or a vice to hold the PCB.
    - Don't leave the soldering iron on a pad/vias for too long, or the copper will come off.
    - Use a soldering station, so that you can set the temperature depending on the task at hand.
    - Use a solder pump to remove excess solder or to remove a soldered component.
    - Apply flux on a dirty surface to make soldering easier
![pcb_soldering.jpg](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/soldering.jpg)
11. Check the continuity between the components on the board and.
12. Take the PCB for a ride.


Useful links:

- [How to etch a circuit board](http://www.wikihow.com/Etch-a-Circuit-Board) 
- [PCB etching using laser printers](http://www.instructables.com/id/PCB-etching-using-laser-printer/#stepanchor-step3)
- [DIY PCB etching](http://fritzing.org/learning/tutorials/pcb-production-tutorials/diy-pcb-etching)
- [A better etching solution](http://www.instructables.com/id/Stop-using-Ferric-Chloride-etchant!--A-better-etc/)
- [Etching with vinegar, salt and hydrogen peroxide](http://makezine.com/projects/cheap-friendly-and-precise-pcb-etching/)

## Pimp my PCBs

If you are like me, you propably, would like to stop the copper on your PCBs from oxidizing with time and, at the same time, give your PCBs a more professional look. This can be accomplished using:
- Copper tin plating
    - [PCB Electroless Tin Plating](http://www.instructables.com/id/PCB-Electroless-Tin-Plating/)
    - [How to tin a PCB without using expensive tinning solution](http://stompville.co.uk/?p=85)
    - [Liquid Tinning of Home Brew PCB / Tin Plating Copper Clad Circuit Boards](https://www.youtube.com/watch?v=wOqkI-S-wdI)
    - [Tinning a PCB with Bungard Sur Tin](https://www.youtube.com/watch?v=MGbxrRmP-Zs)
![](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/Alldone11.jpg)

- Solder masks
    - [Solder Mask - Wikipedia](https://en.wikipedia.org/wiki/Solder_mask)
    - [DIY Printed Circuit Board With Solder Mask](http://www.jonshobbies.com/diy-printed-circuit-board-with-solder-mask-part-1.html)
    - [Professional Home Brew PCB: Creating a solder mask using UV curable paint](http://www.instructables.com/id/Professional-Home-Brew-PCB-Creating-a-solder-mask/)
    - [Dry Film Solder Mask](http://www.instructables.com/id/Dry-Film-Solder-Mask/)
    - [Solder Mask Colours](http://andybrown.me.uk/wk/2015/01/05/pcb-colours/)
    - [How to apply UV Curable Solder Mask](https://www.youtube.com/watch?v=Vj_cdBZO1Tk)
![](https://github.com/gKouros/pandora-pcb-manufacturing-tutorial/blob/master/images/Final-PCB.jpg)
    

Last, but not least, you could go a step further and take a look into adding silkscreens on your PCBs, in order to give them an even more professional look and at the same time help with placing the components on the board ([DIY PCB silkscreen cheap, easy and fast](https://www.youtube.com/watch?v=M_m1YBTzgvY))



*And don't forget, PCB making, is an art, that you perfect with time and experimentation.*

