## Large Lad Keyboard

![picture of keyboard](https://i.imgur.com/CQWAD2X.jpg)
![picture of PCB and plate](https://i.imgur.com/Z27w4RX.jpg)
148 key hotswap keyboard with a Standard US layout at the core. 

Two rows of function keys, 21 keys to the left, and some extras filling in the top right, along with a rotary encoder.

Nobody is selling this keyboard. KiCad project files are in this repo. If you want one you need to place an order at a PCB fabrication house for the PCB (and the plate. Or get the plate made elsewhere.) I got the plate made as a "PCB" with 1.6mm aluminum; if you want to try FR4 maybe that would work too.

I didn't design a case for this board. I simply attached two pieces of 1/2" square dowel across the top and bottom rows of holes in the plate. If you'd like to design a case I'd be happy to link it here.

* PCB: 146 x 490 mm
* Plate: 167 x 495 mm

Other materials you will need:

* 148x Through-hole diodes (1N4148)
* 147x MX switches and keycaps
* 147x Kailh hotswap sockets
* 1x set of stabilizers for a full sized keyboard
* 1x Rotary encoder, clickable. (The kind used on keyboards.)
* 1x WeAct STM32F411CEU6 V3.1 "Blackpill" (or a similar board with [the same pinout](/blackpill.png)

If I were to make a rev 2 of this, I would enlarge the stab holes in the plate. I had a rough time getting it to fit and I needed to file down a few edges in the plate. I also intended the plate to have (black) soldermask on top, but I messed that up so the top is bare aluminum right now. (The plate also has a few plated holes in it that don't do anything. This was recommended to me as a way to make PCB fab houses less likely to reject the design for not looking like a PCB. I'm not sure why a business would want to not take someone's money in this way, but whatever.)

Assembly: solder in the diodes and encoder on top, sockets and MCU on bottom. (I used peel-away strips for the MCU to help reduce the vertical size of the overall build while having the MCU socketed for easy removal.) Then attach your stabs to the PCB, put the plate on, and put the switches in. The switches are the only thing holding the PCB up. Then figure out how to mount the plate to some kind of case or just use pieces of wood like I did.

It works with QMK firmware, see my fork here: https://github.com/Hyphen-ated/qmk_firmware

The matrix is a bit of an [unholy nightmare](/keyboard-layout-colors.png) at 12x13. It needs to be much squarer than the layout actually is, because there aren't enough pins otherwise.

Loading firmware: 
* On the blackpill, hold BOOT and press NRST, then release both
* Open STM32CubeProgrammer. Make sure it's connected to the blackpill on the right under "usb configuration"
* Click "open file" and load the QMK hex file built for this board
* Click "download"

Shoutouts to [ai03](https://wiki.ai03.com/books/pcb-design/page/pcb-guide-part-1---preparations), https://github.com/piit79/Kicad-STM32, https://github.com/chgray/daprice-keyswitches, https://github.com/daprice/keyswitches.pretty, http://builder.swillkb.com/, http://www.keyboard-layout-editor.com/
