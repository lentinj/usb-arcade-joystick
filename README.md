# USB Arcade Joystick using a Minimus 32

This repository contains the source code for my joystick described here:

https://jamie.lentin.co.uk/embedded/arcade-joystick/

This is basically the LUFA Joystick demo, but with alterations to:

* Use custom joystick/button interfaces, rather than rely on board drivers
* Debounce buttons
* Use 8 buttons instead of 2

## Building and installing

Clone the code and make sure LUFA is downloaded with:

    git submodule update --init

Then edit ``makefile`` to suit your board. This is a standard LUFA makefile,
``MCU``, ``ARCH``, ``BOARD`` and ``F_CPU`` are particular values to pay
attention to.

To build and flash to an attached chip in DFU mode (for a minmus, hold down HWB
after reset):

     make && make dfu
