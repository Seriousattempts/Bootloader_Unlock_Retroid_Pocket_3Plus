# Bootloader_Unlock_Retroid_Pocket_3Plus
Bootloader unlock using CVE-2022-38694 for Retroid Pocket 3+

The bootloader unlock is required before flashing any custom firmware or custom fixes like:
- [Batocera Odroid M1](https://batocera.org/download)
- [GammaOS](https://github.com/TheGammaSqueeze/GammaOS)
- [GammaOS RK3566](https://github.com/TheGammaSqueeze/GammaOS-RK3566)
- [ROCKNIX x55 |SAFE|](https://rocknix.org/devices/powkiddy/x55/)
- [RK3588 |PS2/Wii Emulation|RISKY|](https://rocknix.org/contribute/build/#option-1-clean-the-package-that-failed)



#Warning:

*I did this late at night with no sleep and after I stopped recording, going based off of lack of energy memory. I apologize ahead of time*

Proceed at your own risk. 
Unlocking the bootloader will void your warranty and can potentially damage your device. I am not responsible for any damage to your device or any data loss incurred.
Only supported on Windows systems.
Important Notices:

Data Erasure: Unlocking the bootloader will erase all data on your device. Your device will be factory reset to its original state.
Unlock Warning: After unlocking, an unlock warning message will appear on the screen every time you boot your device. This is normal and cannot be removed.

*Prerequisites:*
- Unlocking Procedure (Attempt 1):
- Unisoc USB Drivers: Install the Unisoc USB drivers located in the [UnisocDrivers folder](https://github.com/TheGammaSqueeze/GammaOS/blob/main/UnisocDrivers.zip)
- ums512_alldocube_iplay_50_EN_20230801 from [https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader/releases/tag/1.72](https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader/releases/tag/1.72)
- [ADB (Platform Tools)](https://developer.android.com/tools/releases/platform-tools) (maybe, I really don't remember but I put it in the extracted ums512_alldocube_iplay_50_EN_20230801 folder and I always go to the adb folder when using it
- Enabled developer options on Rp3+ (Go to Settings → About Phone, Tap Build Number 7 times. Then back to Settings → System, Advanced, Developer options. **Enable USB Debugging and OEM Unlock in Developer Options**

# Video version:
[![Unlock bootloader in RP3+](https://i.ytimg.com)](https://www.youtube.com/ "Unlock bootloader in RP3+")

1. Install Unisoc driver, extract adb to the extracted ums512_alldocube_iplay_50_EN_20230801 folder
2. Put RP3+ into Android Recovery (Turn off, turn on while holding power along with volume buttons)
3. Run *unlock_autopatch_512.bat* from computer, and then enter fastboot on RP3+
4. Follow unlock_autopatch_512 instructions, profit I think.

Note, if that doesn't work
5. Restart device back to recovery mode, go to "Apply update from ADB" and restart running *unlock_autopatch_512.bat* from computer
6. If that doesn't work:
- Restart RP3+ to normal use
- Open cmd from file explorer folder of "ums512_alldocube_iplay_50_EN_20230801"
- Run the following:
6.1. adb devices
6.2. 
adb push fdl1-dl.bin /data/local/tmp/
adb push fdl2-dl.bin /data/local/tmp/
6.3. unlock_autopatch_512



Unlocking Procedure (Attempt 2, never attempted, taken from [https://github.com/TheGammaSqueeze/Bootloader_Unlock_Anbernic_T820](https://github.com/TheGammaSqueeze/Bootloader_Unlock_Anbernic_T820)):
Shut Down Device: Ensure your device is completely shut down with no USB cable attached.
Run Unlock Script: Open the unlock_autopatch_512.bat script on your computer.
Connect Device:

Within 30 seconds of running the script, hold down the HOME/BACK button on the turned-off unit.
While holding the button, plug in the USB cable to your device.
Continue Unlock Process: The unlock script will now proceed. You can release any buttons once the script is running.
Wipe data: Your unit will now reboot. It will likely show the battery charging screen, in this case just turn on the device. Upon the second reboot you will be asked to wipe your device. Use the volume buttons to navigate to the wipe option, use the power button to confirm this option. Your unlock is now complete.


**By following this guide, you acknowledge that you understand the risks involved in unlocking your device's bootloader. Ensure you have backed up all important data before proceeding.**
