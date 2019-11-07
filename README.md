Steps:

1. sudo apt install liblz4-tool
2. git clone https://github.com/VladimirSazonov/jw-boot-logo-for-Jetson-Nano
3. cd jw-boot-logo-for-Jetson-Nano
4. git clone https://github.com/nothings/stb
5. g++ -o jw_boot_image main.cpp
6. ./jw_boot_image [path_to_your_logo]
7. Make sure there is an output file named "bmp.blob"
8. Copy "bmp.blob" into your "[path_to_your_bsp]/Linux_for_Tegra/bootloader/"
9. cd [path_to_your_bsp]/Linux_for_Tegra/
10. Finish installation by the command: sudo ./flash.sh -k BMP --image bootloader/bmp.blob  jetson-nano-qspi-sd mmcblk0p1
