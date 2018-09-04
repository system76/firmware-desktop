# To update your firmware:

1. Backup all data. There is a small possibility that updating firmware can cause data loss.

### Downloading and preparing new firmware
1. In order to update firmware, a flash drive is needed. 
2. Put the firmware.rom and fpt.efi file on a MBR formatted FAT partitioned drive.
3. If you are familiar with the process for doing so, you can skip ahead to the [_Writing new firmware_](README.md#writing-new-firmware) section.
4. The following are instructions for properly formatting the flash drive and putting the new firmware on the drive.

### Preparing Flash Drive
1. Plug in your flash drive.
2. Open the "Disks" program.
4. The left panel of the "Disks" application shows all of the drives connected to your machine. Select the drive that represents your drive.
5. Select the menu button in the top right corner. Select "Format Disk".
6. A pop-up will appear asking how the drive should be formatted. The defaults are desired so select "Format...".
7. Confirm this execution by selecting "Format".
8. Once this process is complete, you should see the volume listed as "Free Space".
9. Select the "+" button to create a partition for this drive.
10. Once again the default settings here should be sufficient. However, you do need to add a name for the flash drive. In this example I named the drive "firmware" so I know what is on the drive when I plug it in. You can name the drive whatever you would like.
11. Select "Create" when you are done supplying a name for the drive.
12. The drive should now be labeled with the name you gave the drive followed by the size and the letters FAT.
13. Now mount the drive by selecting the "Play" button.
14. Now that the drive is ready, download the `firmware.rom` and `fpt.efi` files from here: [leow9-w firmware](firmware.rom), [leow9-w fpt.efi](fpt.efi).
15. Copy over the files to the flash drive.

 
### Writing new firmware
1. After saving and backing up all work, make sure the flash drive with the updated firmware is plugged into the computer.
2. Power off the machine. Unplug the machine.
3. Take the side glass panel off, so that access to the motherboard is available.
4. At the bottom of the board, there is a jumper that needs to be moved from covering 1-2 to 2-3. See the below image where the pins proceed numerically 1,2,3.
![ME Update Jumper](https://raw.githubusercontent.com/system76/firmware-desktop/leow9-w_fix/leow9-w/images/1.png)

4. Power back on the machine. As the machine is powering back up, hold down the 'F12' key.
5. After the System76 logo appears, a list of bootable devices will be displayed.
6. Select `UEFI: Built-in EFI Shell`.
7. A command line will appear with a list of devices connected to the machine.
8. Find the usb device with the firmware on it. It should be the only device labeled "Removable". The name should be `fs0:`, `fs1:` or something similar.
9. Type in the appropriate drive from above (ex. `fs0:`) and press `Enter`.
10. Use the `ls` command to confirm the `firmware.rom` and `fpt.efi` files are present.
11. Type in the command: `fpt -f firmware.rom`. Press `Enter`.
12. When the upgrade is complete (The `Shell> _` line is the last line on the screen), type `reset -s` and press `Enter`. 
13. Unplug the power cord from the power supply for 10 seconds, afterwards plug the power cord back in.
14. Move the jumper back to 1-2 position (normal position). Power the machine back on. The machine may restart a few times. To confirm the update was successful, press the `Delete` key to enter the BIOS on boot.

**NOTE: Some information in the screenshots below may differ from that of your actual machine.**
