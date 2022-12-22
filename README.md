# EFI-ASRock-Z390-Phantom-Gaming-ITX
The EFI of Asrock Z390 Phantom Gamming ITX for Hackintosh

# OS Version
- Ventura 13.1

# OpenCore Version
- 0.8.6

![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/ventura_13_sys_about.jpg?raw=true)
![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/ventura_13_sys_info.jpg?raw=true)
![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/tb3_info.jpg?raw=true)
![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/tb3_network.jpg?raw=true)

## Hardware Specification
| Item | Brand | Comment |
| --- | --- | --- |
| CPU | [Intel I5 9600K](https://ark.intel.com/content/www/us/en/ark/products/134896/intel-core-i5-9600k-processor-9m-cache-up-to-4-60-ghz.html) | |
| Mother Board | [Asrock Z390 Phantom Gaming ITX/AC](https://www.asrock.com/MB/Intel/Z390%20Phantom%20Gaming-ITXac/index.asp) | |
| BIOS Version | 4.40C | |
| Memory | 32GB | Kingston DDR4 3200 16GB Single * 2 |
| SSD | [WD Black SN750 NVMe SSD 1TB](https://www.westerndigital.com/products/internal-drives/wd-black-sn750-nvme-ssd) | |
| iGPU | iGPU Intel UHD 630 | |
| Display Card | [Sapphire PULSE RX 5500 XT 8G GDDR6](https://www.sapphiretech.com/en/consumer/pulse-radeon-rx-5500-xt-8g-gddr6) | |
| WiFi/Bluetooth Module | BCM943602CD | |
| PSU | [CORSAIR SF450 SFX](https://www.corsair.com/ww/en/Categories/Products/Power-Supply-Units/SF-Series%E2%84%A2-80-PLUS-Gold-Power-Supplies/p/CP-9020104-NA) | |
| Case | [Smallest One Mini ITX](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.3c192e8dGWPwJN&id=558710712904&_u=gb7ctd3e108) | |
| Monitor | [LG 27UL600 4K HDR400 IPS](https://www.lg.com/hk_en/monitor/lg-27UL600) | DisplayPort Connect |


## Changelog
_22-Dec-2022_
- Upgraded OC version to `0.8.7`
- Upgraedd KEXTs to the latest version
- Supported macOS Ventura 13.1

_21-Nov-2022_
- Upgraded OC version to `0.8.6`
- Upgraedd KEXTs to the latest version
- Supported macOS Ventura 13.0.1

_29-Oct-2022_
- Upgraded OC version to `0.8.5`
- Upgraedd KEXTs to the latest version
- Supported macOS Monterey `12.6.1`

_20-Sep-2022_
- Upgraded OC version to `0.8.4`
- Upgraedd KEXTs to the latest version
- Supported macOS Monterey `12.6`

_05-Aug-2022_
- Upgraded OC version to 0.8.3
- Upgraedd KEXTs to the latest version
- Supported macOS Monterey 12.5.1

_09-Jul-2022_
- Upgraded OC version to 0.8.2
- Upgraedd KEXTs to the latest version

_26-Jun-2022_
- Upgraded OC version to 0.8.1
- Upgraedd KEXTs to the latest version

_19-May-2022_
- Supported macOS Monterey 12.4

_12-May-2022_
- Fixed error message when BIOS booting phase

_21-Apr-2022_
- Upgraded OpenCore to version `0.8.0`
- Upgraded KEXTs

_01-Apr-2022_
- Supports Monterey 12.3.1

_15-Mar-2022_
- Supports Monterey 12.3

_13-Mar-2022_
- Upgraded OpenCore to version `0.7.9`
- Upgraded KEXTs

_26-Feb-2022_
- Upgraded OpenCore to version `0.7.8`
- Upgraded KEXTs
- Supported Monterey 12.2.1

_09-Feb-2022_
- Upgraded OpenCore to version `0.7.8`
- Upgraded KEXTs

_31-Jan-2022_
- Upgraded OpenCore to version `0.7.7`
- Upgraded KEXTs
- Supports Monterey 12.2

_16-Dec-2021_
- Upgraded OpenCore to version `0.7.6`
- Upgraded KEXTs

_18-Nov-2021_
- Upgraded OpenCore to version `0.7.5`
- Upgraded KEXTs

_07-Oct-2021_
- Upgraded OpenCore to version `0.7.4`
- Upgraded KEXTs

_05-Sep-2021_
- Upgraded OpenCore to version `0.7.3`
- Upgraded KEXTs
- Supported macOS 11.6

_27-Feb-2021_
- Supported macOS 11.2.2

_05-Feb-2021_
- Upgraded OpenCore to version `0.6.6`
- Upgraded KEXTs

_08-Jan-2021_
- Upgraded OpenCore to version `0.6.5`
- Upgraded KEXTs
- Enabled Thunderbolt 3 and support hot plug, check tutorial [here](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/enable_tb3.md)

_16-Dec-2020_
- Supported macOS version: `11.1`

_10-Dec-2020_
- Upgraded OpenCore to version `0.6.4`
- Upgraded KEXTs

_05-Dec-2020_
- Support macOS version: 11.0.1

_03-Dec-2020_
- Upgraded OpenCore to version `0.6.3`
- Upgraded KEXTs
- Support macOS version: 10.15.7

_09-Oct-2020_
- Upgraded OpenCore to version `0.6.2`
- Upgraded KEXTs

_15-Sep-2020_
- Upgraded OpenCore to version `0.6.1`
- Upgraded KEXTs

_11-Sep-2020_
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
- Thunderbolt 3: display, charging, data transfer, no devices to verify the Daisy chaining

# Donate a coffee 
![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/donation.png?raw=true)
