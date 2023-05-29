# PatchBoot
This repository provides a guide for patching [AMI Aptio V UEFI firmware](https://www.ami.com/bios-uefi-utilities/) to circumvent [Secure Boot](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-secure-boot) checks and allow loading of unsigned executables.

## Disclamer
Flashing modified firmware onto your motherboard carries the risk of damaging it. On certain motherboards, **this damage could be irreparable**. Please proceed with caution - you have been warned.

## Reasons for patching
I use a single computer for both gaming and development, and my daily drivers are Arch Linux (yes, I felt the need to mention it) and Windows 10 LTSC. The issue is that certain intrusive anti-cheat systems require Secure Boot to be enabled. Though dual-booting with Secure Boot on is technically possible, it's an incredibly tedious process (and I would need to use different bootloader). So, I decided to straight up patch the firmware. I've [previously attempted simpler solutions](https://github.com/SamuelTulach/SecureFakePkg), but these anti-cheat systems have already adapted to detect and block such methods, preventing me from playing.

## Detection vectors