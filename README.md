# OptimizeLegion5-15ACH6H

Introduce to Optimize Legion 5 15ACH6H

Specs:

- Ryzen 5 5600H
- RTX 3060 6GB (Same RTX 3050/3050Ti/...)
- 16GB RAM
- 512GB SSD

# OPTIMIZE LEGION 5 15ACH6H

## 1. BIOS

- Increase VRAM to 2GB

## 2. Reinstall Windows (optional)
I recommend to reinstall Windows 11 for better performance and battery life. Because Windows 11 is optimized for AMD Ryzen 5000 series. And the default Windows has mayn bloatware which is not necessary.

- Download Windows 11 ISO from [Microsoft](https://www.microsoft.com/software-download/windows11)

- Create bootable USB with [Rufus](https://rufus.ie/)

- Install Windows 11

## 3. Install Drivers
Most of the drivers are installed automatically. But you can install the latest drivers from [Lenovo Support](https://pcsupport.lenovo.com/us/en/products/laptops-and-netbooks/legion-series/legion-5-15ach6h/downloads/driver-list/component?name=Display%20and%20Video%20Graphics)
Or u can download with [Lenovo Legion Toolkit](https://github.com/BartoszCichecki/LenovoLegionToolkit) which is a great tool for Legion series.

## 4. Install Software
There are some software that I recommend to install.
- Optimizer (see below): Tool that you can configure your laptop to get better performance and battery life(remember to read them carefully).
  - [Optimizer](https://github.com/hellzerg/optimizer)
  - [Winuntil](https://github.com/ChrisTitusTech/winutil)
- Fan control: You can control your fan speed with these tools.
  - [Legion Fan Control](https://www.legionfancontrol.com/)
- General tool: The most I recommend is Lenovo Legion Toolkit. It's a great tool for Legion series.
  - [Lenovo Legion Toolkit](https://github.com/BartoszCichecki/LenovoLegionToolkit)
- Gaming tool: You can use these tools to optimize your gaming experience.
  - [Nvidia GeForce Experience](https://www.nvidia.com/en-us/geforce/geforce-experience/): Optimize your game settings automatically for NVIDIA graphics card. But I don't recommend to use this because it. Normal settings are enough for gaming.
- Add 60Hz to driver(becasue 60Hz not supported by default)
  - [CRU](https://www.monitortests.com/forum/Thread-Custom-Resolution-Utility-CRU): Add 60Hz option.


## 5. Setttings
- Update newest Windows 11, drivers and software.
- System Properties -> Performance Options
  - Disable all animations except "Animate controls and elements inside windows", smooth edges of screen fonts, show window contents while dragging.

# Install Hackintosh
## 1. Increase VRAM to 2GB
- Go to BIOS -> Config -> Graphic Device -> Set to UMAFrameBufferSize -> Set to 2048MB
## 2. Increase EFI partition size to 250MB
Do it yourself.
## 3. Disabling XHCI1 Controller
Using Advanced Bios Legion 5: Add everything inside folder Advanced Bios Legion 5 to USB. Boot from that usb (Go to bios -> Boot -> Boot from USB **Remeber disable secure boot** first). Then go to Advanced -> FCH Common Options -> USB Configuration Options -> Disable XHCI1 Controller

## 4. Install Hackintosh
Create USB installer introduce by Dortania. [Link](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html#downloading-macos) (Using Opencore 0.88). We just create com.apple.recovery.boot folder and stop. After that we using PreBuilt (Folder EFI)
### 4.1. Ready to install
Using EFI folder from `EFI for Installer`
- Copy EFI folder to EFI partition
- Boot from USB (USB has 2 folder is EFI and com.apple.recovery.boot)

### 4.2. Install Hackintosh
- Must using GPU Dynamic option.
- Boot from USB -> In Opencore menu choose Install MacOS (Press "Space" to show hidden menu) -> Choose MacOS Installer
- Install MacOS (Remember connect to internet by Ethernet port)
### 4.3. Post Install
- Replace EFI folder with EFI folder in `EFI for Running`
- Save Opencore as default boot option
- Using Hacktintool and copy OC (inside EFI) to EFI partition: Open Hackintool -> Disk -> Mount Disk -> Open EFI partition -> Copy OC folder to EFI partition (Has Boot, Window) resutl like this (EFI partition has 3 folder is Boot, OC, Windows)
- Using EFI easy and add EFI boot option -> Go to BIOS -> Boot -> Opencore as default boot option.
- Reboot and enjoy Hackintosh
# Credits
- [kalkmann](https://github.com/kalkmann/Legion-5600H-Hackintosh)
- [Lunarixus](https://github.com/Lunarixus/Legion5-15ACH6H-macOS)
