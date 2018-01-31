# This update is not yet available. You will receive an email when your model's firmware is ready to update.

# To update firmware:

1. Backup machine's data. There is a small possibility that updating firmware can cause data loss.
2. Ensure AC stability. AC failure during update can cause damage to your system and be unrecoverable.

### Intel Instructions for updating BIOS
   
   1.  Extract the [zip file](https://github.com/system76/firmware-desktop/blob/master/jacv6/S1200SPO_BIOS_R03010026_.zip) to a 
   HD or USB Flash Drive

         **It is important that the drive is partitioned with FAT32**
  
   2.  Boot the system to EFI Shell
   3.  Map the respective storage device in system with the command
          `Shell> map -r`
   4.  Change the Shell to mapped device file system
          Example: Shell> fs0: (or fs1:)
   5.  Run `Startup.nsh` on the prompt
   6.  Reboot system after the update is completed.
