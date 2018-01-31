# This update is not yet available. You will receive an email when your model's firmware is ready to update.

# To update your firmware:

1. Backup machine's data. There is a small possibility that updating firmware can cause data loss.

### Intel Instructions for writing new firmware
User can update BIOS flash image via any of the follow methods...
*A. UEFI iFlash32* 
   1.  Boot the system to EFI Shell
   2.  Copy IFlash32.efi and BIOS .CAP file to a HD or USB Flash Drive
   3.  Map the respective storage device in system with the command
       Shell> map -r
   4.  Change the Shell to mapped device file system
       Example: Shell> fs0: (or fs1:)
   5.  Run the IFlash32 utility on the prompt
       fs0:\> IFlash32 [File Name] /u /ni
   6.  Reboot system after the update is completed.

*B. Use flash programmer to burn the new BIOS ROM image (16MB) into the flash chip.*

*C. Backup BIOS update instructions*
   1.  Boot the system to EFI Shell
   2.  Copy IFlash32.efi and BIOS .CAP file to a HD or USB Flash Drive
   3.  Map the respective storage device in system with the command
       Shell> map -r
   4.  Change the Shell to mapped device file system
       Example: Shell> fs0: (or fs1:)
   5.  Run the IFlash32 utility on the prompt
       fs0:\> IFlash32 [File Name] /u /ni UpdateBackupBios
   6.  It will update primary BIOS with processed capsule and the backup BIOS update will be completed in next normal boot.
   7.  Restart unit, Backup flash update done.
