# How to enable Thunderbolt 3 of Asrock Z390 Phantom Gaming-ITX/ac for Hackintosh

> IMPORTANCE: In this step, includes flash the custom BIOS firmware and flash the specified firmware of thunderbolt 3 device, I can't guarantee the approcah is 100% successful in your operation, so please take the risk by yourself and no responsibility of me when any exception happened in your operation, please note it.

This solution is reference to Fangf's, please check in details from his blog: [华擎ASRock Z390 Phantom Gaming ITX/ac 雷电3 完美驱动 热插拔](https://blog.fangf.cc/2020/05/19/TB3/), according to the tutorial, flash the specified firmware of thunderbolt 3 have to be operated in Windows OS (I completed in Windows 10).

[TOC]

## Preparation

- Windows OS running on `ASRock Z390 Phantom Gaming ITX/ac` 

## Flash specified BIOS version

Flash the specified BIOS [Z39PGIX4.40C](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/bios/Z39PGIX4.40C), for example by [Instant Flash](https://www.asrock.com/support/BIOSIG.asp?cat=BIOS9).

## Install Thunderbolt 3 device driver

Install thunderbolt 3 device driver by downloading from [Asrock offical website](https://www.asrock.com/mb/Intel/Z390%20Phantom%20Gaming-ITXac/index.asp#Download), then complete the driver's installation.

## BIOS Setting

After the driver of thunderbolt 3 install, resboot the machine.

1. Boot to BIOS setting, and press `F6` to change to `Advance Mode` set: 
   1. `Advanced` -> `Intel(R) Thunderbolt` -> `GPIO3 Force Pwr`: `Enable`
   2. `Advanced` -> `Intel(R) Thunderbolt` -> `Thunderbolt USB support`: `Enable`
2. Reboot to Windows

## Flash the specificied firmware version of Thunderbolt 3 device

1. Reboot and boot to `Windows OS`, this step is flash the firmware of thunderbolt 3 drvice, download the tools zip file [FwUpdateTool(v1.0.4)(44)](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/tools/TB3/FwUpdateTool_v1.0.4_44.zip), unzip the file, and run the firmware update tool `FwUpdateTool.exe`, then select firmware file `ASROCK_Z390_PG_ITX_ac_LP_HR_2C_A1_rev20_TI_170628_noUVP_CNL.BIN` to update the firmware, this update step will take around 1 minute.
2. After flashed the firmware of thunderbolt 3 device, shut down the machine, unplug-in the power cable of the machine, and press the switch of the power supplier to change to `G3` mode for 1 minute.



## Add SSDTs

### Add `SSDT-DTPG.aml` 

Restart machine and boot to Hackintosh. Put [SSDT-DTPG.aml](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/tools/SSDT-DTPG.aml) to the `ACPI` folder of OC: `EFI -> OC -> ACPI`

### Add Thunderbolt 3 SSDT

1. Open `IORegistryExplorer` and search keyword `rp21`, then check the result as below.

   1. If `dc` got, please put [SSDT-TbtOnPch_PINI.aml](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/tools/SSDT-TbtOnPch_PINI.aml) to the folder `EFI -> OC -> ACPI`

   2. If `D8` got, please put [SSDT-TbtOnPch_PINI_D8.aml](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/tools/SSDT-TbtOnPch_PINI_D8.aml) to the folder ``EFI -> OC -> ACPI`
      ![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/ioregistry_search.jpg?raw=true)

### Configure `config.plist`

#### ACPI section

Configure `config.plist` and add `SSDT-DTPG.aml` and `SSDT-TbtOnPch_PINI.aml`/ or `SSDT-TbtOnPch_PINI_D8.aml` to the `ACPI` section and enable them.

![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/ssdt_setting.jpg?raw=true)

#### Add patch of ACPI section: rename `_E2C` to `XE2C`

Add a new patch record in `ACPI -> Patch` of `config.plist`:

```
Find: 5F453243
Replace: 58453243
Comment: change _E2C to XE2C for TB hotplug
Enabled: true
```

![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/patch_of_acpi_tb3.jpg?raw=true)

## Enjoy the Thunderbolt 3 

Reboot the machine with clear NVRAM cache, done!

Enjoy the thunerbolt 3 in Hackintosh.

![](https://github.com/ansonliao/EFI-ASRock-Z390-Phantom-Gaming-ITX/blob/master/images/tb3_info.jpg?raw=true)

## Advantages of thunderbolt 3

- In my case, I connect my `HHKB` keyboard to the thunderbolt 3 port, the keyboard is available immediately when my Hackintosh is wake up. Before when this keyboard connects to the `USB` port of the back panel of the mother board, have to wait some seconds (such as 10 seconds) for available from the machine is wake up.