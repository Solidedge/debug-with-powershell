# Check toolchain with powershell
Debug a NCS project's toolchain with a powershell script. Check version of applications, software and OS. Print pathways, and connected development kits. This script was used with a BLE-MIDI project, and is therefore tailored for that.

# Disclaimer
It's been a while since I set this up to work, do so at your own risk! You might need to alter the execution policy, which is done by entering "Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass" in your powershell terminal.

# Requirements
This script has only been tested with these requirements:
- Visual Studio Code
- Tools, software and OS listed in Toolchain

# Checks
These checks are tailored for a nRF Connect SDK project, utilizing MIDI via BLE. My recommendation is therefore to tailor this script for your own usage.

## Toolchain
Minimum version is defined by the version a project used when developed. ie: this script was last used for a project that used CMAKE 3.16.2; newer and/or older versions might work, but there is no garantuee. Upgrading/downgrading any tool might affect other tools as well.
Tool | Minimum Version
---- | --------
CMAKE | 3.16.2
West | 0.10.1 
Ninja | 1.10.0 
nRFjprog | 10.12.1 
J-Link | 6.88 
Powershell | 2021.2.2 
Windows | 10.19042 

## Toolchain paths
Prints values for inspection. Undefined values will not print anything.
- GNUARMEMB_TOOLCHAIN_PATH
- ZEPHYR_TOOLCHAIN_VARIANT
- ZEPHYR_BASE
- West manifest
- Zephyr base
- Topdir

## Physical peripherals
Checks for connected devices, lists them and their families.
