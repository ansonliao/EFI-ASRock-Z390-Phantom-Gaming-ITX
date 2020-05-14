# EFI-ASRock-Z390-Phantom-Gaming-ITX
The EFI of Asrock Z390 Phantom Gamming ITX for Hackintosh

It built by: ![t_logo](https://user-images.githubusercontent.com/6239630/73442546-179b4b80-4366-11ea-9a1e-1e96102aa86c.png) @hackintosh_by 

## Hardware Specification
| Item | Brand | Comment |
| --- | --- | --- |
| CPU | [Intel I5 9600K](https://ark.intel.com/content/www/us/en/ark/products/134896/intel-core-i5-9600k-processor-9m-cache-up-to-4-60-ghz.html) | |
| Mother Board | [Asrock Z390 Phantom Gaming ITX/AC](https://www.asrock.com/mb/Intel/Z390%20Phantom%20Gaming-ITXac/index.asp) | |
| BIOS Version Of MB | 4.2 | |
| Memory | Kingston DDR4 3200 16GB Single | |
| SSD | Intel 760P 512GB, M.2, NVMe 2280 | |
| iGPU | Intel UHD 630 | |
| Display Card | [Sapphire PULSE RX 5500 XT 8G GDDR6](https://www.sapphiretech.com/en/consumer/pulse-radeon-rx-5500-xt-8g-gddr6) | |
| WiFi/Bluetooth Module | BCM94360CS2 | |
| PSU | CORSAIR SF450 SFX | |
| Case | [ Smallest One Mini ITX](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.3c192e8dGWPwJN&id=558710712904&_u=gb7ctd3e108) | |
| Monitor | [LG 27UL600 4K HDR400 IPS](https://www.lg.com/us/monitors/lg-27UL600-W-4k-uhd-led-monitor) | DisplayPort Connect (version 1.2) |


## Updates:

### 14-May-2020
- New eGPU introduced: [Sapphire PULSE RX 5500 XT 8G GDDR6](https://www.sapphiretech.com/en/consumer/pulse-radeon-rx-5500-xt-8g-gddr6)
- Updated Mac machine model to `iMac 19,1` as new eGPU introduced
- Updated some kexts
- Updated `config.plist` to support new hardware introduced

### 27-Apr-2020
- Works with Clover bootloader version: v5.0 r5114
- Updated to support Catalina 10.15.4
- Updated some KEXTs, WhateverGreen, Lilu
- Didn't updated AppleALC.kext to version `1.4.8`, as my case is after upgrade AppleALC to version `1.4.8`, audio layout ID `11` out of work to drive built-in audio devices of MB, tries others some layout IDs of ALC1220, but failed, if anyone have solution, please create issue let me known, thanks.
