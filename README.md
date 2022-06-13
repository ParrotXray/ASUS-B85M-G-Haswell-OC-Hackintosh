### 🌐Language
[English](README.md) | [中文](README-zh.md)

# 🍎ASUS-B85M-G-Haswell-Hackintosh 

## 🖥️Device

| Motherboard | Asus B85M-G |
|------------|-------------------------------|
| CPU | i5 4460,4570/i7 4770(Haswell) |
| dGPU | AMD Radeon RX580 |
| iGPU | Intel® HD Graphics 4600 |
| RAM | DDR3 1600MHz 32GB |
| Audio | Realtek ALC887 |
| WIFI／Bluetooth | FV-T919(BCM94360cd) |
| Ethernet | Realtek® 8111G |
| BIOS Version | 0904 |

## 📀System

### Noteice:
iGPU with Haswell cpu cannot be driven on macOS Ventura, dGPU needs to be installed
 
| ![alt text](Mac13.png) |
|------------|
| <a href="https://www.apple.com/tw/macos/macos-ventura-preview/"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/MacOS_logo_%282017%29.svg/512px-MacOS_logo_%282017%29.svg.png?20210723125421" height="32px"/>macOS Ventura 13(beta) |
| <a href="https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.1"><img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/LogoApprox.svg" height="34px"/>Opencore 0.8.1 |
| <a href="https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#how-to-decide"><img src="https://aux.iconspalace.com/uploads/imac-icon-256.png" height="30px"/>iMac 19.1 |
 
- Download:https://github.com/ParrotXray/ASUS-B85M-G-Haswell-OC-Hackintosh/releases/download/v0.8.1.Ventura/Opencore.0.8.1.build-macOS.Ventura.zip

| ![alt text](Mac.png) |
|------------|
| <a href="https://www.apple.com/tw/macos/monterey/"><img src="https://static.techspot.com/images2/downloads/topdownload/2021/10/2021-10-27-ts3_thumbs-36e.png" height="32px"/>macOS Monterey 12.4 |
| <a href="https://github.com/dortania/build-repo/releases"><img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/LogoApprox.svg" height="34px"/>Opencore 0.8.2-Dev |
| <a href="https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#how-to-decide"><img src="https://aux.iconspalace.com/uploads/imac-icon-256.png" height="30px"/>iMac 17.1 | 
 
- Download:https://github.com/ParrotXray/ASUS-B85M-G-Haswell-OC-Hackintosh/releases/download/v0.8.1/Opencore.0.8.1.build.zip

## 💡Device status
### Works：
- [x] Graphics
- [x] USB
- [x] Sleep
- [x] WiFi
- [x] Speakers
- [x] Microphone
- [x] Bluetooth
- [x] Ethernet
- [x] AirDrop
### Unkown：
- [ ] Apple Services

## 🛠️OC DevicePropertises setting

| Use iGPU+dGPU hardware acceleration |  Use iGPU(DVI)  |  Audio
:-------------------------:|:-------------------------:|:-------------------------:
PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x1B,0x0)
AAPL,ig-platform-id:04001204(DATA)|AAPL,ig-platform-id:0300220D(DATA)|layout-id:05000000(DATA)
device-id:12040000(DATA)|device-id:12040000(DATA)|-
model:Intel HD Graphics 4600(STRING)|framebuffer-fbmem:00009000(DATA)|-
-|framebuffer-stolenmem:00003001(DATA)|-
-|model:Intel HD Graphics 4600(STRING)|-

## 🛠️Setting BIOS

#### CFG lock:
- The BIOS preset is unlocked

#### SATA:

- Advanced/SATA Configuration/SATA Mode Selection：`AHCI`

#### CPU:

- Advanced/CPU Configuration/Intel Virtuallzation Technology：`Enabled`

- Advanced/System Agent Configuration/VT-d：`Disabled`

#### USB:

- Advanced/USB Configuraton/Legacy USB Support：`Enabled`

- Advanced/USB Configuraton/Intel xHCI Mode：`Enabled`

- Advanced/USB Configuraton/EHCI Hand-off：`Enabled`

#### Fix Sleep:

- Advanced/Onboard Devices Configuration/Serial Port Configuration/Serial Port：`Disabled`

#### Boot:

- Boot/Fast Boot：`Disabled`

- Boot/CSM/Launch CSM：`Disabled`

- Boot/Secure Boot menu/OS Type：`Other OS`

### GPU Settings

#### Use iGPU:

- Advanced/System Agent Configuration/Primary Display：`iGPU`

- Advanced/System Agent Configuration/iGPU Memory：`64M`

#### Use dGPU:

- Advanced/System Agent Configuration/Primary Display：`PCIE`

#### Use dGPU+iGPU hardware acceleration:

- Advanced/System Agent Configuration/Primary Display：`PCIE`

- Advanced/System Agent Configuration/iGPU Memory：`64M`

- Advanced/System Agent Configuration/iGPU Multi-Momltor：`Enabled`
