# To update firmware:

1. Backup machine's data. There is a small possibility that updating firmware can cause data loss.
2. Ensure AC stability. AC failure during update can cause damage to your system and be unrecoverable.

### Intel Instructions for updating BIOS
   
   1.  Extract the [zip file](https://github.com/system76/firmware-desktop/blob/master/jacv6/S1200SPO_BIOS_R03010026_.zip) to an HD or USB Flash Drive

         **_It is important that the drive is partitioned with FAT32_**
  
   2.  Boot the system to EFI Shell
   3.  Change the Shell to mapped device file system
          Example: Shell> fs0: (or fs1:)
   4.  Run `Startup.nsh` on the prompt.
   5.  Follow prompts to begin the update.
   6.  When asked to update the FRU or SDR, select `5` to `Exit FRU/SDR update`. 
   5.  Reboot system after the update is completed.
