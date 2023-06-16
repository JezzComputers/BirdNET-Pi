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
1. Open Raspberry Pi imager (Download - https://www.raspberrypi.com/software)
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
5. Power on when ready

## First Boot
1. Ensure all cables are plugged and then LASTLY the power cable to Raspberry Pi
2. Don't touch your pi until the next step is done
3. After your pi has restarted (As many times as it needs to) you will see a setup wizard or if you used the settings menu, you would see the desktop
4. The setup wizard:

![Setup Wizard](https://github.com/JezzComputers/BirdNET-Pi/assets/129046176/bbcddef9-2dce-48be-a8f4-b7fa6aac09e9)

6. The GUI Desktop:

![Desktop](https://github.com/JezzComputers/BirdNET-Pi/assets/129046176/d7bd8a91-d461-4644-a1e4-d2dbac4db6cf)

7. Follow the setup wizard to complete installation (Skip this step if you were taken to the desktop)
8. If prompted, follow further instructions to finish setting up your Raspberry Pi
9. Open the Raspberry Pi menu then select Preferences then Raspberry pi configuration

![Pi-config](https://github.com/JezzComputers/BirdNET-Pi/assets/129046176/1370a769-f7ba-4dd2-9396-f23a2c702f56)

10. Go through the individual tabs changing any settings to suit your needs
11. Change the default username, password, and the hostname to ones you will remember. Also change the Wi-Fi settings to the ones matching your area
12. In the interface tab leave all off except for SSH and VNC because they will be used for communicating with the Raspberry Pi wirelessly

## Recommended Additions
**Software Removal**
1. Click the Raspberry Pi menu then click Preferences then Recommended Software

![Pi-rec-software](https://github.com/JezzComputers/BirdNET-Pi/assets/129046176/7ef131c7-e6d2-4f22-95be-b037b28196c2)

3. Scroll down unchecking all of the software that you don't want
4. Then click apply (bottom right corner of screen)

**TeamViewer Install**

To directly download, run this script in the Raspberry Pi terminal; <code>wget https://download.teamviewer.com/download/linux/teamviewer_arm64.deb</code>
To download follow these steps:
1. Navigate to your preferred web browser
2. Paste this link into the search bar: https://www.teamviewer.com/en-us/download/raspberry-pi
3. You should see a page like this:

![image](https://github.com/JezzComputers/BirdNET-Pi/assets/129046176/f97cd7da-042c-41e9-8e09-f7b14be22a9c)

4. select <code>x86-64bit</code>
5. Once it has finished downloading transfer the file to your Raspberry Pi
6. On your Raspberry Pi run the TeamViewer installer then do as prompted
From the terminal
1. Go to the folder/directory with the TeamViewer installer in it
2. Run this command: <code>sudo dpkg -i teamviewer_15.42.4_arm64.deb</code> (IMPORTAINT change the 15.42.4 to whatever version you have)

**NodeRED Install + Run on boot**

Run this script in the Raspberry Pi terminal; <code>bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)</code>
To enable AutoStart on boot run this script; <code>sudo systemctl enable nodered.service</code>

## Troubleshooting
Updates Failing - If your BirdNET-Pi updates are failing or not working try running this command <code>chmod a+x ~/BirdNET-Pi/scripts/update_birdnet.sh</code>
