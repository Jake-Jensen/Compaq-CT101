# Compaq-CT101
My repo housing my personally dumped firmware, root instructions, and everything else related to this rather unknown tablet.

# Required tools
ADB
Fastboot
MTK fastboot drivers 
(links incoming soon)

## Root steps
1. Enable OEM unlocking switch in developer settings
2. Using ADB, do `adb reboot bootloader`
3. Once in the bootloader state, select fastboot
4. Using fastboot, do `fastboot oem unlock` then `fastboot flashing unlock`. I'm not sure which one works as they both returned success for me.
5. Download the Magisk boot image from this repo, and put it next to your fastboot executable.
6. Using fastboot do `fastboot flash boot magiskboot.bin`
7. wait for it to finish, then do `fastboot reboot`
8. Once Android starts, open the magisk stub app, then press install, and under method, select `direct`, and you're done.
