### 🌐Language
[English](README.md) | [中文](README-zh.md)

# 🍎Asus B85M-G Hackintosh 

## 🖥️Device

| Model | Asus B85M-G |
|------------|-------------------------------|
| CPU | i5 4460,4570,i7 4770(Haswell) |
| dGPU | AMD Radeon RX580 |
| iGPU | Intel® HD Graphics 4600 |
| RAM | 32GB |
| Audio | Realtek ALC887 |
| WIFI／Bluetooth | BCM94360cd |
|Ethernet|Realtek 8111|
| BIOS Version | 0904 |

## 📀System

| Version |
|------------|
![alt text](Mac.png)
| <img src="https://static.techspot.com/images2/downloads/topdownload/2021/10/2021-10-27-ts3_thumbs-36e.png" height="32px"/>Monterey 12.2.1 |
| <img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/LogoApprox.svg" height="34px"/>Opencore 0.7.8 |
| <img src="https://freepikpsd.com/file/2019/10/logo-ordinateur-png-1-Transparent-Images.png" height="30px"/> SMBIOS:iMac 17.1 | 

## 🛠️OC DevicePropertises setting

   iGPU+dGPU hardware acceleration |  Use iGPU(DVI)  |  Audio
:-------------------------:|:-------------------------:|:-------------------------:
PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x1B,0x0)
AAPL,ig-platform-id:04001204(DATA)|AAPL,ig-platform-id:0300220D(DATA)|layout-id:05000000(DATA)
device-id:12040000(DATA)|device-id:12040000(DATA)|-
model:Intel HD Graphics 4600(STRING)|framebuffer-fbmem:00009000(DATA)|-
-|framebuffer-stolenmem:00003001(DATA)|-
-|model:Intel HD Graphics 4600(STRING)|-

## 🛠️Setting BIOS
### Hard drive:

SATA Mode:AHCI

### CPU:

Advanced/CPU Configuration/Intel Virtuallzation Technology:Enabled

Advanced/System Agent Configuration/VT-d:Disabled

### iGPU:

Advanced/System Agent Configuration/Primary Display:iGPU

Advanced/System Agent Configuration/iGPU Memory:64M

### dGPU:

Advanced/System Agent Configuration/Primary Display:PCIE

### dGPU+iGPU:

Advanced/System Agent Configuration/Primary Display:PCIE

Advanced/System Agent Configuration/iGPU Memory:64M

Advanced/System Agent Configuration/iGPU Multi-Momltor:Enabled

### USB:

Advanced/USB Configuraton/Legacy USB Support:Enabled

Advanced/USB Configuraton/Intel xHCI Mode:Enabled

Advanced/USB Configuraton/EHCI Hand-off:Enabled

### Fix Sleep:

Advanced/Onboard Devices Configuration/Serial Port Configuration/Serial Port:Disabled

### Boot:

Boot/Fast Boot:Disabled

Boot/CSM/Launch CSM: Disabled

Boot/Secure Boot menu/OS Type:Other OS


## 💡Device stetus

😪Sleep:normal

💾USB Device:normal

![alt text](Usb.png)

🔊Audio:normal,injact alcid=5

![alt text](Audio.png)

💻iGPU:Assist dGPU hardware acceleration/dGPU:normal

![alt text](GPU.png)

📡WIFI/Ethernet:normal

![alt text](Ethernet.png)
