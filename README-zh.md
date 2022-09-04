### 🌐Language
[English](README.md) | [中文](README-zh.md)

# 🍎ASUS-B85M-G-Haswell-Hackintosh 

## 🖥️設備

| 主板 | Asus B85M-G |
|------------|-------------------------------|
| CPU | i5 4460,4570,i7 4770(Haswell 1150 CPUs) |
| 獨顯dGPU | AMD Radeon RX580 |
| 內顯iGPU | Intel® HD Graphics 4600 |
| 記憶體 | 32GB |
| 音頻 | Realtek ALC887 |
| WIFI／Bluetooth | FV-T919(BCM94360cd) |
| 內建網卡 | Realtek® 8111G |
| BIOS版本 | 0904 |

## 📀系統

### macOS Ventura

**注意**:  
在macOS Ventura上無法驅動帶有Haswell cpu的核顯，需要安裝獨顯

**更新macOS Ventura B3需注意**:  
替換完OC版本後，在終端機先執行此命令 **`sudo kextcache -i/`** ，在系統更新重啟後，需要先執行 **`CleanNvram.efi`** 後才能繼續下一步，如果在之前更新失敗需要套用新的OC引導後需在系統設置再下載一次更新

| ![alt text](Mac13.png) |
|------------|
| <a href="https://www.apple.com/tw/macos/macos-ventura-preview/"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/MacOS_logo_%282017%29.svg/512px-MacOS_logo_%282017%29.svg.png?20210723125421" height="32px"/>macOS Ventura 13(beta 6) |
| <a href="https://github.com/dortania/build-repo/releases/tag/OpenCorePkg-3e2e62a"><img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/LogoApprox.svg" height="34px"/>Opencore 0.8.4-Dev-3e2e62a |
| <a href="https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#how-to-decide"><img src="https://aux.iconspalace.com/uploads/imac-icon-256.png" height="30px"/>iMac 19.1 |

- <a href=https://github.com/ParrotXray/ASUS-B85M-G-Haswell-OC-Hackintosh/releases/tag/v0.8.4-Dev-3e2e62a><img src="https://aux.iconspalace.com/uploads/downloads-folder-icon-256.png" height="32px">點我下載EFI文件

### macOS Monterey

| ![alt text](Mac.png) |
|------------|
| <a href="https://www.apple.com/tw/macos/monterey/"><img src="https://static.techspot.com/images2/downloads/topdownload/2021/10/2021-10-27-ts3_thumbs-36e.png" height="32px"/>macOS Monterey 12.5 |
| <a href="https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.3"><img src="https://raw.githubusercontent.com/acidanthera/OpenCorePkg/master/Docs/Logos/LogoApprox.svg" height="34px"/>Opencore 0.8.3 |
| <a href="https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#how-to-decide"><img src="https://aux.iconspalace.com/uploads/imac-icon-256.png" height="30px"/>iMac 17.1 | 

- <a href=https://github.com/ParrotXray/ASUS-B85M-G-Haswell-OC-Hackintosh/releases/tag/v0.8.3><img src="https://aux.iconspalace.com/uploads/downloads-folder-icon-256.png" height="32px">點我下載EFI文件
 
## 💡設備狀態
### 正常工作：
- [x] 顯卡
- [x] USB
- [x] 睡眠
- [x] WiFi
- [x] 揚聲器
- [x] 麥克風
- [x] 藍芽
- [x] 內建網卡
### 未知：
- [ ] Apple服務

## 🛠️OC DevicePropertises設定

| 使用iGPU+dGPU硬件加速 |  使用iGPU(DVI)  |  音頻
:-------------------------:|:-------------------------:|:-------------------------:
PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x2,0x0)|PciRoot(0x0)/Pci(0x1B,0x0)
AAPL,ig-platform-id:04001204(DATA)|AAPL,ig-platform-id:0300220D(DATA)|layout-id:05000000(DATA)
device-id:12040000(DATA)|device-id:12040000(DATA)|-
model:Intel HD Graphics 4600(STRING)|framebuffer-fbmem:00009000(DATA)|-
-|framebuffer-stolenmem:00003001(DATA)|-
-|model:Intel HD Graphics 4600(STRING)|-

## 🛠️BIOS設定
  
#### CFG鎖:

- BIOS 預設已解鎖

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

### GPU設定

#### 只使用iGPU:

- Advanced/System Agent Configuration/Primary Display：`iGPU`

- Advanced/System Agent Configuration/iGPU Memory：`64M`

#### 只使用dGPU:

- Advanced/System Agent Configuration/Primary Display：`PCIE`

#### 使用dGPU+iGPU硬件加速:

- Advanced/System Agent Configuration/Primary Display：`PCIE`

- Advanced/System Agent Configuration/iGPU Memory：`64M`

- Advanced/System Agent Configuration/iGPU Multi-Momltor：`Enabled`
