# To update your firmware:

1. Backup all data. There is a small possibility that updating firmware can cause data loss.

### Downloading and preparing new firmware
1. Updating firmware requires a flash drive at least 2 GB in size.
2. The firmware.rom file needs to be placed on a thumbdrive with MBR FAT32 formatting.
3. Feel free to skip ahead to the later sections if this is familiar ground.
4. To properly format a flash drive, follow the next instructions:

### Preparing Flash Drive
1. Plug in the flash drive.
2. Open the "Disks" program.
3. The left panel of the "Disks" application shows all of the drives connected to the machine. Select the flash drive.
4. Select the menu button in the top right corner. Select "Format Disk".
5. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
6. Confirm the execution by selecting "Format".
7. Once this process is complete, the volume should be listed as "Free Space".
8. Select the "+" button to create a partition for this drive.
9. The default settings should be sufficient. A name for the partition can be added to help identify the use of the drive.
10. Select "Create". The drive should be labeled with the name(if any) as well as the size and the parition type, FAT.
11. Mount the drive by selecting the "Play" button.
12. When the drive is ready, download the `firmware.rom` file from here: [wilp12 firmware](https://github.com/system76/firmware-desktop/blob/master/wilp12/firmware.rom). Click `Download` to begin the download.

13. The sha512sum checksum for this download is:
```d9e7b59727de9699aa8149e9839c08dd3bf505143442c059edb1cbbdf3eedc3c7c342529825b773a5c8087ce40cceae9b67dfd27893caa37a919fb4bf3d89a95```. 

    Confirm that the download has the same checksum by executing the following command in the firmware.rom directory:

     `sha512sum -b firmware.rom`

14. Copy over the firmware file to the flash drive.

### Writing new firmware
1. After saving and backing up the machine, make sure the flash drive with the updated firmware is plugged into the computer.
2. Power off the machine.
3. Power back on the machine. As the machine is powering back up, hold down the 'Del' key.
4. After the System76 logo is shown, the Gigabyte BIOS will appear. It should look similar to the following image.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**
![GIGABYTE UEFI BIOS Utility](https://raw.githubusercontent.com/system76/firmware-desktop/master/wilp12/images/1.png)

5. Press `F8` to start the QFlash utility.

6. Select `Update BIOS from Drive`.
7. Select the flash drive with the firmware on it.
8. Select the `firmware.rom` file.
9. The QFlash will take a couple of seconds to read the file. A pop-up will then appear listing the information associated with this firmware update. Confirm that the following is going to be installed.

```
Model Name: H170-D3HP

BIOS Version: F20e??

BIOS date: 01/19/2018

Checksum: 7AF3
```
*Note*: The System76 team has thoroughly tested this BIOS and confirmed it is not corrupted.

10. Select "Normal Update". The update process will then begin. This may take up to 5 minutes.
11. When the update process is complete, the system will reboot. The update process is now complete.

**Note:**
After the firmware update completes, if the system reboots with the flashdrive still plugged in, you may be brought to a yellow and black command line prompt titled: "EFI Shell version x". If this is the case, press the `ctrl`-`alt`-`del` keys all at once and your system will restart. Promptly remove the flashdrive and your system will reboot into your operating system.
