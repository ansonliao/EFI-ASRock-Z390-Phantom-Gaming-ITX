# EFI-ASRock-Z390-Phantom-Gaming-ITX
The EFI of Asrock Z390 Phantom Gamming ITX for Hackintosh

Clover built by: ![t_logo](https://user-images.githubusercontent.com/6239630/73442546-179b4b80-4366-11ea-9a1e-1e96102aa86c.png) @hackintosh_by 

# OS Version
- Catalina 10.15.6

# OpenCore Version
- 0.6.0

![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/migrate_to_oc/images/oc_catalina_10.15.6.jpg?raw=true)

## Hardware Specification
| Item | Brand | Comment |
| --- | --- | --- |
| CPU | [Intel I5 9600K](https://ark.intel.com/content/www/us/en/ark/products/134896/intel-core-i5-9600k-processor-9m-cache-up-to-4-60-ghz.html) | |
| Mother Board | [Asrock Z390 Phantom Gaming ITX/AC](https://www.asrock.com/MB/Intel/Z390%20Phantom%20Gaming-ITXac/index.asp) | |
| BIOS Version | 4.0 | |
| Memory | Kingston DDR4 3200 16GB Single | |
| SSD | [WD Black SN750 NVMe SSD 1TB](https://www.westerndigital.com/products/internal-drives/wd-black-sn750-nvme-ssd) | |
| iGPU | iGPU Intel UHD 630 | |
| Display Card | [Sapphire PULSE RX 5500 XT 8G GDDR6](https://www.sapphiretech.com/en/consumer/pulse-radeon-rx-5500-xt-8g-gddr6) | |
| WiFi/Bluetooth Module | BCM943602CD | |
| PSU | [CORSAIR SF450 SFX](https://www.corsair.com/ww/en/Categories/Products/Power-Supply-Units/SF-Series%E2%84%A2-80-PLUS-Gold-Power-Supplies/p/CP-9020104-NA) | |
| Case | [Smallest One Mini ITX](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.3c192e8dGWPwJN&id=558710712904&_u=gb7ctd3e108) | |
| Monitor | [LG 27UL600 4K HDR400 IPS](https://www.lg.com/hk_en/monitor/lg-27UL600) | DisplayPort Connect |


## Changelog
_21-Sep-2020_
- Migrated to OpenCore 0.6.0
- Clover version will be dropped
- Removed `AirportBrcmFixup.kext` as `BCM943602CD` no need any patch (`BCM94360CS2` also don't need any bluetooth KEXT patch)
- Updated KEXTs
- Changed WiFi/bluetooth module to `BCM943602CD`

_21-Jul-2020_
- Upgraded macOS to 10.15.6
- Clover bootloader version: v5.0 r5114
- Updated `AirportBrcmFixup.kext` to the latest version `2.0.7`
- Added bluetooth patches for WiFi/Bluetooth card `BCM94360CS2`, if your bluetooth is works fine, maybe you need to remove these 3 patches `BrcmBluetoothInjector.kext`, `BrcmFirmwareData.kext`, `BrcmPatchRAM3.kext` from `EFI->CLOVER->kext-Other`, please refer to: https://github.com/acidanthera/BrcmPatchRAM

_27-Apr-2020_
- Works with Clover bootloader version: v5.0 r5114
- Updated to support Catalina 10.15.4
- Updated some KEXTs, WhateverGreen, Lilu
- Didn't updated AppleALC.kext to version `1.4.8`, as my case is after upgrade AppleALC to version `1.4.8`, audio layout ID `11` out of work to drive built-in audio devices of MB, tries others some layout IDs of ALC1220, but failed, if anyone have solution, please create issue let me known, thanks.

# What Works
- WiFi, Bluetooth
- iServices: Airdrop, iMessage, App Store, Handoff, etc.
- USB
- Ethernet
- Audio card
- Sleep, wake up
- Onboard DP port, HDMI port

# What Broken:
- Thunderbolt 3 maybe out of work, I didn't pay much time on this
