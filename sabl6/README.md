# To update your firmware:

1. Backup all data. There is a small possibility that updating firmware can cause data loss.

### Downloading and preparing new firmware
1. Updating firmware requires a flash drive at least 2 GB in size.
2. The firmware.cap file needs to be placed on a thumbdrive with MBR FAT32 formatting.
3. Feel free to skip ahead to the later sections if this is familiar ground.
4. To properly format a flash drive, follow the next instructions:

### Preparing Flash Drive
1. Plug in the flash drive.
2. Open the "Disks" program.
3. The left panel of the "Disks" application shows all of the drives connected to your machine. Select the flash drive.
4. Select the menu button in the top right corner. Select "Format Disk".
5. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
6. Confirm the execution by selecting "Format".
7. Once this process is complete, the volume should be listed as "Free Space".
8. Select the "+" button to create a partition for this drive.
9. The default settings should be sufficient. A name for the partition can be added to help identify the use of the drive.
10. Select "Create". The drive should be labeled with the name(if any) as well as the size and the parition type, FAT.
11. Mount the drive by selecting the "Play" button.
12. When the drive is ready, download the `firmware.cap` file from here: [sabl6 firmware](https://github.com/system76/firmware-desktop/blob/master/sabl6/firmware.cap). Click `Download` to begin the download.

13. The sha512sum checksum for this download is:
```d0c3782f1ef97ab7eccc33bbe36fb54f9e3249262b8fc74d3bdab894154f42ae30117a22537cf671f4cc593d8514cb8608eabb94df7fd9bb82ce403d7242b439```. 

    Confirm that the download has the same checksum by executing the following command in the firmware.cap directory:

    `sha512sum -b firmware.cap`

14. Copy over the firmware file to the flash drive.

### Writing new firmware
1. After saving and backing up all of your work, make sure the flash drive with the updated firmware is plugged into your computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'Del' key.
4. After seeing the System76 logo, you should be brought to the ASUS BIOS.

5. The BIOS should look similar to the following screenshot. Select the "Advanced Mode" at the bottom right of the screen (or press `F7`).

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**
![ASUS UEFI BIOS Utility - EZ Mode](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/1.png)

6. Towards the top of the screen, select the "Tool" tab.

![ASUS UEFI BIOS Utility - Tool Tab](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/2.png)

7. Select the top option, "ASUS EZ Flash 3 Utility".

8. Now you will be prompted to choose to update via Storage device or via the Internet. Select "via Storage Device" and press "Next".

![ASUS UEFI BIOS Utility - Update method](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/3.png)

9. You will now be prompted with a file manager. Select the correct Drive and move through the files and folders on the flash drive (using arrow keys and the "Enter" key) to select the `firmware.cap` file.

![ASUS UEFI BIOS Utility - Select Firmware](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/4.png)

10. You will then be prompted twice to confirm that the file you selected will be read and used to update the firmware/BIOS.

11. The update will then commence with a progress bar at the bottom of the screen.

12. When the update completes a prompt will appear saying the system will reboot.

13. Once the system reboots, an American Megatrends screen will appear. Press F1. You will be brought back into the BIOS. Press F10 to save and exit the BIOS. The computer will restart once again this time into your operating system. The firmware updating process is now complete.

14. To confirm the update was successful, check in either the BIOS or using `dmidecode` that the BIOS verison is: `3405`. The ME version is `11.6.10.1196`.

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, you may be brought to a yellow and black command line prompt titled: "EFI Shell version x". If this is the case, press the `ctrl`-`alt`-`del` keys all at once and your system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
