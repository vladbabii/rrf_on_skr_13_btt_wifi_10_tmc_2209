# RepRapFirmware on BTT Hardware ( SKR v1.3, Wifi 1.0, TMC 2209 )

![SKR v1.3, Wifi 1.0, TMC 2209](https://github.com/vladbabii/rrf_on_skr_13_btt_wifi_10_tmc_2209/blob/main/board.jpg?raw=true)

## Useful Links

* https://teamgloomy.github.io/
* https://github.com/gloomyandy/RepRapFirmware/releases/tag/v3.3.0_8
* https://github.com/gloomyandy/DuetWiFiSocketServer/releases/tag/V1.26-05
* https://www.reddit.com/r/3Dprinting/comments/lzlp4z/flashing_firmware_on_the_bigtreetech_rrf_wifi_10/


## Hardware:
* 1x SKR v.1.3 
* 1x BTT wifi 1.0 
* 3x BTT TMC-2209 (UART)

## Firmware
* BTT Wifi 1.0 -> DuetWiFiServer-esp8266-lpc-1.26-05.bin
* SKR v1.3     -> firmware-lpc-wifi-3.3.0_8.bin

## Docs
* BTT Wifi 1.0 -> https://github.com/bigtreetech/BTT-Expansion-module/blob/master/BTT%20RRF%20WiFi/BTT%20RRF%20WiFi%20V1.0%20User%20Manual.pdf
* SKR v1.3 -> https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3/tree/master/BTT%20SKR%20V1.3

# Flashing 8266

1. (windows) First thing first.. you need this driver to get the USB working.. http://www.wch-ic.com/downloads/CH341SER_EXE.html
2. (windows) Get NodeMCU Flasher -> https://github.com/nodemcu/nodemcu-flasher in Win32/Release or Win64/Release
3. start nodemcu flasher
4. hit gear icon
5. select DuetWiFiServer-esp8266-lpc-1.26-05.bin since skr has LPC processor
6. Put the card into burn mode 
6.1 pressi both the boot and reset buttons 
6.2 wait 1 second
6.3 release reset 
6.4 wait 1 second
6.5 release boot
7. click operation->flash
8. (optional) look at Log window

# Flashing SKR v1.3 -> LPC1768

1. copy firmware-lpc-wifi-3.3.0_8.bin to micro sd card as firmware.bin
2. insert card into board
3. power on, wait 15 seconds, power off
4. insert card into pc
5. check filename is now "FIRMWARE.CUR" -> means successfull flashing
6. connect btww wifi board to skr

# Configuration
1. use https://teamgloomy.github.io/Configurator/Start
2. get files
3. put on a new sd card on /sys
4. get web files from https://github.com/Duet3D/DuetWebControl/releases
5. put files on sd card on /www

# First usage
1. power on board, check your router for board if (if it's dhcp)
2. open http://ip-address-goes-here
3. enjoy
