# My Hackintosh OpenCore config for Gigabyte Z390 Aorus Pro WiFi 

## Hardware Config

- Gigabyte：Gigabyte Z390 Aorus Pro WiFi
- BIOS Version：F9
- CPU：i7-8700
- GPU：MSI RX570 ARMOR 4G OC
- Memory：Kingston 8G DDR4-3466 HyperX FURY x2
- Storage：Adata XPG SX8200Pro 512G
- Power：SUPER FLOWER LEADEX 650W

## BIOS Setting (IMPORTANT)!!!

* Save & Exit → Load Optimized Defaults
* BIOS → Fast Boot → Disabled
* BIOS → CSM Support → Disabled
* BIOS → Secure Boot → Secure Boot Enable -> Disabled
* BIOS → Windows 8/10 Features → Windows 8/10
* Peripherals → Intel Platform Trust Technology (PTT) → Disable
* Peripherals → Software Guard Extensions (SGX) → Disable
* Peripherals → Trusted Computing → Security Device Support →  Disable
* Peripherals → USB Configuration → Legacy USB Support →  Enabled
* Peripherals → USB Configuration → XHCI Hand-off →  Enabled
* Peripherals → Network Stack Configuration → Network Stack →  Disabled
* Peripherals → SATA And RST Configuration → SATA Mode Selection →  AHCI
* Chipset → Vt-d → Disabled
* Chipset → Internal Graphics → Enabled
* Chipset → DVMT Pre-Allocated → 64M
* Chipset → DVMT Total Gfx Mem → MAX 
* Chipset → Audio Controller → Enabled
* Chipset → Above 4G Decoding → Enabled
* Power → Platform Power Management → Disabled
* Power → ErP → Disabled
* Power → RC6 (Render Standby) -> Disabled

I don't find CFG Lock on the BIOS setting, so I set Kernel → Quirks → `AppleXcpmCfgLock` → true
@[***cheneyveron***](https://github.com/cheneyveron) does something for CFG Lock on Gigabyte Motherboard, but I don't understand how to do.

## Software info.

- OS：macOS Big Sur 11.1
- OpenCore version：0.6.4
<!-- - UHD630：Work。DeviceProperties -> Add -> `PciRoot(0x0)/Pci(0x2,0x0)` -> `AAPL,ig-platform-id` → `0300983E`。 -->
- RX570：Work
- Audio：Work
- USB：Work
- Ethernet：Work
- Sleep：Work
- Bootup/Shutdown：Work
- iCloud & App Store & iMessage & FaceTime：You should generate `MLB`, `ROM`, `SystemSerialNumber`, `SystemUUID` in PlatformInfo -> Generic
- AirDrop & HandOff & Continuity：Not Work, because I don't have Bluetoth


## Acknowledgements

- @[***cheneyveron***](https://github.com/cheneyveron): I refer his config about Big Sur with OC 0.6.4 config
- [OpenCore](https://github.com/acidanthera/OpenCorePkg): A famous bootloader for hackintosh