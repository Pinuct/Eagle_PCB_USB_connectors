[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

# Eagle PCB USB connectors
Eagle library for USB connectors directly on PCB.

This repository contains documentation and a library to use with Eagle to create USB connectors directly on the PCB itself (free connectors!). By the moment the only usb connectors are the USB micro B and the USB type C. This only works with PCB thickness of 0.6 mm. 

The [eagle_library](https://github.com/Pinuct/Eagle_PCB_USB_connectors/tree/master/eagle_library) folder contains the Eagle library

The [Connector Test](https://github.com/Pinuct/Eagle_PCB_USB_connectors/tree/master/Connector%20Test) folder contains and eagle proyect of the test PCB i used to test the different models of USB pcb patterns i made.

The [micro USB type b](https://github.com/Pinuct/Eagle_PCB_USB_connectors/tree/master/micro%20USB%20type%20b)and [micro USB type c](https://github.com/Pinuct/Eagle_PCB_USB_connectors/tree/master/micro%20USB%20type%20c) folders contains documentation i used to make this proyect, it includes the PDFs of the USB spefication of each type of USB with all the data, dimensions and pinout i used to create the Eagle components. Also includes the images os the dimensions an pinout extracted form the PDF.

## Why?

I started this proyect because i wanted an easy and cheap method to connect my electronic boards to a PC. I don't wanted a realiable connector for thousands of uses, i wanted just an ocasional connector to hook up to my PC and program it, or take some data. So this type of connector are just fine for that pruporse, not soldering, not extra cost, not uncommon cables, just a mirco B cable and your are good to go. The only problem with this type of connectors is that you have to use 0.6 mm PCB thicknes, and today mosts PCB fabs can do 0.6mm thicknes without extra cost. If you are ok with that, there we go!


## Extra info

<center>
  
| USB micro B mid plate dimensions  | USB type C mid plate dimensions |
| ------------- | ------------- |
| <img width="300" height="200" src="https://github.com/Pinuct/Eagle_PCB_USB_connectors/blob/master/micro%20USB%20type%20b/images/receptacle%20front%20view%20(inside).png?raw=true">  | <img width="300" height="200" src="https://github.com/Pinuct/Eagle_PCB_USB_connectors/blob/master/micro%20USB%20type%20c/images/receptacle%20side%20section%20(detail).png?raw=true">  |

</center>

As you can see, both mid plates have 0.6 mm thickness. Is true that the pads itself are not below or above that dimension, but the diference is so small it doesent matter. So 0.6mm thinckes PCB and we are fine.

  In the library there are three components:

  - **PCB_MICRO_USB_B** 
  - **PCB_USB_C**   
  - **PCB_USB_C_2.0** 
  
In PCB_MICRO_USB_B there is pads only in one side (it can't be both sides because the USB plug in the micro B cable has a metalic back and it can short the pads). In the other hand, the USB type C is created to inset either way so PCB_USB_C and PCB_USB_C_2.0 has pads on both sides.
  
The difference between the PCB_USB_C and the PCB_USB_C_2.0 is that the PCB_USB_C_2.0 has extra wires and vias to convert the PCB_USB_C into a USB 2.0 specification compatible, that means that you only use 4 lines of the connector: V+, GND, D- and D+. 
  
Each one of the components have different footprint models. The difference in the models is in the cutout slots for the usb cable plug to insert on the PCB, i played with the thicknes of the slot and the terminations. I can say that in the PCB_MICRO_USB_B the one that work for me the best is the one with the tighter dimensions with the round end to give the connector a little bit more space to insert further inside. For the PCB_USB_C/2.0 i can't say which one is the best because i couldn't test it yet.
  
**USB micro B footprints:**

<img  src="https://github.com/Pinuct/Eagle_PCB_USB_connectors/blob/master/micro%20USB%20type%20b/images/footprints.png?raw=true">
