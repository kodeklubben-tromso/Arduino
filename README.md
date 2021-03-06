# Arduino Laser Tag
Library and sketch code for an Arduino-based Laser Tag game.

The code is part of a cooperation project between [Kodeklubben Tromsø](https://kodeklubben-tromso.github.io/) (Tromsø Code Club) and [Nordnorsk Vitensenter](https://nordnorsk.vitensenter.no/) (Northern Norwegian Science Museum) called *Skills Makerlab.* The *Makerlab* is a free evening activity for kids between 13-19 years.

![Complete kit](img/completekit.jpg)


### Hardware
All hardware is based on the Arduino Microcontroller. Each set uses an Arduino Nano (Lasergun) and an Arduino Uno (Laservest). In addition to several components, the kits also use custom PCBs to reduce the number of wires and remove the need for breadboards. The complete setup will be made available through an instructional manual, with component requirements, schematics for PCBs and soldering, .

### Software
Software is provided as is, the latest version has not been tested with a complete kit yet, but it does compile for the Arduino boards.

### Limitations

- Range of the IR leds are limited to about 30-40 meters.
- The Neopixel Library does cause some intereference with the IR library due to disabling interrupts.
- The response flash of the Laser Vest has a low range, and will probably be reworked to use a radio signal instead.

## Version 1.0
Version 1.0 have been developed during the last *Makerlab* courses.

### Core Features
**Laser Gun**

- Sending an IR signal by the use of a Single IR LED.
- The IR signal contains a 32-bit number which contains:
	- Command field
	- Player ID
	- Team ID
	- Checksum
- A laser marker, visual only.
- Trigger debouncing.

![Laser gun](img/gun.jpg)

**Laser Vest**

- IR receivers that reads the 32-bit gun signal and register hits.
- Disabling of the gun if the player gets tagged by a player from the other team.
- Responding to being tagged by another player by flashing a message back.
- Neopixel team color markers.

![Laser Vest](img/vest.jpg)

## Version 2.0
Version 2.0 is currently under development, some of the planned features are:

- LCD display attached to the gun (can be see in picture) for displaying score, team and other information.
- Solenoid recoil simulator.
- MP3 player and speaker.
- New battery and power supply system.
- Magazine.

## Contributors
The main contributors to the project are:

- Hedinn Gunhildrud - hedinn@nordnorsk.vitensenter.no
- Morten Grønnesby - morten.gronnesby@uit.no 


# Third Party Libraries
The library uses some third party libraries:

- [IRremote library](https://github.com/z3t0/Arduino-IRremote) by **Ken Shirrif**

- [Adafruit Neopixel Library](https://github.com/adafruit/Adafruit_NeoPixel) by **Adafruit**


