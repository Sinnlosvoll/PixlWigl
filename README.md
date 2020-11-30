# PixlWigl

Tired of moving your mouse manually to keep your pc awake? Oh boy, do I have the solution for YOU!

Just plug the finished device into a USB-A port and watch your mouse dance in a square of 3 pixels, keeping your screensaver or any other activity detections at bay.

# Make your own

## Hardware
 - Two USBasps (with at least one cable)
 - something tweezer like

## Software

### Mac
 - brew install avrdude 
 - brew tap osx-cross/avr
 - brew install avr-gcc avr-binutils

### Linux
 - pacman -S avrdude avr-gcc

### Windows
 - choco install avrdude
 - and somehow avr-gcc
   - make sure they are in the path when executing the build/flash commands.




## Compiling
Simply execute
```bash
make build
```
and if all prerequisite software was installed.
## Flashing
Connect both USBasps together via the ribbon cable, and plug in the one, that shall not be the PixlWigl in the future.
Bridge the JP2 pins together with anything metallic, like a pair of tweezers.
Holding the JP2 bridged, execute the following command:
```
sudo make flash
```
The USBasp with the bridged JP2 is now configured to be a PixlWigl, and can be plugged into any device that accepts USB HID mice:

BSD, Linux, Mac, Windows, Android, QNX, FreeDos, the world is your oyster now.

# Credits
This is a modified version of a project from Joonas Pihlajamaa, that can be found at http://codeandlife.com/2012/02/11/v-usb-tutorial-continued-hid-mouse/

# License
For all parts that do not belong to other licenses, the default License is GPLv3.
