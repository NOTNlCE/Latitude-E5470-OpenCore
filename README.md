# Latitude-E5470-OpenCore
My working copy of OpenCore for the Dell Latitude E5470 supporting Mojave through Monterey.

# Hardware

- i5-6300HQ
- HD 520
- 16GB DDR4
- 1080p Screen
- Intel Wireless
- 500GB SATA SSD

# What Works

- CPU + IGPU Power Management
- Battery Status
- HDMI
- Sleep and Wake
- Audio
- Keyboard & Audio Fn Keys
- Trackpad and Buttons (no gesture support)
- Intel WiFi (See notes)
- Dell E-Port Replicatior Dock & Dock Display Output

# Notes

At the time of writing, this contains a working OpenCore 0.7.8 image and configuration running Monterey (12.2.1).
This branch utilizes OpenCanopy, and has an APFS Variable set to Ignore with Secure Boot set to Disabled. These can be adjusted back to defaults if using macOS Big Sur or higher.

This branch also works with Mojave, Catalina, and Big Sur, but may require tweaks for various items.

Important: Currently, the keyboard and trackpad work well, but need work.
The brightness control keys currently crash the system, but Fn+B raises screen brightness and Fn+S decreases brightness.
Additionally, my system uses an i5-6300HQ and utilizes CPUFriend to tweak frequencies. Your machine may require these to be removed or disabled to boot.
I have reverted this WiFi card back to the stock Intel card and the associated Intel Airport kext has been added. If you are using a Broadcom card, please use AirPortBrcmFixup and the associated Bluetooth kexts for functionality. If you are using an OS other than macOS Monterey, please replace the copy of the Airport kext with the OS version you are using.

The latest commit of VoodooPS2 has support for Alps trackpads, but in my testing, this did not function. We are currently one revision behind main to support our trackpad using the "Trackpad as Mouse" SSDT. Hopefully improvements will come soon.

# Issues

As reported, the HDMI port is causing issues in macOS Monterey + newer. Progress can be viewed in the open issue #2.
