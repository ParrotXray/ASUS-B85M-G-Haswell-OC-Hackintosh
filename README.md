# 🍎Asus B85M-G Hackintosh 

## 🖥️Device
MB:Asus B85M-G.

BIOS version:0940.

CPU:i5 4460.

GPU:AMD Radeon RX560/HD4600.

Audio:Realtek ALC887.

Memory:32GB.

Ethernet/WIFI:Realtek 8111/BCM4360.

![alt text](info.png)


## 📀System

OS:MacOS Big Sur11.4

SMBIOS:iMac 15.1

![alt text](Mac.png)


## 🛠️Setting BIOS
### CPU:

Advanced/CPU Configuration/Inyel Virtuallzation Technology:Enabled

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

### Sleep:

Advanced/Onboard Devices Configuration/Serial Port Configuration/Serial Port:Disabled

### Boot:

Boot/Fast Boot:Disabled

Boot/CSM/Launch CSM: Disabled

Boot/Secure Boot menu/OS Type:Other OS


## 💡Device status

😪Sleep:normal

💾USB Device:normal

![alt text](Usb.png)

🔊Audio:normal,injact alcid=99

![alt text](Audio.png)

💻HD4600:unusual,Rx560 instead

![alt text](GPU.png)

📡WIFI/Ethernet:normal

![alt text](Ethernet.png)
