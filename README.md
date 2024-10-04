# MINI-SDVX
A mini controller for games such as Sound Voltex, USC, KShoot, osu 4k, etc.  Based off of mon's Pocket Voltex!

## Thanks To
- Everyone in the Cons & Stuff Discord channel.
- mon for his initial development of the Pocket Voltex.
- CrazyRedMachine for HID stuff

## Features
- Super small - About 7" x 4" and a little over 1/2" high (About 1-1/2" including knobs)
- 7 Gateron Red Keyswitches (Start, BT-A, BT-B, BT-C, BT-D, FX-L, FX-R)
- Reactive & HID LEDs
- PBT G20 Keycaps
- Quality Bourns Encoders (VOL-L, VOL-R)
- Solid Aluminum Black 20mm Knobs
- 6 Rubber Feet
- Single Screw Back Panel
- Arduino Pro Micro based
- Acts as a gamepad or keyboard/mouse.  While plugging in, hold BTN-A for 3-4s for gamepad mode.  Hold BTN-B instead for keyboard/mouse mode.
- USB-C Input

## Parts Required:
- 1x 3D Printed Case (1.2mm walls, top, bottom layers; 20-25% infill minimum)
- 1x 3D Printed Cover
- 7x Gateron Red Keyswitches (or other similar MX-style switch)
- 2x Bourns PEC16-2015F-N0024 Encoders
- 1x 1x1 G20 Keycap
- 4x 1x1.25 G20 Keycap
- 2x 1x2 G20 Keycap
- 2x 20mm Diameter Solid Aluminum Knobs (17-22mm height, 6mm inner diameter hole)
- 1x Arduino Pro Micro
- 6x Rubber Feet (0.8-1cm in diameter)
- 1x Micro USB Male to USB C Female (27cm length)
- 1x M3x5 Screw
- Cat5e Cable (~2 feet, strip it open and take a twist of wire)
- Hot Glue
- Solder
- USB C cable (preferably one with deep insertion)

## LED Parts Required:
- 7x 2x3x4mm Square LEDs (choose your desired colors)
- 7x Resistors (High brightness 100Ohm, Medium brightness 220Ohm)

## Recommended Tools/Etc.
- Temperature Controlled Soldering Iron
- Hot Glue Gun
- Needle Nose Pliers
- Wire Cutter/Stripper
- Phillips Screwdriver (if you use a phillips head M3 screw)
- Allen Key (for knobs' grubscrew, M3 screw if you have a hex head)
- Rubbing/Isopropyl Alcohol
- Microfiber Cloth (for cleaning w/ alcohol)
- Eye Protection + Safety Mask

## General Assembly Instructions
- 3D print case and cover.
- Insert Gateron switches and secure each corner of the switch with hot glue on the inside.
- Using a soldering iron, tin all contacts on the Gateron switches.
- Wire up all the common/ground for the switches and the encoders.
- Wire up all the switches and encoders with their own individual wire.
- Solder all the wires to the board.
  - Arduino Pro Micro Pinout
    - VOL-L A 2
    - VOL-L B 3
    - VOL_R A 0 (RXI)
    - VOL_R B 1 (TXO)
    - BT_ST   4
    - BT_A    5
    - BT_B    6
    - BT_C    7
    - BT_D    8
    - FX_L    9
    - FX_R    10
- Plug in your arduino and flash firmware. Note: If you are running into the "Using OLD HID" error, try enabling verbose compilation output under File > Preferences > Show Verbose Output during [compilation] and uploading again.  For some reason, this fixes it for me most of the time.
- BOOT IN KEYBOARD MODE(Hold the second button from the left for 3-4s while plugging it in).  TEST to make sure everything works.
- Plug in micro usb to USB-C adapter cable into the arduino.  Slide arduino into its slot and route the USB-C cable.
- Push encoders through their holes.  Mount with washer and nut.
- Bend metal encoder mounting tabs 45 degrees outward.  Additionally, bend one of the protrusions slightly inward so it doesn't collide with the micro usb cable.
- Do some cable management.  Carefully flatten the cables.
- Hot glue USB-C port.
- Slide in the cover and secure with M3x5 screw.  PLEASE be careful, as you are threading into plastic and thus the hole is easily strippable.
- Wipe circles on the bottom with rubbing/isopropyl alcohol.  Apply adhesive rubber feet.
- Mount keycaps.
- Mount knobs.  Use the arduino pin headers as a spacer on each side so the knobs are the same height and don't rub on the encoder nub.
- Flash firmware and setup your desired game.
  - Arduino IDE: https://www.arduino.cc/en/main/software
  - KONAMI SPOOF NO LONGER NEEDED - JUST SELECT "ARDUINO LEONARDO"

## HID LED Assembly Instructions
- Take off keycaps.
- Insert LED through switch.
- Solder negative(shorter) leg to the switch's leg that connects to ground/common.  Clip LED shorter if needed.
- Solder resistor(100 or 220 Ohm depending on desired brightness) to positive(longer) leg.  Clip LED & resistor shorter if needed.
- Solder other end of resistor to a wire.  The other end of the wire will be soldered to the Arduino Pro Micro.
  - Arduino Pro Micro Pinout for LEDs
    - BT_ST_LED 16
    - BT_A_LED  14
    - BT_B_LED  15
    - BT_C_LED  18 (A0)
    - BT_D_LED  19 (A1)
    - FX_L_LED  20 (A2)
    - FX_R_LED  21 (A3)
- Plug in your arduino and flash firmware if it needs to be updated.
- Flatten cables and close cover.
### Done.  Enjoy!!

## Links I used to make the first batch of 3
- Gateron Red Keyswitches: https://kbdfans.com/collections/gateron-swithes/products/gateron-swtich-3pin-or-5pin?variant=35765199373
- Bourns PEC16-2015F-N0024 Encoders: https://www.mouser.com/ProductDetail/Bourns/PEC16-2015F-N0024?qs=sGAEpiMZZMsWp46O%252Bq11WTXwm4kPVvHwmPh3cKfowck%3D
- 1x1 G20 Keycap (BCT): https://pimpmykeyboard.com/g20-1-space-pack-of-10/
- 1x1.25 G20 Keycap (WAN): https://pimpmykeyboard.com/g20-1-25-space-pack-of-4/
- 1x2 G20 Keycap (NEM): https://pimpmykeyboard.com/g20-2-space-pack-of-4/
- 20mm Diameter Solid Aluminum Knobs: https://www.aliexpress.com/item/32912465745.html?spm=a2g0o.cart.0.0.43bd3c00dwdyAf&mp=1
- Arduino Pro Micro (WARNING: CONTAINS 10): https://www.aliexpress.com/item/4000045084392.html
- Rubber Feet: https://www.ebay.com/itm/50PCS-Rubber-Feet-Clear-Semicircle-Bumpers-Door-Silicone-Buffer-Pad-Furniture/152925672374
- Micro USB Male to USB C Female: https://www.aliexpress.com/item/32983342667.html
- M3x5 Screw: https://www.ebay.com/itm/20X-M3-3-80mm-Round-Pan-Head-Phillips-Screws-304-Stainless-Steel-Machine-Screws/302237442873
- USB C cable (WARNING: CONTAINS 10): https://www.aliexpress.com/item/33032210292.html

## Links I used for LEDs
- 2x3x4mm LEDs: https://www.aliexpress.com/item/4000463652201.html
- 100Ohm Resistors: https://www.ebay.com/itm/100PCS-1-4W-0-25W-Metal-Film-Resistor-1-Full-Range-of-Values-0%CE%A9-to-10M%CE%A9/252838503547

## Alternate Parts to Consider
- DSA profile keycaps might be a good alternative to G20 if G20 is too expensive or hard to get.
- 20mm knobs can be picked up for much cheaper if you opt for ones that are not all aluminum.
- Cherry MX O-Ring Dampers can be used for a quieter and softer bottom-out.  I had to put 2 on FX-L and FX-R each for dampening to work.  The rest of the keycaps have 1 O-Ring.

## Links to other GitHubs
- https://github.com/mon/PocketVoltex

## Possible To-Do List
- M3 Nut hole on cover
- Increase spacing between BTN and FX
- Tweak vinyl skin aesthetic button size cutouts
- Consider new way to secure back panel
