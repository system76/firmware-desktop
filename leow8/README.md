# To update your firmware:

1. Backup all data. There is a small possibility that updating firmware can cause data loss.

### Downloading and preparing new firmware
1. Updating firmware requires a flash drive at least 2 GB in size.
2. The firmware.rom file needs placed on a thumbdrive with a MBR FAT32 formatting
3. Feel free to skip ahead to the later sections if this is familiar ground.
4. To properly format a flash drive, follow the next instructions:

### Preparing Flash Drive
1. Plug in the flash drive.
2. Open the "Disks" program.
3. The left pannel of the "Disks" application shows all of the drives connected to your machine. Select the flash drive.
4. Select the menu button in the top right corner. Select "Format Disk".
5. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
6. Confirm the execution by selecting "Format".
7. Once this process is complete, the volume should be listed as "Free Space".
8. Select the "+" button to create a partition for this drive.
9. The default settings should be sufficient. A name for the partition can be added to help identify the use of the drive.
10. Select "Create". The drive should be labeled with the name(if any) as well as the size and the parition type, FAT.
11. Mount the drive by selecting the "Play" button.
12. When the drive is ready, download the `firmware.rom` file from here: [leow8 firmware](https://github.com/system76/firmware-desktop/blob/master/leow8/firmware.rom). Click `Download` to begin the download of the firmware.

13. The sha512sum checksum for this download is:
    ```b1d68c4dd368a0a913dbf11a6e2b2e6ba3b2e3dbfb47c7c3bff0b6657e9fd7453d387d29e478aa67c605a63a98001accf7bec1fc7cc07a3eb7cb92722278461b```.

    Confirm that the download has the same checksum by executing the following command in the fimrware.rom directory:

     `sha512sum -b firmware.rom`

14. Copy over the firmware file to the flash drive.

 
### Writing new firmware
1. After saving and backing up the machine, make sure the flash drive with the updated firmware is plugged into the computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'Del' key.
4. After seeing the System76 logo, the Gigabyte BIOS will appear.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**

![Initial BIOS screen](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/1.png)

5. Move the mouse to the bottom right of the screen. Four options will pop up from the bottom of the screen. Click on the "Q-Flash" option.

![QFlash Button](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/2.png)

6. Select "Update your BIOS".

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/3.png)

7. Find and select the `firmware.rom` file that is on the flashdrive.
8. Towards the bottom left of the center pannel, there will be a name of a device (perhaps an "Unknown Device") as well as a red triangle. 

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/4.png)

9. Select the red triangle to see a list of connected devices. Select the appropriate flashdrive the firmware is on. See the image below, the second device "Generic (Part.-84541422 of 000...) is the flash drive in this example.

![Selecting correct flashdrive](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/5.png)

10. With the correct drive now selected, any folders would show up in the left pannel, files in the right pannel. Seeing that the firmware.rom file is the only file on the flashdrive, it shows immediately in the right pannel.

11. Double-Click on the `firmware.rom` file.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/7.png)

12. With the choice between a "FAST" or "INTACT" install, select the "INTACT" option.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/8.png)

13. Now the firmware on the machine is being updated. This should not take more than 5 minutes. A progress bar showing the progress of writing the new firmware will appear.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/9.png)

14. Once the firmware has been written, the screen will indicate that the system will reboot. Once the system reboots, remove the flash drive. The firmware should now be up-to-date.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/10.png)

15. To confirm the update was successful, check in either the BIOS or using `dmidecode` that the BIOS verison is: `F8b Z5`.

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, you may be brought to a yellow and black command line prompt titled: "EFI Shell version x". If this is the case, press the `ctrl`-`alt`-`del` keys all at once and your system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
