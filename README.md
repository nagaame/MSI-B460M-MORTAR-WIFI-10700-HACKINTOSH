[![OpenCore Version](https://img.shields.io/badge/OpenCore-0.7.9-green.svg)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)
![GitLab tag (latest by date)](https://img.shields.io/gitlab/v/tag/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)
![GitHub issues](https://img.shields.io/github/issues-raw/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)

# MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH

# 硬件列表

| 项目   | 名称                          | 价格   |
| ---- | --------------------------- | ---- |
| CPU  | Intel 10th CORE 10700       | 2559 |
| 主板   | 微星迫击炮 MAG B460M MORTAR WiFi |      |
| 内存   | 芝奇 幻光戟 16GB * 2 DDR4 3200   | 800  |
| 显卡   | 核显 HD630                    | 0    |
| 硬盘   | 三星 970EVO Plus SSD 1TB      | 1019 |
| 硬盘2  | Intel 760P SSD              | 0    |
| 电源   | 安钛克 NE650W                  | 469  |
| 散热器  | 追风者 12DX 黑白版                | 249  |
| 机箱风扇 | 追风者 12cm RGB * 3            | 129  |
| 机箱   | 追风者 MATX 410                | 449  |
| 无线网卡 | BCM94360CS2 PCIE            | 200  |
| 独立显卡 | 蓝宝石 RX590                   | 1500 |

# 说明

USB定制已经配置, 不需要再次定制USB, 关闭了主板后置的两个USB2.0接口, 无线网卡蓝牙和WiFi都是原生驱动, 独显RX590 原生驱动

如果你需要自己重新定制, 把这两个驱动取消或删除, 打开XhciPortLimit选项, 重启后进行自己的USB定制

![](https://raw.githubusercontent.com/nagaame/images/master/img/fix-dir/2022/03/23/22-17-31-669316485e6c5aaaff5c21d8883264d8-1648032321679-55b9c6e9.jpg?token=ABPNKGF7UMZQPA3AZUQ4PLLCHMWD2)

# BIOS配置

[升级]([B460](https://cn.msi.com/Motherboard/MAG-B460M-MORTAR-WIFI/support)) 主板的BIOS到最新版本后, 只需要打开D.T.M选项即可, 其余大部分设置都不需要设置, 如果你的内存支持高频率的话, 可以打开BIOS对内存应用的XMP功能

# 跑分

## CPU

![](https://raw.githubusercontent.com/nagaame/images/master/img/fix-dir/2022/03/24/01-06-35-f9e31c6136e438a2850d26e11bc4def9-Snipaste_2022-03-23_22-25-11-6cc5d7d1.png?token=ABPNKGCCYIPHJ35RDV5M6RLCHNJ52)

## GPU

### opencl

![](https://raw.githubusercontent.com/nagaame/images/master/img/fix-dir/2022/03/24/01-15-50-59d4322949e9b51a0a14792a2a6cf51d-Snipaste_2022-03-23_22-28-49-5e7f3382.png)



# 安装过程



## 工具

* opencore configuration

* balenaEtcher

* U盘

* text editor





# 其他

## config.plist

默认文件为仅有核显情况下, 驱动核显, 不包括独显的一些优化和设置

## config.plist.gc

核显作为硬件加速功能, 驱动独显, 并且视频信号输出通过独显

# 感谢

* Apple

* [opencore]([GitHub - acidanthera/OpenCorePkg: OpenCore bootloader](https://github.com/acidanthera/OpenCorePkg))

* [opencore configuration]([Download OpenCore Configurator 2.58.1.0 | mackie100 projects](https://mackie100projects.altervista.org/download-opencore-configurator/))

* [Lilu]([GitHub - acidanthera/Lilu: Arbitrary kext and process patching on macOS](https://github.com/acidanthera/Lilu)) and [WhateverGreen]([GitHub - acidanthera/WhateverGreen: Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs](https://github.com/acidanthera/WhateverGreen))

* [PcBeta](https://www.pcbeta.com/)