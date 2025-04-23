# Bootloader_Unlock_Retroid_Pocket_3Plus
Bootloader unlock using CVE-2022-38694 for Retroid Pocket 3+
**By following this guide, you acknowledge that you understand the risks involved in unlocking your device's bootloader. Ensure you have backed up all important data before proceeding. Credits: This bootloader unlocking process is based on the work from the following repository: TomKing062/CVE-2022-38694_unlock_bootloader.**

The bootloader unlock is required before flashing any custom firmware or custom fixes like
- ~~[GammaOS](https://github.com/TheGammaSqueeze/GammaOS)~~ Device doesn't install GammaOS


## Warning for video proof:
*I did this late at night with no sleep and after I stopped recording, going based off of lack of energy memory. I apologize ahead of time*

# Video version:
[![How to unlock Retroid Pocket 3+ UNISOC T618 bootloader](https://i.ytimg.com/vi_webp/0o8FVecnDrY/maxresdefault.webp)](https://www.youtube.com/watch?v=0o8FVecnDrY) "How to unlock Retroid Pocket 3+ UNISOC T618 bootloader")

Proceed at your own risk. 
Unlocking the bootloader will void your warranty and can potentially damage your device. I am not responsible for any damage to your device or any data loss incurred.

Only attempted on Windows systems.
Important Notices:

Data Erasure: Unlocking the bootloader will erase all data on your device. Your device will be factory reset to its original state.
Unlock Warning: After unlocking, an unlock warning message will appear on the screen every time you boot your device. This is normal and cannot be removed.

# *Prerequisites:*
- Unlocking Procedure (Attempt 1):
- Unisoc USB Drivers: Install the Unisoc USB drivers located in the [UnisocDrivers folder](https://github.com/TheGammaSqueeze/GammaOS/blob/main/UnisocDrivers.zip)
- ums512_alldocube_iplay_50_EN_20230801 from [https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader/releases/tag/1.72](https://github.com/TomKing062/CVE-2022-38694_unlock_bootloader/releases/tag/1.72)
- [ADB (Platform Tools)](https://developer.android.com/tools/releases/platform-tools) (maybe, I really don't remember but I put it in the extracted ums512_alldocube_iplay_50_EN_20230801 folder and I always go to the adb folder when using it
- Enabled developer options on Rp3+ (Go to Settings → About Phone, Tap Build Number 7 times. Then back to Settings → System, Advanced, Developer options. **Enable USB Debugging and OEM Unlock in Developer Options**

**1.** Install Unisoc driver, extract adb to the extracted ums512_alldocube_iplay_50_EN_20230801 folder

**2.0** Put RP3+ into Android Recovery/Download Mode (Turn off, turn on while holding power along with bottom volume button) while your device is plugged in (You'll hopefully hear it [at least on windows] connect as you turn it on with a black screen in download mode)
**2.1** Download Mode work better for me when I reformatted the device with a new .pac file 4/22/2015 [https://drive.google.com/drive/folders/1g9m8BlrCsdzXduEUfDERLilVLzxFQxX8](https://drive.google.com/drive/folders/1g9m8BlrCsdzXduEUfDERLilVLzxFQxX8)

**3.** Run *unlock_autopatch_512.bat* from computer, and then enter fastboot on RP3+

**4.** Follow unlock_autopatch_512 instructions, profit I think. If that doesn't work, have your device plugged in first and then go into Android Recovery.

**5.** Restart device back to recovery mode, go to "Apply update from ADB" and restart running *unlock_autopatch_512.bat* from computer, follow those instructions.

**6.** If that doesn't work:

**6.1.** Restart RP3+ to normal use

**6.2.** Open cmd from file explorer folder of "ums512_alldocube_iplay_50_EN_20230801"

Type the following:

**6.3.** adb devices

**6.4.** adb push fdl1-dl.bin /data/local/tmp/

**6.5.** adb push fdl2-dl.bin /data/local/tmp/

**6.6.** unlock_autopatch_512


The bootloader unlock is required before flashing any custom firmware or custom fixes like
- ~~[GammaOS](https://github.com/TheGammaSqueeze/GammaOS)~~

1. GammaOS Lite v1.5.1 - Anbernic RG505: Device doesn't install GammaOS after running EraseUserData
2. GammaOS v1.5.1 - Anbernic RG505: Device doesn't install GammaOS after running EraseUserData
3. GammaOS Core Alternative Flashing Guide using RKDevTool (It's not Rockchip, duh) https://www.youtube.com/watch?v=_-6ZYrNGTRs
4. 


