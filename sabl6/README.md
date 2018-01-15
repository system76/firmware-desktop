# To update your firmware:

1. Backup your data. There is a small possibility that updating your firmware can cause data loss.

### Downloading and preparing new firmware
1. In order to update your firmware, you will need a flash drive.
2. You will want to put the firmware.rom file on a MBR formatted FAT partitioned drive.
3. If you are familiar with the process for doing so, you can skip ahead to the _Writing new firmware_ section.
4. The following are instructions for properly formatting your flash drive and putting the new firmware on the drive.

### Preparing Flash Drive
1. Plug in your flash drive.
2. Open the "Disks" program.
4. The left pannel of the "Disks" application shows all of the drives connected to your machine. Select the drive that represents your drive.
5. Select the menu button in the top right corner. Select "Format Disk".
6. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
7. Confirm this execution by selecting "Format".
8. Once this process is complete, you should see the volume listed as "Free Space".
9. Select the "+" button to create a partition for this drive.
10. Once again the default settings here should be sufficient. However, if you would like, you can add a name for the partition. In this example I named the drive "firmware" so I know what is on the drive when I plug it in.
11. Select "Create" when you are done supplying a name for the drive.
12. The drive should now be labeled with the name you gave the drive followed by the size and the letters FAT.
13. Now mount the drive by selecting the "Play" button.
14. Now that the drive is ready, download the `firmware.rom` file from here: [sabl6 firmware](https://github.com/system76/firmware-desktop/blob/master/sabl6/firmware.rom). Click `Download` to begin the download of the firmware.
15. Copy over the firmware file to the flash drive.


### Writing new firmware
1. After saving and backing up all of your work, make sure the flash drive with the updated firmware is plugged into your computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'Del' key.
4. After seeing the System76 logo, you should be brought to the ASUS BIOS.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**

5. The BIOS should look similar to the following screenshot. Select the "Advanced Mode" at the bottom right of the screen (or press `F7`).

![ASUS UEFI BIOS Utility - EZ Mode](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/1.png)

6. Towards the top of the screen, select the "Tool" tab.

![ASUS UEFI BIOS Utility - Tool Tab](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/2.png)

7. Select the top option, "ASUS EZ Flash 3 Utility".

8. Now you will be prompted to choose to update via Storage device or via the Internet. Select "via Storage Device" and press "Next".

![ASUS UEFI BIOS Utility - Update method](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/3.png)

9. You will now be prompted with a file manager. Select the correct Drive and move through the files and folders on the flash drive (using arrow keys and the "Enter" key) to select the firmware.CAP file.

![ASUS UEFI BIOS Utility - Select Firmware](https://raw.githubusercontent.com/system76/firmware-desktop/master/sabl6/images/4.png)

10. You will then be prompted twice to confirm that the file you selected will be read and used to update the firmware/BIOS.

11. The update will then commence with a progress bar at the bottom of the screen.

12. When the update completes a prompt will appear saying the system will reboot.

13. Once the system reboots, an American Megatrends screen will appear. Press F1. You will be brought back into the BIOS. Press F10 to save and exit the BIOS. The computer will restart once again this time into your operating system. The firmware updating process is now complete.

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, you may be brought to a yellow and black command line prompt titled: "EFI Shell version x". If this is the case, press the `ctrl`-`alt`-`del` keys all at once and your system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
