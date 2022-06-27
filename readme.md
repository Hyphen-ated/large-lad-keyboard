Large Lad Keyboard

148 key keyboard with a Standard US layout at the core. 

Two rows of function keys, 21 keys to the left, and some extras filling in the top right, along with a rotary encoder.

Nobody is selling this keyboard. If you want one you need to place an order at a PCB fabrication house for the PCB and the plate.

I didn't design a case for this board. I simply attached two pieces of 1/2" square dowel across the top and bottom rows of holes in the plate. If you'd like to design a case I'd be happy to link it here.

PCB: 146 x 490 mm
Plate: 167 x 495 mm

Bill of materials:

* 148x Through-hole diodes (1N4148)
* 147x MX switches
* 147x Kailh hotswap sockets
* 1x Rotary encoder
* 1x WeAct STM32F411CEU6 V3.1 "Blackpill" (or a similar board with the same pinout)

It works with QMK firmware, see my fork here: TODO

Loading firmware: 
* On the blackpill, hold BOOT and press NRST, then release both
* Open STM32CubeProgrammer. Make sure it's connected to the blackpill on the right under "usb configuration"
* Click "open file" and load the QMK hex file built for this board
* Click "download"