# HP-Elitebook-x360-1030-G3-Hackintosh
## My EFI folder

# ALWAYS USE YOUR OWN SSDTs! CREATE THEM USING [SSDTTime](https://github.com/corpnewt/SSDTTime)

## Working:
- Wifi
- Touchscreen
- All USB ports (not Thunderbolt just USB-C)
- Apple Services (your results may vary but mine works)

## Not working:
- Bluetooth (config.plist issue I never fixed)
- Camera

Runs macOS Ventura.
EFI is currently OpenCore 1.0.1

All kexts were their latest versions as of Sep 2, 2024.

My laptop kicked the bucket a few weeks ago, so I will not be updating it any further.


## BIOS

### Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(This must be off, if you can't find the option like me, enable AppleXcpmCfgLock under Kernel -> Quirks. Your hack will NOT boot with CFG-Lock enabled)

### Enable

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI

### If available:
- Virtualization Technology (VTx) - Yes
- Virtualization Technology for Directed I/O (VTd) - Yes
- Video Memory Size - 64 MB
- Intel Management Enginge (ME) - Yes


Credit to [yingw on Github](https://github.com/yingw/HP-Elitebook-X360-1030-G3-Hackintosh/) for his BIOS settings list :)
