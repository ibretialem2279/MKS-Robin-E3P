# Mks-Robin-E3P-Marlin2.0-Firmware
## Features
The firmware of Mks Robin E3P is forked from Robin Nano, based on [Marlin2.0.x](https://github.com/MarlinFirmware/Marlin), added the [LittlevGL](https://github.com/littlevgl/lvgl), supporting colourful GUI and touch screen. It is developed on PlatformIO, we hope more and more developers will participate the development of this repository.

![](https://github.com/makerbase-mks/Mks-Robin-Nano-Marlin2.0-Firmware/blob/master/Images/MKS_Robin_Nano_printing.png)

## Build
As the firmware is based on Marlin2.0.x which is built on the core of PlatformIO, the buid compiling steps are the same as Marlin2.0.x. You can directly using [PlatformIO Shell Commands](https://docs.platformio.org/en/latest/core/installation.html#piocore-install-shell-commands), or using IDEs contain built-in PlatformIO Core(CLI), for example, [VSCode](https://docs.platformio.org/en/latest/integration/ide/vscode.html#ide-vscode) and [Atom](https://docs.platformio.org/en/latest/integration/ide/atom.html). VSCode is recommended.

## About the gcode file preview
The images should be added to gcode file when slicing, and MKS has developed the [plugin for Cura](https://github.com/makerbase-mks/mks-wifi-plugin) to make it.

## About the image conversion
- Open [LVGL online image converter tool](https://lvgl.io/tools/imageconverter). 
- Open bmp images.
- Enter the saved file name.
- Choose color format:True color.
- Choose file output format:Binary RGB565.
- Start convertion.
- Save bin file.
- Copy the converted bin file to the assets folder.
- Copy the assets folder to the SD card.
- SD card is connected to the motherboard, and you can see the update interface after powering on.

## MKS Robin E3p build and update firmware

1. Build config:
     
- `default_envs = mks_robin_e3p`     
- `#define MOTHERBOARD BOARD_MKS_ROBIN_E3P`    
- `#define TFT_LVGL_UI_SPI`

2. Update firmware:
   
- Enter the `.pio\build\mks_robin_e3p` directory, copy the `assets` folder and `Robin_e3p.bin` to the sd card
- SD card is connected to the motherboard, and you can see the update interface after powering on.   
