Improved Video Board for Yamaha YIS805 MSX2/MSX2+ version 1.0
Copyright (c) 2019 RBSC


WARNING!
--------

The pinout of the RGB connector on the new video board differs from the original pinout! On the new board pin 3 is connected to
+12v supply. When making RGB to SCART cables or when using such cables designed for the Japanese MSX mashines, please make sure
that you connect the +12v to the correct SCART pin - pin 8. Connecting +12v to this pin will switch the TV/monitor to 4:3 mode.

DO NOT use this video board with Yamaha YIS503 computers! The layout of the motherboard's connector is different there and you
will cause severe damage to the video board if it's connected to an incompatible computer!

It is advised to power down the computer before switching between PAL and NTSC in order to avoid damage to the encoder chip.


Settings
--------

There are three 3-pin jumpers on the video board. These jumpers are used to set the color encoding for the S-Video and composite
video outputs. All jumpers must be set the same way. When the pins 1-2 of the jumpers are shorted, the NTSC encoding is enabled.
Otherwise, when pins 2-3 of the jumpers are shorted, the PAL encoding is enabled. Please note that the jumper settings do not
affect the RGB output.

Each on-board clock generator can be disabled by setting a jumper under the corresponding quartz resonator. This is done to disable
the unused clock generator in order to avoid interference. For example when using PAL clock, it is highly recommended to disable
the on-board NTSC clock generator.

There are 2 jumpers on board marked ONBOARD and EXT. One is for enabling the frequency from the on-board's NTSC clock generator,
the other is for providing the NTSC frequency from the motherboard. Only one jumper must be set at any time! When using the
external clock, it's recommended to disable both on-board generators.

When setting up the board, it's recommended to measure the voltages on the outputs of 4 potentiometers (variable resistors). The
correct voltage setting is required to form the picture on the composite video and S-Video outputs. The recommended voltage for
the CSYNC variable resistor is 1.3v, the recommended voltages for Red, Green and Blue variable resistors is from 1.5v to 2.0v
depending on the desired saturation. The voltages on R, G and B must be the same to avoid color disbalance. Each color should be
tuned after setting it as the background color - for example when setting the blue color's voltage, use the "color15,4,4" command
in MSX Basic and set the desired saturation of blue color.


Notes
-----

Please use the following quartz oscillators: 3.579 MHz for NTSC and 4.433 MHz for PAL. Using other oscillators may cause
undesired side effects.

It is advised to use the 74HCT04 chip for the frequency generator circuit. The LS and HC series chips may also work, but the
HCT series is highly recommended.

There may be artefacts on the color transitions in the composite video's output. These artefacts can be removed by carefully
adjusting the corresponding trim capacitors (C14 or C20).

The sharpness of the composite video output can be adjusted by the C23 trim capacitor that is marked as "YTRAP". Please use the
screwdriver with a non-conductive handle to adjust the sharpness.

If you are using a jumper pin row instead of the original cable connector, be careful to connect the cable from the MSX's main
board correctly. Incorrect cable connection can damage the video board and MSX!

It is advised to install the angled 13-pin connector for the motherboard's cable onto the video board. This connector prevents
the cable from touching the upper part of the metal shielding above the board.


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided information,
software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small amount of bare boards for
personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the copyright!


Contact information
-------------------

The members of RBSC group Wierzbowsky, Tnt23, Ptero, Pencioner and DJS3000 can be contacted via the MSX.ORG or ZX-PK.RU forums.
Just send a personal message and state your business.

The RBSC repository can be found here:

https://github.com/rbsc

The MSX-related 3D models published by RBSC can be found here:

https://www.thingiverse.com/groups/rbsc/things

-= ! MSX FOREVER ! =-
