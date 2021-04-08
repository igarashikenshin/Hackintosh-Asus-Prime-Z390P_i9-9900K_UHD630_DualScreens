# *Hackintosh-Asus-Prime-Z390P_i9-9900K_RX5700XT*

[中文](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/README.md)｜[English](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/README-EN.md)

![System Info](https://i.loli.net/2021/04/07/IylTbpwdFNgDCjk.png)

### Configuration
1. Motherboard: ASUS PRIME Z390-P
1. BIOS version: 2808
1. CPU: Intel® Core™ i9-9900K Processor
1. Core display: Intel® UHD Graphics 630
1. Onboard network card: Realtek® RTL8111H Gigabit LAN Controller
1. WiFi/Bluetooth: BCM943602CS（BT4.2）
1. Sound Card: Realtek® ALC 887 8-Channel High Definition Audio
1. Solid State Drive: Samsung SSD 970 EVO Plus 500GB

### BIOS settings
1. Advanced-CPU settings-Intel(VMX) Virtualization Technology -enable
1. Advanced-North Bridge-Display Settings-preferred graphics card-Auto, initialize IGPU-enable, DVMT Pre-Allocated-1024M, RC6-auto
1. Advanced-USB Configuration--XHCI Hand-off -enable
1. Advanced-Built-in Device-Serial Port Configuration-Serial Port -off
1. Start-start settings-quick start-disable, if there is an error, wait for the F1 key-disable
1. Setting mode-advanced mode

**Applicable operating system version: macOS Catalina 10.15.1～11.3 beta7**

1. OpenCore version: 0.6.8
1. Clover version: Clover version is no longer available
1. CPU frequency conversion: Working.
1. UHD630: Working.

![Graphics Card](https://i.loli.net/2021/04/07/gEidfyJHLBGUv2N.png)
1. 3.5mm sound & DP & HDMI: HDMI needs to be hot-on/off once in a dual-screen environment to display normally, using AppleALC driver.
1. USB: Working.
1. Wired network card: Working, RealtekRTL8111.kext is used.
1. Wake up from sleep: Working.

![Power Saver](https://i.imgur.com/wZ7IZjm.png)
1. Turn off and turn on: Working.
1. iCloud & App Store & iMessage & FaceTime: Please generate the Board Serial Number, serial number, and SmUUID by yourself, and modify the "Custom UUID" in the SysPrameter system parameters, and the MLB and ROM in the RtVariables variable settings accordingly.
1. AirDrop & HandOff & Continuity: Working.

![Wi-Fi en0](https://i.imgur.com/daoSzyJ.png)
![BlueTooth](https://i.loli.net/2021/04/07/ocigaQV7JOCdpzF.png)
![Apple Watch](https://i.imgur.com/iYimFue.png)

### Tips:

1. The model needs to be set to iMAC19.1 (now preset, please modify it after installation).
1. The config defaults to no verbose mode. To enable verbose mode, config.plist needs to modify the following one: NVRAM-Add-7C436110-AB2A-4BBB-A880-FE41995C9F82-boot-args, add -v.
1. The ScanPolicy value of the config boot disk policy is set to 0. Bootable Windows or Other OS (Linux, Unix) If you need to specify the search partition type, please refer to the OC configuration manual.
1. The config defaults to not display the OC Picker menu. To turn on the menu display, set as follows: Misc-Boot-ShowPicker is true (YES in the plist editor).

### Currently known issues:

1. Windows cannot be set as the startup disk in the startup disk (it prompts that the Bless tool cannot set this disk as the startup disk). Update-the problem has been resolved,you can view [Windows Bootcamp.pdf](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/Boot%20Camp%E6%95%99%E7%A8%8B/Windows%20Bootcamp.pdf)
1. The boot conversion assistant is unavailable (it should be a problem with multiple hard drives, the function can be used normally according to the single hard drive). Update-This issue has been resolved, you can view [Windows Bootcamp.pdf](https://github.com/igarashikenshin/Hackintosh-Asus-Prime-Z390P_i9-9900K_UHD630_DualScreens/blob/master/Boot%20Camp%E6%95%99%E7%A8%8B/Windows%20Bootcamp.pdf)

![Boot Camp](https://i.loli.net/2021/01/23/Ew1NepZ6kStuoh2.png)
