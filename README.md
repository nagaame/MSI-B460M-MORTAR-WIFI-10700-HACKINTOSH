[![OpenCore Version](https://img.shields.io/badge/OpenCore-0.8.6-green.svg)](https://github.com/acidanthera/OpenCorePkg)
[![platform](https://img.shields.io/badge/platform-MacOS11/12/13-red.svg?logo=apple)](https://developer.apple.com/macos)
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/tags)
[![GitHub issues](https://img.shields.io/github/issues-raw/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/issues)
[![GitHub all releases](https://img.shields.io/github/downloads/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/total.svg)](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/releases/latest)
[![Telegram](https://img.shields.io/badge/-telegram-red?color=blue&logo=telegram)](https://t.me/sonny_kirby)

# MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH

### 📂The repository is Archived.

![MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH](https://cdn.kanda.me/images/2022/06/10/0/aff5bb138c5e2084bf093952936af64aff04d225.png)

## 硬件列表

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

## 版本历史

| Tag   | MacOS  | OpenCore |
| ----- | ------ | -------- |
| 0.0.2 | 12.3.1 | 0.7.9    |
| 0.0.3 | 12.3.1 | 0.7.9    |
| 0.0.4 | 12.3.1 | 0.8.0    |
| 0.0.5 | 12.4   | 0.8.0    |
| 0.0.6 | 12.6   | 0.8.4    |
| 0.0.7 | 13.0.1 | 0.8.6    |

## 跑分

### CPU

![](https://cdn.kanda.me/images/2022/06/10/0/6b2dbe16b2296a23efd68c17dd81e2c2f1a9611a.png)

### GPU

#### OpenCL(rx590)

![](https://cdn.kanda.me/images/2022/06/10/0/a21c5ca7658e63f110eddcf8fa7ebff21970bf45.png)

#### Metal(rx590)

![](https://cdn.kanda.me/images/2022/06/10/0/ce9be6793c2396aa96eaa12438125a093db9443b.png)

## 截图

驱动情况截图见[文件夹](https://github.com/nagaame/MSI-B460M-MORTAR-WIFI-10700-HACKINTOSH/tree/master/screenshot)

## 安装流程

### 工具

* opencore configuration

* balenaEtcher

* U盘/移动硬盘

* text editor

* 良好的上网环境

### 第一步

你可以自己使用[gibMacOS](https://github.com/corpnewt/gibMacOS)下载镜像文件, 自己制作U盘引导盘, 也可以从我共享的阿里云盘下载DMG[镜像](https://www.aliyundrive.com/s/pWXnWL2EPkf)文件, 改后缀名PDF为DMG, 然后使用`balenaEtcher`写入到你的U盘中, 注意DMG文件得是包含分区描述信息的, 写入完成后U盘有两个分区, 一个`EFI`分区和系统数据分区, 使用工具挂载`EFI`分区后, 在`EFI`分区创建一个`EFI`文件夹, 接着把仓库的两个文件夹复制到`EFI`文件夹中, 如果镜像自带其他的`EFI`文件夹, 直接替换旧的`EFI`文件夹即可, 替换成功就可以重启进行引导和安装了

### 引导

重启, 一直重复按**F12**, 调出引导菜单, 选择从已经写入系统和引导的U盘或者移动硬盘引导, 如果可以正常显示`opencore`的菜单, 说明引导成功, 选择install macOS xxx 等待引导

接着会显示安装界面, 首先格式化硬盘, 我们打开左上角的菜单, 选择硬盘工具, 找到你需要格式化的硬盘, 选择抹掉, 名称可以输入`MacOS`或者其他好记忆的名字, 格式选择`APFS`, 分区图选择`GUID`分区图, 然后抹掉成功后, 退出磁盘工具, 回到安装流程, 选择格式化后的硬盘, 选中它, 直接点击下一步安装, 没有格式化过的硬盘无法安装MacOS

> ⚠️ 格式化后, 会丢失这个硬盘的数据, 记得你要确保这个硬盘是闲置的, 没有数据的, 或者已经备份这个需要被格式化的硬盘的数据⚠️

### 设置

静待拷贝文件成功, 接着我们重启, 还是按**F12**调出引导菜单, 选择你的U盘/移动硬盘引导`opencore`, 打开`opencore`菜单后, 选择你上一步, 格式化的硬盘的名字的那个选项, 正式启动`MacOS`, 等待启动, 显示界面后, 设置新系统的设置和选项, 你也可以在这一步选择从`TimeMachine`或者其他Mac恢复你的数据

### 后续

启动成功后, 说明`MacOS`已经安装成功, 我们还需要一些步骤配置一下, 安装opencore configuration app, 接着使用app挂载安装了MacOS的这块硬盘的`EFI`分区, 然后创建一个`EFI`文件夹, 如果有了就不需要创建了, 然后拷贝仓库`opencore`和驱动文件到这个`EFI`文件夹中

## 说明

### USB定制

USB定制已经配置, 不需要再次定制USB, 关闭了主板后置的两个USB2.0接口, 无线网卡蓝牙和WiFi都是原生驱动, 独显`RX590` 原生驱动

如果你需要自己重新定制, 把这两个驱动取消或删除, 打开`XhciPortLimit`选项, 重启后进行自己的USB定制

如需定制, 建议使用[USBToolBox](https://github.com/USBToolBox/tool)进行USB定制

![](https://cdn.kanda.me/images/2022/06/10/0/a7d43fea1cca89088abdb35808851100864a0780.jpeg)

### BIOS配置

[升级](https://cn.msi.com/Motherboard/MAG-B460M-MORTAR-WIFI/support)主板的BIOS到最新版本后, 只需要打开`D.T.M`选项即可, 其余大部分设置都不需要设置, 如果你的内存支持高频率的话, 可以打开`BIOS`对内存应用的`XMP`功能

### 必要驱动

驱动文件说明, 请参考[这里](https://github.com/maemual/MSI-B460M-10700-5500XT#%E7%AC%AC%E4%B8%89%E6%AD%A5%E6%94%B6%E9%9B%86%E9%A9%B1%E5%8A%A8%E6%96%87%E4%BB%B6)

![](https://cdn.kanda.me/images/2022/06/10/0/de1bfa6f378a4945fdf82b187c360edab578be42.png)

### 配置文件

#### config.plist

默认文件为仅有核显情况下, 驱动核显, 不包括独显的一些优化和驱动设置

#### config.550.plist

核显作为硬件加速功能, 驱动**vega56/64**系列,  并且视频信号输出通过独显, 核显无法作为视频信号输出, 使用的话, 记得改名成config.plist

#### config.5500.plist

驱动新款的**5500xt** + 独显的配置, 因为本人没有55xx系的显卡, 只是按照理论上驱动的配置去添加了配置文件, 还有待测试, 视频信号输出通过独显, 核显无法作为视频信号输出, 使用的话, 记得改名成config.plist

## 注意

- 只驱动核显的话, 优先使用主板的DP接口而不是HDMI接口, 没有对HDMI进行一些好的配置, HDMI可能会产生花屏问题

- 这块(微星B460M迫击炮)主板HDMI接口不支持4K/60Hz, 只有4K/30Hz, 只有DP接口支持4K/60Hz

- 显示器建议使用4K分辨率的显示器, 大部分情况下默认会开启HIDPI

- 显示器的DP协议建议使用比较新的1.4版本协议, 如果出现黑屏问题在显示器设置里边切换其他版本DP协议试试

- 记得使用`opencore configuration`修改`opencore`的config.plist配置文件手动**注入三码**

- 如果没有进行USB定制的话, 可能会导致休眠失败/唤醒等休眠不彻底问题

- 如果你的引导画面苹果logo比较大, 或者你的显示器不是4K的显示器, 可以编辑配置文件`NVRAM`-> `4D1EDE05-38C7-4A6A-9CC6-4BCCA8B38C14`中的`UIScale`修改为01, 如果是HIDPI屏幕就修改成02

- 每次修改`NVRAM`的内容, 保存重启后, 都需要重新刷新`NVRAM`

- 修改`7C436110-AB2A-4BBB-A880-FE41995C9F82`的`boot-args`参数去掉`-v`可以关闭啰嗦模式, 记得每个参数需要空格分隔

- 驱动对主板的2.5Gbps有线网卡支持似乎有兼容问题, 有线连接建议手动修改成1000Mbps速率

- 不包括驱动主板自带的Intel无线网卡, 如需驱动见[itlwm](https://github.com/OpenIntelWireless/itlwm)

- RX590显卡用户如果发现驱动异常, 尝试移除`RadeonBoost.kext`驱动

## 驱动情况

- [x] 睡眠唤醒

- [x] USB定制(USB2/USB3)

- [x] 核显(仅支持到10代, 不支持11/12代CPU的核显)

- [x] 独显(rx550/580/590/5500xt)

- [x] 2.5Gbps板载以太网卡

- [x] WiFi/Bluetooth(需要免驱WiFi/Bluetooth无线网卡)

- [x] AirDrop(需要免驱WiFi/Bluetooth无线网卡)

- [x] 接力和随航(需要免驱WiFi/Bluetooth无线网卡)

- [x] 通用控制(需要12.3+ version系统)

- [x] FaceTime/iMessage/App Store(需要注入三码)

## 引用

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
