# This update is not yet available. You will receive an email when your model's firmware is ready to update.

# To update your firmware:

1. Backup all data. There is a small possibility that updating firmware can cause data loss.

### Downloading and preparing new firmware
1. Updating firmware requires a flash drive at least 2 GB in size.
2. The firmware.cap file needs placed on a thumbdrive with a MBR FAT32 formatting
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
12. Now that the drive is ready, download the `firmware.rom` file from here: [wilp13 firmware](https://github.com/system76/firmware-desktop/blob/master/wilp12/firmware.rom). Click `Download` to begin the download of the firmware.

13. The sha512sum checksum for this download is `*redacted*`. Confirm that the download has the same checksum by executing the following command in the firmware.rom directory. `sha512sum -b firmware.rom`

15. Copy over the firmware file to the flash drive.

### Writing new firmware
1. After saving and backing up the machine, make sure the flash drive with the updated firmware is plugged into the computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'END' key.
4. After the System76 logo appears, the Q-Flash application will launch.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/3.png)

5. Select `Update BIOS`.
6. The next screen is to select the file to be flashed. 

![Initial File Selection](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/4.png)

7. If the `firmware.rom` file is listed on the righ pannel, use the arrow keys to select the file. Press `Enter` to confirm this selection.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/7.png)

  - Towards the bottom left of the center pannel, there will be a name of a device (perhaps an "Unknown Device") as well as a red triangle. Selecting the triangle will provide a dropdown menu of other devices connected to the computer. If the flashdrive with the firmware file is not the currently selected drive, select the proper drive. Use the arrow keys to browse the flash drive for the `firmware.rom` file. When the file appears in the right pannel, Press `Enter` to select the file.

![Selecting correct flashdrive](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/5.png)

8. The next page will ask between a "FAST" or "INTACT" install. In order to update the ME, select the "INTACT" option.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/8.png)

9. The firmware is now being updated. This should not take more than 5 minutes. You will see a progress bar showing the progress of writing the new firmware.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/9.png)

10. Once the firmware has been written, the screen will indicate that the system will reboot. When the system begins the reboot cycle, remove the flash drive. The firmware should now be up-to-date.

![Selecting firmware.rom](https://raw.githubusercontent.com/system76/firmware-desktop/master/leow8/images/10.png)

11. To confirm the update was successful, check in either the BIOS or using `dmidecode` that the BIOS verison is: `F9b`. 

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, a yellow and black command line prompt titled: "EFI Shell version x" may appear. If this is the case, press the `ctrl`-`alt`-`del` keys all at once and the system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
