# *Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens*

## *交流QQ群：1071120659*

[中文](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/README.md)｜[English](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/README-EN.md)

![System Info](https://i.loli.net/2021/02/17/zMhEk3DxdnbOaU1.png)


### 配置
1. 主板: ASUS PRIME Z390-P
1. BIOS版本：2808
1. CPU: Intel® Core™ i9-9900K Processor
1. 核显: Intel® UHD Graphics 630
1. 板载网卡: Realtek® RTL8111H Gigabit LAN Controller
1. WiFi/蓝牙: BCM943602CS（BT4.2）
1. 声卡: Realtek® ALC 887 8-Channel High Definition Audio
1. 固态硬盘: Samsung SSD 970 EVO Plus 500GB

### BIOS设置
1. 高级-CPU设置--Intel(VMX) Virtualization Technology -enable
1. 高级-北桥-显示设置--首选显卡-Auto，初始化IGPU-enable，DVMT Pre-Allocated-1024M，RC6-auto
1. 高级-USB Configuration--XHCI Hand-off -enable
1. 高级-内置设备-Serial Port Configuration-Serial Port -off
1. 启动-启动设置--快速启动-disable，若出现错误等待按下F1键-disable
1. 设置模式-高级模式

**可适用操作系统版本：macOS Catalina 10.15.1～11.3 beta6**

1. OpenCore版本：0.6.8
1. CPU变频：正常。
1. UHD630：正常。

![Graphics Card](https://i.loli.net/2021/04/07/gEidfyJHLBGUv2N.png)
1. 3.5mm声音 & DP & HDMI：双屏环境下HDMI需要热开关一次才能正常显示，使用AppleALC驱动。
1. USB：正常。
1. 有线网卡：正常，使用了RealtekRTL8111.kext。
1. 睡眠唤醒：正常。

![Power Saver](https://i.imgur.com/wZ7IZjm.png)
1. 关机开机：正常。
1. iCloud & App Store & iMessage & FaceTime：请自行生成Board Serial Number、序列号、SmUUID，并相应的修改SysPrameter系统参数中的“自定义UUID”，和RtVariables变量设置中的MLB、ROM。
1. AirDrop & HandOff & Continuity：正常。

![Wi-Fi en0](https://i.imgur.com/daoSzyJ.png)
![BlueTooth](https://i.imgur.com/Cgr8AJv.png)
![Apple Watch](https://i.imgur.com/iYimFue.png)

### Tips：

1. 机型需设定为iMAC19.1（现已预置，安装完成后请自行修改）。
1. 该config默认为无verbose模式。如需启用verbose模式，config.plist需要修改以下一项：NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args，添加-v。
1. 该config启动盘策略 ScanPolicy 值设置为0。可引导Windows或Other OS（Linux、Unix）如需指定搜索分区类型，可参考OC配置手册。
1. 该config默认为不显示OC Picker菜单。如需开启菜单显示，设置如下：Misc-Boot-ShowPicker 值为true（plist编辑器中为YES）。

### 目前已知问题：

1. 启动磁盘中无法设定Windows为启动磁盘（提示Bless工具无法将此磁盘设定为启动磁盘）。 更新-该问题已解决，可查看[Windows Bootcamp.pdf](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/Boot%20Camp%E6%95%99%E7%A8%8B/Windows%20Bootcamp.pdf)
1. 启动转换助理不可用（应该是多硬盘问题，单硬盘据查该功能可正常使用） 。更新-该问题已解决，可查看[Windows Bootcamp.pdf](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/Boot%20Camp%E6%95%99%E7%A8%8B/Windows%20Bootcamp.pdf)

![Boot Camp](https://i.loli.net/2021/01/23/Ew1NepZ6kStuoh2.png)

