# BirdNET-Pi
## Item List
1. Raspberry Pi 3 or higher
2. Power supply for Pi of choice
3. Thermal pads with heatsinks (for pi of choice)
4. Micro SD card (16gb or higher)
5. USB microphone
6. Internet connection (Using ethernet is recommended but you can also use the built in wireless)
7. Keyboard/Mouse/Display (With cables if needed)

## Flashing the operating system
1. Open Raspberry Pi imager (Download - https://www.raspberrypi.com/software/)
2. Select CHOOSE OS
3. Select RASPBERRY PI OS (64-bit)
4. Select CHOOSE STORAGE
5. Select your SD card from the menu
6. Optionally before the WRITING process click the settings menu to configure OS before flashing
7. Select WRITE and wait for flashing to finish
8. When prompted remover micro-SD card

## Prepping the Raspberry-Pi (Pre-Boot)
1. Install heatsinks
2. Place your Raspberry Pi in a position near a door/window with access to outside air and noise
3. Place mic outside next to window/door and run mic wire through window/door then plug mic into your Raspberry pi then plug in any other items such as ethernet
4. Ensure everything is plugged in
5. Power On

## Troubleshooting
Updates Failing - If your BirdNET-Pi updates are failing or not working try running this command = <code>chmod a+x ~/BirdNET-Pi/scripts/update_birdnet.sh</code>
