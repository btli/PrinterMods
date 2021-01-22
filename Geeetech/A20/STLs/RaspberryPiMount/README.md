# Raspberry Pi Mount for the Geeetech A20 Series Printers

## Required Materials
- [Raspberry Pi](https://amzn.to/3qHQjad) for Octoprint
- [XL4015 Buck Converter](https://amzn.to/2MgFLzK)
- 6x [M3 x 6mm socket head screws](https://amzn.to/35YzTSU)
- 4x [M2.5 x 6mm socket head screws](https://amzn.to/3qGnIlB)
- 1x [USB cable](https://amzn.to/2M7rm9b)
- [Silicone Wire](https://amzn.to/3iATvll)
- 1x [4-pin JST-XH connector](https://amzn.to/3iHLD1q)
- 2x [1-pin Dupont connector](https://amzn.to/3sO08oQ)
- 2x [Spade Connectors](https://amzn.to/2Y59fn7)
- Tools
  - [Soldering Iron](https://amzn.to/363Jacl) & [Solder](https://amzn.to/3iH0yZB)
  - [Multimeter](https://amzn.to/2NrXWmU)
  - [Engineer PA-09](https://amzn.to/3c017MJ) or [IWIS-2820M](https://amzn.to/3sOcKMX)
  - [Wire Crimper](https://amzn.to/3iDiN2e)

## Installation Procedure
1. Print the STL
2. Mount printed plate to unused standoffs using 4x M3 x 6mm screws.
3. Mount Raspberry Pi to plate using 4x M2.5 x 6mm screws.
4. Solder wires to input terminals of buck converter, optionally crimp spade connectors to wires.
5. Solder wires to output terminals of buck converter, crimp 1-pin Dupont connectors.
6. Connect spade terminals to PSU, make sure the Pi is not connected at this point, and power on the printer.
7. Using a multimeter, adjust buck converter output voltage to 5V
8. Turn off the printer and connect the dupont connectors +5V and GND of the Pi. Be very sure this is wired correctly and the voltage of the buck converter has been set properly, there is no polyfuse protection via the GPIO pins.
9. Cut and crimp a USB cable with a JST-XH connector, and connect it to the Pi and controller board.
10. Power on the printer, and done! You should see a /dev/ttyUSB0 which can be used by OctoPrint or Klipper.


Geeetech A20 A20M A20T
