# RPI GAMEPAD

## Introduction
This experiment aims at developing a gamepad driver for the Raspberry Pi board.

## Toolchains

### MacOS X: toolchain used for this project
For this project I used the following toolchain:

http://www.welzels.de/blog/download/gcc-linaro-arm-linux-gnueabihf-raspbian-2014.05_mac.zip

After unpacking it, I installed it under:

/usr/local/linaro/arm-linux-gnueabihf-raspbian/

#### To build the source code with Linaro-based toolchain
mkdir build_arm
cd build_arm
cmake -D CMAKE_TOOLCHAIN_FILE=../rpi.cmake ../
make
