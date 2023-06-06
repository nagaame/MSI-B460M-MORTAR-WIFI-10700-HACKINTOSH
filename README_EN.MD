[![OpenCore Version](https://img.shields.io/badge/OpenCore-0.8.6-green.svg)](https://github.com/acidanthera/OpenCorePkg)
[![platform](https://img.shields.io/badge/platform-MacOS11/12/13-red.svg?logo=apple)](https://developer.apple.com/macos)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/tags)
[![GitHub issues](https://img.shields.io/github/issues-raw/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/issues)
[![GitHub all releases](https://img.shields.io/github/downloads/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/total.svg)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/releases/latest)
[![Telegram](https://img.shields.io/badge/-telegram-red?color=blue&logo=telegram)](https://t.me/sonny_kirby)

# MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH

![MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH](https://cdn.kanda.me/images/2022/06/10/0/aff5bb138c5e2084bf093952936af64aff04d225.png)

## Hardware list.

| 项目   | 名称                          | 价格   |
| ---- | --------------------------- | ---- |
| CPU  | Intel 10th CORE 10700       | 2559 |
| 主板   | 微星迫击炮 MAG B460M MORTAR WiFi |      |
| 内存   | 芝奇 幻光戟 16GB * 2 DDR4 3200   | 800  |
| 显卡   | 核显 HD630                    | 0    |
| 显示器  | LG 27UL850 (4K)             | 2800 |
| 硬盘   | 三星 970EVO Plus SSD 1TB      | 1019 |
| 硬盘2  | Intel 760P SSD              | 0    |
| 电源   | 安钛克 NE650W                  | 469  |
| 散热器  | 追风者 12DX 黑白版                | 249  |
| 机箱风扇 | 追风者 12cm RGB * 3            | 129  |
| 机箱   | 追风者 MATX 410                | 449  |
| 无线网卡 | BCM94360CS2 PCIE(免驱)        | 200  |
| 独立显卡 | 蓝宝石 RX590                   | 1500 |

## 

## Version history.

| Tag   | MacOS  | OpenCore |
| ----- | ------ | -------- |
| 0.0.2 | 12.3.1 | 0.7.9    |
| 0.0.3 | 12.3.1 | 0.7.9    |
| 0.0.4 | 12.3.1 | 0.8.0    |
| 0.0.5 | 12.4   | 0.8.0    |
| 0.0.6 | 12.6   | 0.8.4    |
| 0.0.7 | 13.0.1 | 0.8.6    |

## Benchmark

### CPU

![](https://cdn.kanda.me/images/2022/06/10/0/6b2dbe16b2296a23efd68c17dd81e2c2f1a9611a.png)

### GPU

#### OpenCL(rx590)

![](https://cdn.kanda.me/images/2022/06/10/0/a21c5ca7658e63f110eddcf8fa7ebff21970bf45.png)

#### Metal(rx590)

![](https://cdn.kanda.me/images/2022/06/10/0/ce9be6793c2396aa96eaa12438125a093db9443b.png)

## Screenshot

Please refer to the [folder](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/tree/master/screenshot) for a screenshot of the driver status.

## 安装流程

### 工具

* opencore configuration

* balenaEtcher

* U盘/移动硬盘

* text editor

* 良好的上网环境

### 第一步

You can use `gibMacOS` to download the image file and create a bootable USB drive, or alternatively you can download the DMG image file from my shared Alibaba Cloud Drive [here](https://www.aliyundrive.com/s/pWXnWL2EPkf). Make sure to change the file extension from PDF to DMG before using `balenaEtcher` to write the file to your USB drive. Also, please note that the DMG file should contain partition descriptor information, and once the writing process is complete, your USB drive should have two partitions: an `EFI` partition and a data partition for the system. After mounting the `EFI` partition using a tool, create an `EFI` folder in the partition, then copy the two folders from the repository into the `EFI` folder. If the image comes with other `EFI` folders, simply replace the old `EFI` folder with the new one. Once the replacement is successful, you can restart your device to begin the booting and installation process.

### Boot

Restart your device and continuously press **F12** to access the boot menu. From there, select the option to boot from the USB drive or external hard drive that you have already written the system and bootloader onto. If the `opencore` menu displays correctly, then the booting process has succeeded. Select `install macOS xxx` from the menu and wait for the installation to complete.

Next, the installation interface will appear. The first step is to format your hard drive. To do this, open the menu in the top left corner of the screen and select "Disk Utility". Find the hard drive you want to format and select "Erase". You can name it "MacOS" or any other memorable name, choose `APFS` as the format, and select `GUID Partition Map` as the partition map. After successful formatting, exit the Disk Utility and return to the installation process. Select the formatted hard drive and click "Next" to install. Please note that macOS cannot be installed on a hard drive that has not been formatted.

> ⚠️ Warning: Formatting the hard drive will result in the loss of all data on that drive. Please ensure that the hard drive is not being used and does not contain any important data. If necessary, please make sure to backup any important data before proceeding with the formatting process. ⚠️

### Settings

Wait patiently for the file transfer to complete. Then, restart your device and press **F12** to access the boot menu again. Select your USB drive or external hard drive that contains the `opencore` bootloader. After opening the `opencore` menu, select the option with the name of the hard drive you formatted in the previous step to officially start `MacOS`. Wait until the system starts up, and then set up your new system settings and preferences. If necessary, you can also choose to restore your data from a `Time Machine` backup or another Mac at this step.

### Afterwards

If the system has successfully started up, it means that `MacOS` has been installed successfully. However, there are still some steps you need to follow to properly configure the system. First, you need to install the "opencore configuration app". Next, use the app to mount the `EFI` partition on the hard drive where macOS is installed. Then, create an `EFI` folder (if it doesn't already exist) and copy the `opencore` bootloader and driver files from the repository into this `EFI` folder.

## Explanation

### USB customization.

USB customization has already been configured, so there is no need to customize the USB again. The two USB 2.0 ports on the back of the motherboard have been disabled. The wireless network card's Bluetooth and WiFi functions are both natively supported, and the dedicated graphics card `RX590` is also natively supported.

If you need to customize the USB again, you can disable or remove these two drivers, enable the `XhciPortLimit` option, and then restart your device to perform the USB customization according to your needs.

If you need to customize your USB, it is recommended that you use [USBToolBox](https://github.com/USBToolBox/tool) to perform the customization.

![](https://cdn.kanda.me/images/2022/06/10/0/a7d43fea1cca89088abdb35808851100864a0780.jpeg)

### BIOS configuration.

After [upgrading](https://cn.msi.com/Motherboard/MAG-B460M-MORTAR-WIFI/support) your motherboard's BIOS to the latest version, you only need to enable the D.T.M option. Most of the other settings do not need to be changed. If your memory supports high frequency, you can also enable the XMP feature in the BIOS to apply it to your memory.

### Essential drivers

For an explanation of the driver files, please refer to [here](https://github.com/maemual/MSI-B460M-10700-5500XT#%E7%AC%AC%E4%B8%89%E6%AD%A5%E6%94%B6%E9%9B%86%E9%A9%B1%E5%8A%A8%E6%96%87%E4%BB%B6).

![](https://cdn.kanda.me/images/2022/06/10/0/de1bfa6f378a4945fdf82b187c360edab578be42.png)

### Config files

#### config.plist

The default files only include drivers for the integrated graphics card. They do not include any optimizations or driver settings for dedicated graphics cards.

#### config.550.plist

Translation: The integrated graphics card serves as a hardware acceleration feature and can be used to drive the `vega56/64` series of dedicated graphics cards. However, video output is only possible through the dedicated graphics card; the integrated graphics card cannot provide video output. If you want to use the integrated graphics card, please remember to rename the configuration file as `config.plist`.

#### config.5500.plist

Translation: To install and use the `5500xt` graphics card with a dedicated graphics card, you can add the necessary configuration file to your system. However, please note that this configuration has not been tested since I don't have a `55xx` series graphics card myself. Video output is only possible through the dedicated graphics card; the integrated graphics card cannot provide video output. If you want to use the integrated graphics card, please remember to rename the configuration file as `config.plist`.

## Attention

- If only the integrated graphics card is used, the DP interface on the motherboard is preferred over the HDMI interface. No good configuration has been made for HDMI, which may cause screen flickering issues.
- The HDMI interface on this MSI B460M Mortar WiFi motherboard only supports 4K/30Hz, while the DP interface supports 4K/60Hz.
- It is recommended to use a 4K resolution display, which will usually enable HIDPI by default.
- For the display's DP protocol, it is recommended to use the newer 1.4 version. If you encounter black screen issues, try switching to a different version of the DP protocol in the display settings.
- Remember to manually inject the three codes into the `opencore` config.plist file using the `opencore configuration`.
- If USB customization has not been performed, it may cause problems with sleep mode, such as failure to enter or exit sleep mode completely.
- If your boot logo (Apple logo) is too large or your display is not a 4K display, you can edit the `UIScale` in the `NVRAM` -> `4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14` section of the configuration file to modify it to 01. If it is an HIDPI screen, change it to 02.
- After modifying the contents of `NVRAM`, you need to refresh it after saving and restarting.
- You can disable verbose mode by modifying the `boot-args` parameter in `7C436110-AB2A-4BBB-A880-FE41995C9F82`. Remember to separate each parameter with a space.
- There may be compatibility issues with support for the motherboard's 2.5Gbps Ethernet port. For a wired connection, it is recommended to manually set the speed to 1000Mbps.

- The drivers provided do not include support for the Intel wireless network card that comes with the motherboard. If you need to use it, please refer to [itlwm](https://github.com/OpenIntelWireless/itlwm) for the driver installation guide.
- If there are issues with the RX590 graphics card driver, try removing the `RadeonBoost.kext` driver.

## Driver situation

- [x] Sleep and wake-up functions
- [x] USB customization (USB2/USB3)
- [x] Integrated graphics card (only supports up to 10th generation CPUs, does not support 11th or 12th generation CPU integrated graphics cards)
- [x] Dedicated graphics card (rx550/580/590/5500xt)
- [x] Onboard 2.5Gbps Ethernet port
- [x] WiFi/Bluetooth (requires a compatible wireless network card with native macOS support)
- [x] AirDrop (requires a compatible wireless network card with native macOS support)
- [x] Handoff and Sidecar (requires a compatible wireless network card with native macOS support)
- [x] Universal Control (requires macOS 12.3+ version)
- [x] FaceTime/iMessage/App Store (requires injection of three codes)

## Quote

* https://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1924348&highlight=Monterey%2B12.3

* https://github.com/mrdonkey3/hackintosh-oc-msi-b460m-mortar-i7-10700-big-sur

## Credits

* [Apple](https://www.apple.com.cn/)

* [opencore](https://github.com/acidanthera/OpenCorePkg)

* [opencore configuration](https://mackie100projects.altervista.org/download-opencore-configurator/)

* [balenaEtcher](https://www.balena.io/etcher/)

* [gibMacOS](https://github.com/corpnewt/gibMacOS)

* [Lilu](https://github.com/acidanthera/Lilu) and [WhateverGreen](https://github.com/acidanthera/WhateverGreen)

* [Hackintool](https://github.com/headkaze/Hackintool)

* [USBToolBox](https://github.com/USBToolBox/tool)

* [PcBeta](https://www.pcbeta.com/)
