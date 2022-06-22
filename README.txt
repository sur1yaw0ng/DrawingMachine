# DrawingMachine



###	FABRICATION NOTES	###
The structural parts we ordered didn't have the same cross section as the pieces that
came on the Ender. Reference drawings are included in the rhino model, but the original
ender pieces have a 45 degree chamfer to accept the geometry of the wheel more readily.
I didn't understand at first how the adjustment on the wheels worked, so assumed that the
best way to get the wheels to work with the new pieces was to machine a chamfer in the relevant tracks.
The chamfer was done on the bridgeport with a 45 degree router bit. Even though it's not strictly
necessary, I think that having some amount of chamfer will help the wheels operate as they should, 
and stay firmly seated in the track.

The 3d Printed parts included in the model are the first iteration I printed, but the tolerance was too
tight for the parts that are supposed to fit into the t-slots, and the pieces failed. Soon to re-tool the parts
for a second round.

The bed modeled is configured to have four support/adjustment points as on the original ender, may be
worth adding more since the bed is so large, to help avoid flexing?



###	CODE NOTES		###
All the code necessary is in the foilder Marlin-bugfix-1.1.x, which is the version compatible with the 8-bit
board present in the prototype. After the bootloader is burned with the arduino, the arduino IDE should be able
load new firmware onto the ender via a direct USB connection. Newer motherboards will be compatible with newer 
versions of Marlin, as well as accept new firmware via the SD card



###	RHINO NOTES	###
Use command SaveSmall to make files smaller than 100mb to work with GitHub



###	FLASHING BOOTLOADER	###
Only necessary for older motherboards. Requires Arduino Uno/Micro and jumper wires. Tutorials linked below:
https://howchoo.com/ender3/ender-3-bootloader-firmware-update-marlin
https://all3dp.com/2/ender-3-pro-firmware-update-marlin/
https://www.th3dstudio.com/hc/guides/bootloader/bootloader-flashing-guide-cr-10-ender-2-3-5-wanhao-i3-anet-1284p-boards/



###	SPLASH SCREEN		###
Black and white image at 128 x 64 pixels, input into link provided below
to convert into text bitmap to input in code.
Copy and paste resulting text into _Bootscreen.h using Arduino IDE

https://marlinfw.org/tools/u8glib/converter.html



###	BED SIZE		###
Bed size is defined in Configuration.h, lines 877-878



###	MACHINE NAME		###
Machine name is defined in Configuration.h, line 132