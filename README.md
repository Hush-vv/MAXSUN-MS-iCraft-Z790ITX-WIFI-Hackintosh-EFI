# MAXSUN MS iCraft Z790ITX WIFI Hackintosh EFI

EFI Partition and Guidelines for my Mini-ITX Hackintosh

![About](./assets/about.png)

## Hardware

- MAXSUN MS iCraft Z790ITX WIFI
- Intel Core i5-13400
- Asgard DDR5 6400CL32 16GBx2 RGB
- YESTON RX6800XT-16GD6
- 2xWD Black SN750 1TB NVMe
- USCORSAIR SF750W
-  WiFi/BT：Intel Wi-Fi6 AX211（BCM943602CS - MacOS 13）

## Config

- SMBIOS - MacPro7,1
- Verbose Off
- Scaled for 4K
- `agdpmod=pikera` is enabled for AMD GPU

## Bios

- VT-d - Enabled
- Above 4G decoding - Enabled
- Intel（VMX）- Enabled
- CFG Lock - Disabled

## AirportItlwm

- Only enabled in Sonoma, remove MinKernel 23.0.0 for other system versions [Problem feedback](https://github.com/OpenIntelWireless/itlwm/issues/883)

<details>
<summary><strong>EFI file content</strong></summary>

## EFI file content

```
EFI
├── BOOT
│   └── BOOTx64.efi
└── OC
    ├── ACPI
    │   ├── SSDT-MS-iCraftZ790ITX.aml (MS iCraft Z790ITX WIFI dedicated ssdt)
    │   ├── SSDT-DTGP.aml
    │   └── SSDT-AMD Radeon Pro W6800X.aml (Activate Type-C port on graphics card and rename graphics card)
    ├── Drivers
    │   ├── HfsPlus.efi
    │   ├── OpenCanopy.efi
    │   ├── OpenHfsPlus.efi
    │   ├── OpenRuntime.efi
    │   ├── ResetNvramEntry.efi  
    │   └── ToggleSipEntry.efi
    ├── Kexts
    │   ├── AGPMInjector.kext
    │   ├── AirportItlwm.kext
    │   ├── AppleALC.kext
    │   ├── CPUFriend.kext    
    │   ├── CPUFriendDataProvider.kext    -Disabled(HWP has been customized using SSDT and does not need to be enabled)
    │   ├── CpuTopologyRebuild.kext    
    │   ├── CpuTscSync.kext    -Disabled
    │   ├── Lilu.kext
    │   ├── LucyRTL8125Ethernet.kext
    │   ├── RadeonSensor.kext
    │   │   └── Contents
    │   │       └── PlugIns
    │   │           └── SMCRadeonGPU.kext 
    │   ├── RestrictEvents.kext
    │   ├── SMCProcessor.kext
    │   ├── SMCSuperIO.kext
    │   ├── USBMap.kext
    │   ├── VirtualSMC.kext
    │   └── WhateverGreen.kext
    ├── OpenCore.efi
    ├── Resources 
    │   ├── Audio
    │   ├── Font
    │   ├── Image
    │   └── Label
    ├── Tools
    │   ├── CleanNvram.efi 
    │   └── OpenShell.efi
    └── config.plist
```
</details>

## Changelog

```

0.2.1 - Adding Intel Network Card Driver for macOS14

0.2.0 - Customized USB port

0.1.1 - initial release

```

![Geekbench](./assets/geekbench.png)

