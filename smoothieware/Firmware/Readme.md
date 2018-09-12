# Step by step
## Download
  Download Firmware-xxxxxxxx.bin 
## Copy
  Rename Firmware-xxxxxxxx.bin to firmware.bin
  Copy the file firmware.bin to a micro sdcard, then safely remove the sdcard from your computer

## Filename
  Make sure the file is named firmware.bin, and not anything else.
  Also make sure you downloaded the file itself, and not the HTML page containing it, as this would cause chaos. A good method is to check the MD5 sum for the file you downloaded ( or opening it in a web browser ).
Make sure you eject the SD card from your computer properly ( “eject” in your file explorer's menus ).

## Power
  Plug the sdcard into the AZSMZ Mini sdcard slot, then plug a mini USB cable into the board

## Observe
  AZSMZ Mini will boot and you should see the leds count up for a few seconds, then they will start flashing, at this point has flashed the latest version of Smoothieware and is running.

## SD card problems
 If there is a problem with the SD card, LED4 will be off.
 If this happens, you need to format the SD card (can use mobile or camera), and if that fails, use another SD card.

 You can make sure the new firmware was flashed by looking at the content of the SD card.

 If the firmware was flashed successfully, the filename should have changed to FIRMWARE.CUR

## Connect
You can now connect to AZSMZ Mini with Pronterface ( or any other host program, see Software ) at any baud rate, look for a serial USB device on your computer.

If running windows you may need to install the Windows Drivers
Mac OS/X and Linux have the drivers built in.
You can ignore any messages about missing DFU drivers.

## Terminal
You can also connect to AZSMZ Mini with any serial console program, which should be set to local echo and Linefeed line endings.

Typing help will show a list of console commands available.

Some useful commands are:-

version - which shows the current smoothie version
ls /sd - which lists the files on the sdcard
play /sd/file - which will print the file from the sdcard
More commands can be found on the Console commands list and useful G-codes are in the Supported G-codes list
