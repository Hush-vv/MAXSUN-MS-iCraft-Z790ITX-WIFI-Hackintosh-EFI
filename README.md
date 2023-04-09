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
- DW1820a WiFi/BT

## Config

- SMBIOS - MacPro7,1
- Verbose Off
- Scaled for 4K
- `agdpmod=pikera` is enabled for AMD GPU

## Bios

- CFG-Lock - off
- Fast Boot - off
- VT-d - off
- CSM - off
- VT-x - on
- Above 4G decoding - on
- Re-Size BAR Support - on
- XHCI Hand-off - on

## Overclocking

- VCore: Fixed 1.28V
- DVID: -0.045
- LLC: 3
- P 0-1: 50
- P 2-7: 49
- E 0-3: 39


## Changelog

```

0.1.1 - initial release

```

![Geekbench](./assets/geekbench.png)

