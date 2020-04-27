# EFI-ASRock-Z390-Phantom-Gaming-ITX
The EFI of Asrock Z390 Phantom Gamming ITX for Hackintosh

It built by: ![t_logo](https://user-images.githubusercontent.com/6239630/73442546-179b4b80-4366-11ea-9a1e-1e96102aa86c.png) @hackintosh_by 

## Hardware Specification
| Item | Brand | Comment |
| --- | --- | --- |
| CPU | Intel I5 9600K | |
| Mother Board | Asrock Z390 Phantom Gaming ITX/AC | |
| BIOS Version | 4.0 | |
| Memory | Kingston DDR4 3200 16GB Single | |
| SSD | Intel 760P 512GB, M.2, NVMe 2280 | |
| iGPU | iGPU Intel UHD 630 | |
| Display Card | No | Only iGPU of CPU |
| WiFi/Bluetooth Module | BCM94360CS2 | |
| PSU | CORSAIR SF450 SFX | No display card, no need more powerful PSU to support |
| Case | [ Smallest One Mini ITX](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.3c192e8dGWPwJN&id=558710712904&_u=gb7ctd3e108) | |
| Monitor | LG 27UL600 4K HDR400 IPS | DisplayPort Connect |


## Updates:

### 27-Apr-2020
- Works with Clover bootloader version: v5.0 r5114
- Updated to support Catalina 10.15.4
- Updated some KEXTs, WhateverGreen, Lilu
- Didn't updated AppleALC.kext to version `1.4.8`, as my case is after upgrade AppleALC to version `1.4.8`, audio layout ID `11` out of work to drive built-in audio devices of MB, tries others some layout IDs of ALC1220, but failed, if anyone have solution, please create issue let me known, thanks.
