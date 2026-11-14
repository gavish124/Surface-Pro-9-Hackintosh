# Surface-Pro-9-Hackintosh
macOS on the Microsoft Surface Pro 9 with patches

<img width="1440" height="960" alt="Screenshot 2026-11-13 at 10 11 16 PM" src="https://github.com/user-attachments/assets/8035b2b3-3932-47b2-aec1-91fca433ccf4" />



## Changelog

 - 11/11/26 - Create repo
 - 11/13/26 - Update WhateverXe kext to [patched 0.8.2](https://github.com/gavish124/WhateverXe) (made by me). Replace BigSurface kext with [WIP kext](https://github.com/Lulurala3119/BigSurface-for-Surface-Laptop-5) optimized for Surface Laptop 5 thanks to [Lulurala3119](https://github.com/Lulurala3119)

## Tested macOS versions

 - macOS 26.7.1

## Additional Notes

[](https://github.com/jlempen/Surface-Laptop-3-OpenCore#recommendations)

Please be aware that all  `PlatformInfo`  and  `SMBIOS`  information was removed from the  `config.plist` file. You will need to generate your own  `PlatformInfo`  with  [CorpNewt's GenSMBIOS tool](https://github.com/corpnewt/GenSMBIOS)  before installing macOS with this repo's EFI folder.

The `AirportItlwm` kext in this repo's EFI folder is [Laobamac's patched AirportItlwm kext](https://github.com/laobamac/itlwm) for macOS Tahoe. If you are installing macOS Sequoia, please use the patched `AirportItlwm` kext for Sequoia.


<details>  
<summary>What works</summary>
 
## What works
 
 - GPU Acceleration via patched `WhateverXe` kext
 - Brightness slider via patched `SSDT_PNLF` aml

 </details>

<details>  
<summary>What needs some more work</summary>
 
## What needs some more work
 
 - Surface exclusive hardware (i.e. power & volume buttons, type cover hotswap, trackpad)
 - GPU issues (i.e. cursor artifacting, video playback issues on Safari, 120 Hz issues)
 - USB mapping

 </details>

<details>  
<summary>Issues when using 120 Hz</summary>
 
## Issues when using 120 Hz
 
At the moment, switching to 120 Hz is not working well as the display fails to initialize with 120 Hz with acceleration, but has no problem initializing at 60 Hz and changing to 120 Hz after boot, or booting 120 Hz without acceleration via the `-wex-no-accel` boot-arg.

 </details>

<details>  
<summary>Related repositories</summary>
 
 - [jlempen/Surface-Laptop-3-OpenCore](https://github.com/jlempen/Surface-Laptop-3-OpenCore)
 - [retropineaple/whateverxe-hp-envy-x360](https://github.com/retropineaple/whateverxe-hp-envy-x360)
 - [b00t0x/WhateverXe](https://github.com/b00t0x/WhateverXe)
 - [wsl540777/Tahoe-Theme-for-OpenCore](https://github.com/wsl540777/Tahoe-Theme-for-OpenCore)

 </details>
 
