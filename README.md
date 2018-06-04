# rtl88x1cu
This repository contains drivers for Realtek 8811CU/8821CU Wireless LAN 802.11ac USB NIC. Soruce code is based on a driver CD provided with a Realtek 8811CU card. It's updated to build on newer kernel versions.

## Build and install
Use following commands in source directory:
```
git clone https://github.com/LokManSiu/rtl88x1cu.git -b master
cd rtl88x1cu
make
sudo make install
sudo modprobe 8821cu
```
## Raspberry Pi
To build this driver on Raspberry Pi you need to set correct platform in Makefile.
Change
```
CONFIG_PLATFORM_I386_PC = y
CONFIG_PLATFORM_ARM_RPI = n
```
to
```
CONFIG_PLATFORM_I386_PC = n
CONFIG_PLATFORM_ARM_RPI = y
```
