# specs_keys - REV 1 (confirmed working, typing on it now :D)

### TKL ISO keyboard based on an g80-3000HAD running QMK

20 Years ago I found 2 g80-3000 HAD Keyboards in the trash, one broke lately so I designed a PCB to mount these sweet sweet Cherry MX black switches on it.

The base plate is the acryl plate from an old TFT Monitor cut to size and sanded. (roughly)
Between PCB and baseplate is some foamy stuff for dampening.


So, except the pcb and the mcu and a couple smd parts this thing is completly salvaged from trash (45 € where 40€ were the PCBs, still have 3 if you want one)

Features  :
  - ATMega 32U4 @ 8 MHz (why the crystal ... such a waste, sigh)
  - USB-C jack **with FUSE and full ESD protection** (gnd vcc d+ d-)
  - MOSFET controlled bottom backlighting pads for 14 LEDs with resistors plus 2 extra 2mm connectors for lantern style lightning
  - Scroll and caps indicators (active low atm.. I kinda like it)
  - SPI interface and reset
  - 340mA overall power consumption with full lights


the QMK layout and config can be found here :  https://github.com/specs32/specs_keys/tree/main/specskeys

I hex the MCU with avrdude from cli after QMK compile, somehow I had trouble with bootloaders all my life ^^ (also safer this way .. I guess;))

> qmk_firmware [master]× » avrdude -c usbasp -p m32u4 -B10 -U lfuse:w:0xD2:m -U hfuse:w:0x98:m -U efuse:w:0xFF:m

> qmk_firmware [master]× » avrdude -c usbasp -pm32u4 -B10 -Uflash:w:.build/specskeys_default.hex                

designed with kicad nightly Version: (5.99.0-10004-g132ec37b56), release build
and some gimp

credits to evyd13 , evil80 and ebastler for initial ideas.

License : CC-BY-NC-SA

![3d-VIEW](https://github.com/specs32/specs_keys/blob/main/gh80-3003-nicosmod/gh80-3003-nicosmod.png)

![PCB](https://github.com/specs32/specs_keys/blob/main/gh80-3003-nicosmod/pcb.png) 

![FOTO1](https://github.com/specs32/specs_keys/blob/main/photo_2021-05-04_18-33-33.jpg)

![FOTO2](https://github.com/specs32/specs_keys/blob/main/photo_2021-05-04_18-33-43.jpg)
