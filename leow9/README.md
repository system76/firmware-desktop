# To update your firmware:

1. Backup your data. There is a small possibility that updating your firmware can cause data loss.

### Downloading and preparing new firmware
1. In order to update your firmware, you will need a flash drive. 
2. You will want to put the firmware.rom file on a MBR formatted FAT partitioned drive.
3. If you are familiar with the process for doing so, you can skip ahead to the [_Writing new firmware_](README.md#writing-new-firmware) section.
4. The following are instructions for properly formatting your flash drive and putting the new firmware on the drive.

### Preparing Flash Drive
1. Plug in your flash drive.
2. Open the "Disks" program.
4. The left panel of the "Disks" application shows all of the drives connected to your machine. Select the drive that represents your drive.
5. Select the menu button in the top right corner. Select "Format Disk".
6. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
7. Confirm this execution by selecting "Format".
8. Once this process is complete, you should see the volume listed as "Free Space".
9. Select the "+" button to create a partition for this drive.
10. Once again the default settings here should be sufficient. However, if you would like, you can add a name for the partition. In this example I named the drive "firmware" so I know what is on the drive when I plug it in.
11. Select "Create" when you are done supplying a name for the drive.
12. The drive should now be labeled with the name you gave the drive followed by the size and the letters FAT.
13. Now mount the drive by selecting the "Play" button.
14. Now that the drive is ready, download the `firmware.rom` file from here: [leow9 firmware](https://github.com/system76/firmware-desktop/blob/master/leow9/firmware.rom). Click `Download` to begin the download of the firmware.
15. Copy over the firmware file to the flash drive.

 
### Writing new firmware
1. After saving and backing up all of your work, make sure the flash drive with the updated firmware is plugged into your computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'Del' key.
4. After seeing the System76 logo, you should be brought to the Gigabyte BIOS.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**

![Initial BIOS screen](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/1.png)

5. Drag your mouse to the bottom right of the screen. You will see four options pop up from the bottom of the screen. Click on the "Q-Flash" option.

![QFlash Button](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/2.png)

6. Here you will have the option to "Update your BIOS" or "Save your BIOS". Select "Update your BIOS".

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/3.png)

7. Now you need to find and select the `firmware.rom` file that is on your flashdrive.
8. Towards the bottom left of the center panel, there will be a name of a device (perhaps an "Unknown Device") as well as a red triangle. 

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/4.png)

9. Select the red triangle to see a list of connected devices. Select the flashdrive you put the firmware on. See the image below, the second device "Generic (Part.-84541422 of 000...) is the flash drive I have the firmware on.

![Selecting correct flashdrive](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/5.png)

10. With the correct drive now selected, any folders would show up in the left panel, files in the right panel. Seeing that the firmware.rom file is the only file on the flashdrive, it shows immediately in the right panel.

11. Double-Click on the `firmware.rom` file.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/7.png)

12. You will now have the choice between a "FAST" or "INTACT" install. Click on the "INTACT" option.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/8.png)

13. Now the firmware on your machine is being updated. This should not take more than 5 minutes. You will see a progress bar showing the progress of writing the new firmware.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/9.png)

14. Once the firmware has been written, the screen will indicate that the system will reboot. Once the system reboots, remove the flash drive and you should be all good to go.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow9/images/10.png)

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, you may be brought to a yellow and black command line prompt titled: "EFI Shell version x". If this is the case, press the `ctrl`-`alt`-`del` keys all at once and your system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
