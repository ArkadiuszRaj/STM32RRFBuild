# STM32 RRF Build
This repository contains the build system for the STM32 port of RRF V3.2 and later.
It allows creation of the firmware package for variety of the STM32 chips, supported by the STM32duino' Arduino Core library.

## Preparations
You need to clone following repositories into root folder of this cloned repo.

1. Main Ardunio core library, a foundation the RRF is using https://github.com/stm32duino/Arduino_Core_STM32.git

2. STM32 CMSIS library https://github.com/ARM-software/CMSIS_5.git

3. RTOS support package https://github.com/gloomyandy/FreeRTOS.git

4. STM32 port of the RepRapFirmware https://github.com/gloomyandy/RepRapFirmware.git

5. Support libraries for RRF https://github.com/gloomyandy/RRFLibraries.git

6. Wifi interface https://github.com/gloomyandy/DuetWiFiSocketServer


## Building 

Please run ./buid.sh script. 

It will go through all folders, eventually clone repositories and set proper branches. When cloned repo exists, it will try to fetch latest changes automatically. After ensuring all code is refreshed, it will start exeuting several cmake command to build libraries and finally firmware file.

Script uses ncurses menu system to allow selection of the board, sbc or esp8266 access types.
