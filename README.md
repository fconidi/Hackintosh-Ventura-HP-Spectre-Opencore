# Hackintosh-Ventura-HP-Spectre-Opencore
 
Hackintosh Ventura on HP Spectre 13 v102nl Opencore


**Status: (Active)** <br>
**Current version: Ventura 13.6.3**

[![OpenCore](https://img.shields.io/badge/OpenCore-0.9.7-blue.svg)](https://github.com/acidanthera/OpenCorePkg)

## Introduction

**DISCLAIMER:**
Read the entire [Dortania](https://dortania.github.io/OpenCore-Install-Guide) guide before you start. I'm not responsible for any damage.

<details>
<summary>
    <strong>Hardware configuration</strong>
</summary>

### **HP Spectre v-102nl**


[![HP](https://img.shields.io/badge/HP-Specs-red.svg)](https://support.hp.com/gb-en/document/c05300954) [![OpenCore](https://img.shields.io/badge/HP-Support-blue.svg)](https://support.hp.com/gb-en/drivers/hp-spectre-13-v100-notebook-pc/model/13190976/)




 | Component       | Manufacturer and model                                | Additional description           |
 | --------------- | ----------------------------------------------------- | -------------------------------- |
 | CPU             | Intel Core i7-7500U (7th gen - Kaby Lake)      |                                  |
 | GPU             | Intel HD Graphics 620                                |                                  |
 | Screen          | 13.3" FHD IPS UWVA (1920 x 1080)                |                                  |
 | RAM             | 8 GB LPDDR3-1866 SDRAM                                   |                               |
 | SSD Primary     | 512 GB Toshiba NVMe™ M.2 SSD |Disk for Windows macOS and SysLinuxOS|       
 | Audio           | Conexant CX8200 (0x2008)                                        |                                  |
 | Wireless        | Intel Wireless AC 8260                             |                                                                    |
 
</details>  


<details>
<summary>
    <strong>UEFI drivers</strong>
</summary>

|     Driver      | Version           |
| :-------------: | :---------------: |
| HfsPlus.efi | OpenCorePkg 0.9.7 |
| OpenCanopy.efi  | OpenCorePkg 0.9.7 |
| OpenRuntime.efi | OpenCorePkg 0.9.7 |

</details>

<details>
<summary>
    <strong>Neofetch screenshot</strong>
</summary>

<img src="https://github.com/fconidi/Hackintosh-Ventura-HP-Spectre-Opencore/blob/main/neofetch.png" alt="Neofetch screenshot" width="100%"/>

</details>

## Recommended UEFI/BIOS settings

<details>  
<summary>
    <strong>UEFI/BIOS Setup</strong>
</summary>

<summary>
    <strong>Security</strong>
</summary>

- `Intel Software Guard Extensions (SGX) -> Disabled`
- `TPM Device -> Disabled`

<summary>
    <strong>Configuration</strong>
</summary>

- `Virtualization Technology -> Enabled`
- `Hyper-Threading -> Enabled`

<summary>
    <strong>Boot Options</strong>
</summary>

- `Legacy Support -> Disabled`
- `Secure Boot -> Disabled`

</details>


## Configuration advices (config.plist)

You can find configuration guide for Kaby Lake laptops on [dortania.github.io](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/kaby-lake.html) site.


</details>

<details>
<summary>
    <strong>PlatformInfo</strong>
</summary>

    Automatic -> True
    CustomMemory -> False
    UpdateDataHub -> True
    UpdateNVRAM -> True
    UpdateSMBIOS -> True
    UpdateSMBIOSMode -> Create
    UseRawUuidEncoding -> False

- **Generic**
  - `AdviseFeatures -> False`
  - `MaxBIOSVersion -> False`
  - `SpoofVendor -> True`
  - `ProcessorType -> 1793`
  - `SystemMemoryStatus -> Auto`

 **Note**: You need to generate your own values for `SystemProductName`, `SystemSerialNumber`, `MLB`, `ROM` and `SystemUUID` using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS).
 I'm using SMBIOS for MacBookPro14.1.

</details>

   **Note**: For `boot-args` We need `-igfxblr` flag to prevent black screen on system loading screen.


## Status


<details>  
<summary>
    <strong>Working ✅</strong>
</summary>

- `App Store`
- `Audio` - Realtek ALC285 with sound keys (F7 and F8)
- `Brightness Keys` 
- `Battery` (management, percentage and actual work time)
- `Bluetooth and Wi-Fi` - Intel Wireless-AC 7160
- `CPU power management / performance`
- `Keyboard`
- `IGPU Intel HD 620`
- `Internal microphone`
- `SATA SSD / NVMe support`
- `Shutdown / Reboot functions`
- `Sleep/Wake` 
- `Speakers and headphones combo jack`
- `System updates` 
- `Touchpad`
- `USB Ports`
- `Web camera`
- `iMessage`
- `FaceTime`
- `iTunes Store`
  
</details>



<details>  
<summary>
    <strong>rEFInd Boot Manager </strong>
</summary>

I use 4 different OS on my laptop (macOS, Windows 11, SysLinuxOS, Debian)
and it's necessary for me to select proper system to work on every boot.
So I decided to use rEFInd Boot Manager
</details>

## Credits

<summary>
    <strong>Thanks to:</strong>
</summary>

- [Apple](https://www.apple.com) 
- [Acidanthera](https://github.com/acidanthera) team - for OpenCore and necessary kernel extensions
- [CorpNewt](https://github.com/corpnewt) and [headkaze](https://github.com/headkaze/Hackintool) - for useful tools to install and configure system
- [Dortania](https://github.com/dortania) team - for great Hackintosh tutorials
- [OpenIntelWireless](https://github.com/OpenIntelWireless) team - for enable of laptop default Intel Wireless Wi-Fi card.
- [Mieze](https://github.com/Mieze/RTL8111_driver_for_OS_X/releases) - for enable of laptop default Realtek sound card
- [VoodooI2C](https://github.com/VoodooI2C) team - for enable of laptop keyboard
- [Olarila](https://olarila.com) -  for great Hackintosh work, tutorial, images and EFI folder
- [KrolSeb](https://github.com/KrolSeb) -  for great Hackintosh README that was my inspiration for this document
- ... and the rest of not mentioned people who works on Hackintosh project :)
