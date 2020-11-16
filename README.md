# Latitude-E5470-OpenCore
My working copy of OpenCore for the Dell Latitude E5470 supporting Mojave through Big Sur.

At the time of writing, this contains a working OpenCore 0.6.3 image and configuration running Catalina (10.15.7) and Big Sur (11.0.1). 
This branch utilizes OpenCanopy, but does not include the required "Resources" folder - please pull the latest from OcBinaryData.

This branch also works with Mojave, but may require tweaks.

Important: Currently, the keyboard and trackpad work well, but need work. 
The brightness control keys currently crash the system, but Fn+B raises screen brightness and Fn+S decreases brightness.
Additionally, my system uses an i5-6300HQ and utilizes CPUFriend to tweak frequencies. Your machine may require these to be removed or disabled to boot.
I have replaced the stock Intel WiFi card with a DW1560 which works well in Catalina, but requires the noted tweaks for Big Sur. These are applied in the config.plist already.

Hardware:
Dell Latitude E5470 14" Notebook
1080p 13.9" Display
Intel Core i5-6300HQ
16GB DDR4 RAM
DW1560 Wireless
