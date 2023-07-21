# Luma3DS
*Noob-proof (N)3DS "Custom Firmware"*

### What it is
**Luma3DS** is a program to patch the system software of (New) Nintendo (2)3DS handheld consoles "on the fly", adding features such as per-game language settings, debugging capabilities for developers, and removing restrictions enforced by Nintendo such as the region lock.

It also allows you to run unauthorized ("homebrew") content by removing signature checks.
To use it, you will need a console capable of running homebrew software on the Arm9 processor.

Since v8.0, Luma3DS has its own in-game menu, triggerable by <kbd>L+Down+Select</kbd> (see the [release notes](https://github.com/LumaTeam/Luma3DS/releases/tag/v8.0)).

## Changes with the official build
### Note: This build is meant to be used by advanced users
### Note 2: some features are taken from [DullPointer's luma fork](https://github.com/DullPointer/Luma3DS)
- Removed auto-copy to ctrnand and creating essential files backup
- Restored UNITINFO and enable rosalina on safe_firm options on the luma config menu (TWL patch option is now with "enable external firms and modules")
- Added shortcuts:
  - Press start + select to toggle bottom screen (nice when you watch videos)
  - Press A + B + X + Y + Start to instantly reboot the console. Useful in case of freeze, but don't complain if your sdcard get corrupted because of this.
  - Press Start on Rosalina menu to toggle wifi
  - Press Select on Rosalina menu to toggle LEDs (and press Y to force blue led as a workaround when the battery is low)
- Added permanent brightness calibration by Nutez
- Changed colors on config menu because why not
- Continue running after a errdisp error happens (you can press the instant reboot combo to reboot if nothing works)
#
### Compiling
* Prerequisites
    1. git
    2. [makerom](https://github.com/jakcron/Project_CTR) in PATH
    3. [firmtool](https://github.com/TuxSH/firmtool)
    4. Up-to-date devkitARM+libctru
1. Clone the repository with `git clone https://github.com/LumaTeam/Luma3DS.git`
2. Run `make`.

    The produced `boot.firm` is meant to be copied to the root of your SD card for usage with Boot9Strap.

#
### Setup / Usage / Features
See https://github.com/LumaTeam/Luma3DS/wiki

#
### Credits
See https://github.com/LumaTeam/Luma3DS/wiki/Credits

#
### Licensing
This software is licensed under the terms of the GPLv3. You can find a copy of the license in the LICENSE.txt file.

Files in the GDB stub are instead triple-licensed as MIT or "GPLv2 or any later version", in which case it's specified in the file header.
