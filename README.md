# nrF52840_reference_PCB

This is a reference design for the nrF52840 for easy SWD programming and testing.  This layout uses the nrF52840 module from Raytek called the [MDBT50Q](http://www.raytac.com/upload/download_files/1bca545683ea4caf48e1ec796c09b9d9.pdf).
This PCB has been tested and it works!  This design relied heavily on the work of [Adafruit's feather board](https://www.adafruit.com/product/4062).


![](https://github.com/hydronics2/nrF52840_Reference_PCB/blob/master/front_view.png)

I'm building an introduction class where I'd like to introduce students to soldering class, circuit python, and Internet of Things (IOT).  This reference board is a good start. The changes from the feather are:
- broke out more pins
- changed the FLASH to an SOIC package
- changed some other packages slightly for easier soldering


You can order boards from Oshpark using this link: [project](https://oshpark.com/shared_projects/A5jKStz9)

Here's a list of parts:


- ATSAMD21E15B from [digikey](https://www.digikey.com/product-detail/en/microchip-technology/ATSAMD21E15B-AFT/1611-ATSAMD21E15B-AFTCT-ND/6832773). Don't get the ATSAMD21E15L!... the pinout is slightly different.
- 10 pin SWD Header from [digikey](https://www.digikey.com/product-detail/en/microchip-technology/ATSAMD21E15L-AFT/1611-ATSAMD21E15L-AFTCT-ND/6832779)
- generic 5.08mm pitch screw headers (or 5mm)
- 	FIXED IND 10UH 500MA 300 MOHM [digikey](https://www.digikey.com/product-detail/en/tdk-corporation/MLZ2012N100LT000/445-6762-1-ND/2523583)
- 3.3V Regulator (18V max input) [mouser](https://www.mouser.com/ProductDetail/511-LDL1117S50R)
- T0-252-3 Mosfet (not needed) [mouser](https://www.mouser.com/ProductDetail/ON-Semiconductor-Fairchild/FDD8780?qs=%2fha2pyFadugI30EyIBTPkO8PumBRFL59Ls98N48NSzc%3d)
- USB micro connector [digikey](https://www.digikey.com/product-detail/en/amphenol-icc-fci/10118194-0001LF/609-4618-1-ND/2785382)
- standard 6mmx6mm tactile button [sparkfun](https://www.sparkfun.com/products/97)
- screw terminal 5mm pitch [sparkfun](https://www.sparkfun.com/products/8432) or [aliexpress](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20190221221755&SearchText=pcb+screw+terminal)
- input protection diodes on the 12V and USB input into the regulator. This is Adafruit's design. [digikey](https://www.digikey.com/product-detail/en/diodes-incorporated/B130-13-F/B130-FDICT-ND/815318)
- 32.768khz crystal (if needed, see above trinket design) [digikey](https://www.digikey.com/product-detail/en/epson/FC-135-32.7680KA-AG3/SER4086DKR-ND/6132726)
- crystal capacitors C7/C8 based on a 7pf load from the above crystal and assumed 2pf stray capacitence, CX1 = CX2 = 2(7pF - 2pF) = 10pF [digikey](https://www.digikey.com/product-detail/en/wurth-electronics-inc/885012006051/732-7793-1-ND/5454420)


SWD Programmer/Debugger: [Segger](https://www.digikey.com/product-detail/en/segger-microcontroller-systems/8.08.91-J-LINK-EDU-MINI/899-1061-ND/7387472)

![schematic](https://github.com/hydronics2/samd21_QFP_reference_PCB/blob/master/schematic.JPG)

Notes:
- add a ground plane
- chagne the silkscreen to SAMD21E15
- change the silkscreen C7/C8 from 15pf to 10pf
