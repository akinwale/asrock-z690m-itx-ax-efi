# ASRock Z690M-ITX/ax EFI
EFI for the ASRock Z690M-ITX/ax with OpenCore 0.9.9.

* **BIOS Version:** 17.04
* **macOS Version:** Sonoma 14.4.1
* **Processor:** i5-14400F

## Kexts
* AirportItlwm.kext
* AppleALC.kext
* BlueToolFixup.kext
* CpuTopologyRebuild.kext
* IntelBTPatcher.kext
* IntelBluetoothFirmware.kext
* IntelMausi.kext
* Lilu.kext
* LucyRTL8125Ethernet.kext
* RestrictEvents.kext
* SMCProcessor.kext
* SMCSuperIO.kext
* USBPorts.kext
* VirtualSMC.kext
* WhateverGreen.kext
* XHCI-unsupported.kext

## Notes
* Add `-v` to boot args for verbose boot.
* Remember to run GenSMBIOS on the `config.plist` file.

## Current Status
* Boots.
* Audio works.
* Bluetooth works.
* Wi-Fi works.
* Ethernet works.

## USB Port Mapping
Ports mapped using Hackintool. The system case is a Velka 7 case with no front panel I/O, so every rear port is functional. All 14 ports are listed below.

| Port | Description                                         |
|------|-----------------------------------------------------|
| HS04 | USB 2 port (black)                                  |
| HS05 |                                                     |
| HS06 | USB Type-C port with a USB2 device connected        |
| HS07 |                                                     |
| HS08 | BIOS Flashback USB port                             |
| HS09 |                                                     |
| HS10 |                                                     |
| HS13 | LED Controller                                     |
| HS14 | IOUSBHostDevice (Bluetooth)                         |
| SS01 | USB Type-C port with a USB3 device connected        |
| SS02 |                                                     |
| SS03 |                                                     |
| SS04 |                                                     |
| SS05 |                                                     |

## BIOS Settings

### Enabled
| Setting                        | Where?                           |
| ------------------------------ | -------------------------------- |
| Above 4G Decoding              | Advanced \ Chipset Configuration |
| C.A.M. Clever Access Memory*   | Advanced \ Chipset Configuration |
| VT-d                           | Advanced \ Chipset Configuration |
| Intel Virtualization Techology | Advanced \ CPU Configuration     |
| SATA Mode Selection: AHCI      | Advanced \ Storage Configuration | 
| XHCI Hand-off                  | Advanced \ USB Configuration     |

\* Clever Access Memory refers to Resizable BAR

### Disabled
| Setting              | Where?                       |
| -------------------- | ---------------------------- |
| CFG Lock**           | Advanced \ CPU Configuration |
| CSM                  | Boot                         |
| Fast Boot            | Boot                         |
| Intel Platform Trust | Security                     |
| Secure Boot          | Security                     |

\** Can be found after enabling **CPU C States Support**.

## Hardware
| Component        | Model                                             |
| ---------------- | ------------------------------------------------- |
| CPU              | Intel Core i5-14400F                              |
| Motherboard      | ASRock Z690M-ITX/ax                               |
| RAM              | 32GB (2 x 16GB) G.SKILL Ripjaws V DDR4 @ 2400MT/s |
| GPU              | ASRock AMD Radeon RX 6600 Challenger D 8GB        |
| OS Drive         | TEAMGROUP MP44L 500GB                             |
| Audio            | Realtek ALC897                                    |
| WiFi / Bluetooth | Intel Wi-Fi 6E AX211                              |
