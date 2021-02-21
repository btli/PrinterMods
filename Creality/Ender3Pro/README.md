![Ender 3 Mods](https://raw.githubusercontent.com/btli/PrinterMods/main/Creality/Ender3Pro/ender3pro.jpg)
# Ender 3 Mods
I posted a video of my modified Ender 3 Pro in [r/Ender3](https://www.reddit.com/r/ender3/comments/kjvcp1/i_think_its_still_an_ender_lost_track_of_all_the/), and it seems many have gotten 3D printers over the holidays. I put this list together and a few comments about each of the mods to hopefully help people sort through all the things you can do to this printer. There were a lot of comments about relocating the spool holder from the top of the frame on the last post. I had previously used a drybox that was moved to another printer. Giving into the pressure, I've since purchased another one. I can only agree with the Reddit community, it does make a lot of sense since the spool shifts the center of gravity higher introducing added motion to the frame. I also wanted to utilize the resonance compensation feature on [Klipper](https://www.klipper3d.org/Resonance_Compensation.html) and having a changing weight that high on the printer would not be viable. This *should* be the end state of this printer, but who knows, I said that a dozen mods ago. And yes, I could have purchased a more expensive printer, but where's the fun in that?!

*EDIT: Guess it's not over yet, [Voron Switchwire mod](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Gizzle/ender-3_(pro)_switchwire) someday soon!*

## Top 3 Favorite Mods
Did not expect this document to get so long! So I've select what I think are the most important mods, if any, to the Ender 3.
- [OctoPrint](https://octoprint.org/) with [Klipper Firmware](https://www.klipper3d.org/Installation.html)
  - This is a huge quality of life upgrade. Most will likely start with the Cura slicer and there's a [plugin](https://marketplace.ultimaker.com/app/cura/plugins/fieldofview/OctoPrintPlugin) to send prints directly to the printer. One of the strangest mods on my printer is the screen delete. I control and monitor prints exclusively through the Octoprint web interface and the [Printoid mobile app](https://printoid.net/) (I started with Printoid Lite and purchased the pro when I built my second printer).
  - Klipper may not have as many features as Marlin, but in terms of configuration, everything is done via a config file. Fine tuning the printer is far easier with Klippper than Marlin. I was hesitant to make ths switch at first, but after building the Voron printer and using Klipper, I haven't looked back. _HIGHLY_ recommend!
  - Required Materials:
    - [Raspberry Pi 4](https://amzn.to/3rhkuW4)
      - *Any variant works, the [Pi 3](https://amzn.to/3cFrgkm) is also suitable for OctoPrint/Klipper*
      - Consider a [heatsink set](https://amzn.to/36G7Nft) for the Pi as well, it gets a little toasty
    - [MicroSD Card](https://amzn.to/3rdHBRg)
- Automatic Bed Leveling
  - If you're using multiple beds or have warping on the build plate, this upgrade is fantastic. It's also helpful in compensating for a less than perfectly flat bed. Also, everyone's first suggestion for failed prints is to level the bed.
  - Required Materials:
    - [BLTouch Upgrade Kit](https://amzn.to/3cCP48s)
- Hot End Upgrade
  - There's a lot of replacement hotends to choose from. The micro-swiss is a drop in replacement, which I had on the printer for the first few months. It opens up the possibility of printing more material and remedies the bowden tube burning issue. It's a worthwhile investment if you're looking to eventually print materials besides PLA.
  - Required Materials:
    - [Phaetus Dragon Hotend](https://amzn.to/3pPYYqY) *Expensive option, use the standard flow, very unlikely the Ender3 will be printing fast enough to utilize the HF variant*
    - [Micro Swiss All Metal Hotend](https://amzn.to/3cF6BwD) *One of my first upgrades, drop in replacement for the Ender 3. Not the best, but very easy to install*

## Current Printer Mods

### Frame and Bed Mods
- [V-Slot Covers](https://www.thingiverse.com/thing:3248551)
  - https://www.thingiverse.com/thing:3248551
  - Who doesn't like some racing stripes. I printed a mix of red and black.
- LED Holders
  - Top bar for lighting and controlled via Klipper
  - Bottom bar used for temprature and print progress indicators
  - Materials:
    - [Reduced V-Slot Covers](https://www.thingiverse.com/thing:4708685) for the sides in order to run wiring
      - https://www.thingiverse.com/thing:4708685
    - [LED holders](https://www.thingiverse.com/thing:4708698) for WS2812 with 60 pixels per meter
      - https://www.thingiverse.com/thing:4708698
      - [WS2812 LEDs](https://amzn.to/2MPrvOU)
- Linear Rails
  - I don't necessarily recommend this mod. It's expensive for very marginal improvements.
  - Materials:
    - 3x [MGN12H 300mm Linear Rails](https://amzn.to/2Mxf3DF)
    - [Y Axis Carriage](https://www.thingiverse.com/thing:4141819)
      - https://www.thingiverse.com/thing:4141819
    - [X Axis Carriage](https://www.thingiverse.com/thing:4697157) - *Use with Voron Afterburner*
    - https://www.thingiverse.com/thing:4697157
- [Silicone Bed Springs](https://amzn.to/3tqtFW8)
  - The stock springs are terrible, enough said
- [Spring Steel PEI Bed](https://amzn.to/3tojyB8)
- [TPU Damping Feet](https://www.thingiverse.com/thing:4641590)
  - Printed with Hatchbox TPU
    - Alternatively, print with PLA and re-attach rubber feet from stock printer
  - Required to raise the printer for the extended electronics box
- [Electronics Box](https://www.thingiverse.com/thing:4107156)
  - https://www.thingiverse.com/thing:4107156
  - I found the top cover too thick, so you I scaled it down to 2mm Z height in Cura
- [eSUN eBOX](https://amzn.to/3tpDHH6) - Filament Drybox

### Electronics
- Replacement Mainboard
  - [SKR Mini E3 V2.0](https://amzn.to/2YKEPXm)
      - More practical for the Ender 3
  - [SKR 1.4 Turbo Mainboard w/ TMC 2209 Stepper Motor Drivers](https://amzn.to/3rhDa86)
    - I only used the SKR 1.4 since I had extras
      - Clearly I have a problem.. who has these just lying around?!
  - [BTT 5V DCDC Board](https://amzn.to/3ro2oS7) or [DCDC for SKR Mini](https://amzn.to/2YWhwKh)
    - Power for LEDs and Raspberry Pi
- [Raspberry Pi 4](https://amzn.to/3rhkuW4)
  - [OctoPrint](https://octoprint.org/) with [Klipper Firmware](https://www.klipper3)
  - Check the Octoprint Section for my list of plugins
- [Filament Runout Sensor](https://amzn.to/3pQ0rOi)
  - [Sensor Bracket](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/aeresov/TL_filament_sensor_bracket)
- [WS2812 RGB LED Strips](https://amzn.to/2MPrvOU)
- Camera
  - Great for monitoring print progress and creating timelapses
  - USB webcams are a little difficult to source due to the pandemic, but I found the UNZANO camera works very well! The 60FPS is a little overkill, but nothing like super smooth video to monitor your 3D prints.
  - [Camera Arm - Standard Tripod Mount](https://www.thingiverse.com/thing:3095730)
    - https://www.thingiverse.com/thing:3095730
  - Camera Options:
    - Pi Camera or HQ Pi Camera
    - USB Webcam - [Official Octoprint List](https://community.octoprint.org/t/usb-webcams-known-to-work-with-mjpg-streamer/21149) and be sure to [disable autofocus](https://munkjensen.net/wiki/index.php?title=Raspberry_Pi_-_Disable_webcam_autofocus).
      - [Logitech C920](https://amzn.to/39M4vJH)
        - *-r 1920x1080 -f 30*
      - [UNZANO 1080P 60FPS](https://amzn.to/2MSTQnk)
        - *-r 1920x1080 -f 60*
        - For a generic camera, this works amazingly well!
- UPS Back Up
  - [APC 1500VA Sine Wave UPS](https://amzn.to/39MQXxm)
  - Who cares about print resume capabilities when you can just keep printing through the power outage?!

### Printhead
- Automatic Bed Leveling
- [Capricorn PTFE Tubing](https://amzn.to/3jgSn6D)
  - Useful as a reverse bowden tube even after Direct Drive conversion.
- Voron Afterburner
  - All materials are in the [official BOM](https://vorondesign.com/sourcing_guide), *Click the Voron Afterburner Tab at the bottom*
  - You will want to print the parts out of [ABS/ASA](https://amzn.to/3rhiRrm)
    - !!! Only print ABS in a well ventilated area
    - Use an enclosure to print, even if it's a cardboard box
  - Required Materials:
    - [BMG Extruder](https://amzn.to/3riyoXZ)
    - [Phaetus Dragon Hotend](https://amzn.to/3jmkGR5)
	- [Short Body Nema 17 Stepper](https://amzn.to/39IJrDM)

### Wiring
- [Cable Clips](https://www.thingiverse.com/thing:2676595) 
  - [https://www.thingiverse.com/thing:2676595](https://www.thingiverse.com/thing:2676595)
  - Good assortment of styles for wire management
- [Wire Loom Tubing](https://amzn.to/2YEpRm1)
  - 1/2 inch Cord Protector Wire Loom Tubing Cable Sleeve Split Sleeving
  - The stock loom is fine, but the split sleeve makes it much easier to change out wires
- Custom Wiring (*Nice to have for cable management and extensions*)
  - [24AWG Silicone Ribbon Cable](https://amzn.to/2YGWNdv)
    - For sensors, endstops, and Pi to SKR direct serial
    - Do NOT use for the hotend
  - [20AWG silicone Gauge Wire](https://amzn.to/3pQ0bi0)
    - For hotend and powering the Raspberry Pi
  - Connectors
    - [JST-XH](https://amzn.to/3pMmnK4) (*Connectors for the mainboard*)
    - [Dupont](https://amzn.to/2YJx3xg) (*Connectors for the Raspberry Pi GPIO Header*)

## Tools
A list of, at least what I found to be, indespensible tools.

- [Engineer PA-09 Crimping Pliers](https://amzn.to/2YKglO2) - *Best crimping tool available! Expensive, but well worth the money*
- [Paladin Tools PA1118 Wire Stripper](https://amzn.to/2MvSpLW) - *Excellent quality wire strippers*
- [TS80P Soldering Iron](https://amzn.to/3oSmwdO) - Great little soldering iron made even better with [IronOS](https://github.com/Ralim/IronOS)
- [Hex Key Allen Wrench Set with Ball End](https://amzn.to/2Mq3o9Q) - The set that comes with the Ender 3 is great, nice to have extras though
- [Nuts and Bolts](https://www.boltdepot.com/) - A collection of various M3 and M5 fasteners
- [Heatset Inserts](https://amzn.to/3jc1khy) - Mostly used with Voron parts

## Octoprint Plugins
All plugins are in the [OctoPrint Plugin Repository](https://plugins.octoprint.org/) and can be directly installed from the Octoprint Plugin Manager.

- Bed Visualizer
- Custom Background
- Filament Sensor Simplified
- OctoKlipper
- Octolapse
- PrintTimeGenius
- Printoid Notifications
- Resource Monitor
- Tab Order
- Themeify
- WS281x LED Status


## Costs
Probably shouldn't have done this, but since I looked up all the parts... Honestly, not as bad as I thought it would be.

| Ender 3 Mods                                         |  Cost                    | Qty |  Total        | Notes                   |
| ---------------------------------------------------- | ------------------------ | --- | ------------- | ----------------------- |
| Frame and Bed                                        |                          |     |               |                         |
| [WS2812 LEDs](https://amzn.to/2MPrvOU)               |  $                30.88  | 1   |  $    30.88   |                         |
| [MGN12H 300mm Linear Rails](https://amzn.to/2Mxf3DF) |  $                19.52  | 3   |  $    58.56   |                         |
| [Silicone Bed Springs](https://amzn.to/3tqtFW8)      |  $                11.99  | 1   |  $    11.99   |                         |
| [Spring Steel PEI Bed](https://amzn.to/3tojyB8)      |  $                26.59  | 1   |  $    26.59   |                         |
| [eSUN eBOX ](https://amzn.to/3tpDHH6)                |  $                72.99  | 1   |  $    72.99   |                         |
|                                                      |                          |     |  $   201.01   |                         |
|                                                      |                          |     |               |                         |
| Electronics                                          |                          |     |               |                         |
| [SKR 1.4 Turbo w/ TMC2209](https://amzn.to/3rhDa86)  |  $                62.99  | 1   |  $    62.99   |                         |
| [BTT 5V DCDC Board](https://amzn.to/3ro2oS7)         |  $                 9.98  | 1   |  $     9.98   |                         |
| [Raspberry Pi 4](https://amzn.to/3rhkuW4)            |  $                57.99  | 1   |  $    57.99   |                         |
| [Filament Runout Sensor](https://amzn.to/3pQ0rOi)    |  $                15.95  | 1   |  $    15.95   |                         |
| [UNZANO 1080P 60FPS](https://amzn.to/2MSTQnk)        |  $                59.95  | 1   |  $    59.95   |                         |
| [APC UPS\*](https://amzn.to/2X5bbvt)                 |  $               197.99  | 1   |  $   197.99   | \*Not included in total |
|                                                      |                          |     |  $   206.86   |                         |
|                                                      |                          |     |               |                         |
| Printhead                                            |                          |     |               |                         |
| [BMG Extruder](https://amzn.to/3riyoXZ)              |  $                24.99  | 1   |  $    24.99   |                         |
| [Short Body Nema 17 Stepper](https://amzn.to/39IJrDM)|  $                13.50  | 1   |  $    13.50   |                         |
| [Phaetus Dragon Hotend](https://amzn.to/3jmkGR5)     |  $                84.99  | 1   |  $    84.99   |                         |
| [BLTouch](https://amzn.to/3cCP48s)                   |  $                45.98  | 1   |  $    45.98   |                         |
|                                                      |                          |     |  $   155.96   |                         |
| TOTAL                                                |                          |     |  $   567.33   |                         |
