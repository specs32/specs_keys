# specs_keys  TKL keyboard based on an g80-3000HAD

## REV 1 (confirmed working, typing on it now :D)

20 Years ago I found 2 g80-3000 HAD Keyboards in the trash, one broke lately so I designed a PCB to mount these sweet sweet Cherry MX black switches on it.

It runs : QMK firmware 
It has  :
  -ATMega 32U4 @ 8 MHz (why the crystal ... such a waste, sigh)
  -USB-C jack with full ESD protection (gnd vcc d+ d-)
  -bottom backlighting
  -Scroll and caps indicators (active low atm.. I like it)
  -SPI interface and reset

the QMK layout and config can be found here :  https://github.com/specs32/specs_keys/tree/main/specskeys

I hex the MCU with avrdude from commandline after QMK compile, somehow I had trouble with bootloaders all my life ^^ (also safer this way ;))

build with kicad nightly Version: (5.99.0-10004-g132ec37b56), release build

credits to evyd13 and ebastler for initial ideas.

License : CC-BY-NC-SA

![3d-VIEW](https://github.com/specs32/specs_keys/blob/main/gh80-3003-nicosmod/gh80-3003-nicosmod.png)

![PCB](https://github.com/specs32/specs_keys/blob/main/gh80-3003-nicosmod/pcb.png) 

![FOTO1](https://github.com/specs32/specs_keys/blob/main/photo_2021-05-04_18-33-33.jpg)

![FOTO2](https://github.com/specs32/specs_keys/blob/main/photo_2021-05-04_18-33-43.jpg)
