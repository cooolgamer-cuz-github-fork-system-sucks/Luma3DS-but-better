# Starlight3DS
*Nintendo 3DS "Custom Firmware"*

## What it is
**Starlight3DS** is an unofficial fork of [Luma3DS](https://github.com/LumaTeam/Luma3DS) with more features, this is a continuation of [DullPointer's luma fork](https://github.com/DullPointer/Luma3DS) where most features are taken from it and made compatible for the latest Luma3DS version at the time of writing this.
There's also some features taken from other luma forks as well and some that I added myself. Please check the [credits](https://github.com/cooolgamorg/Starlight3DS?tab=readme-ov-file#credits) to see people who made this fork possible!

Starlight3DS requires a full-system persisent exploit such as [boot9strap](https://github.com/SciresM/boot9strap) to run.

## Changes with the official build
Note: The config file is different from the original luma3DS, it's "configplus.ini" instead of "config.ini" to avoid conflicts if you want to switch between this modified version and the official one (like for playing CTGP-7 for example).

- Changed auto-copy to ctrnand and essential backup checks to be less annoying
- Restored UNITINFO and enable rosalina on safe_firm options on the luma config menu (TWL patch option is now with "enable external firms and modules")
- Removed the need of having both "Game Patching" and "External Firms and Modules" enabled for patching sysmodules, just "External Firms and Modules" need to be enabled
- Added shortcuts:
  - Press start + select to toggle bottom screen (nice when you watch videos) inspired by [This](https://github.com/DullPointer/Luma3DS/commit/9fea831656446cbaa2b5b4f6364407bb1b35dee7)
  - Press A + B + X + Y + Start to instantly reboot the console. Useful in case of freeze, but can corrupt your sdcard. This is why this option is now hidden in the `config.ini` file
  - Press Start on Rosalina menu to toggle wifi -> [Original](https://github.com/DullPointer/Luma3DS/commit/c1a20558bed3d792d54069719a898006af20ba85)
  - Press Select on Rosalina menu to toggle LEDs -> [Original](https://github.com/DullPointer/Luma3DS/commit/fa70d374c00e39dee8b9ef54f60deb1da35a0c51) (and press Y to force blue led as a workaround when the battery is low)
- Added [Extra Config menu](https://github.com/DullPointer/Luma3DS/commit/174ed486ab59bd249488c9035682fa7d058d1e80) including:
  - Automatically suppress LEDs
  - Cut power to TWL Flashcards allowing to save battery
  - Home button opens Rosalina
  - start + select shortcut to toggle top/bottom screen (enabled on bottom screen by default)
- Added Day and Night mode (lite):
  - You can choose the screen brightness
  - You can choose to turn on or off LEDs
  - Those will be applied at a desired time
- Added n3ds clock + L2 status in rosalina menu -> [Original](https://github.com/DullPointer/Luma3DS/commit/2dbfa8b5c9b719b7f3056691f54332f42da6de8d)
- Added Software Volume Control -> (now merged with the official luma3ds one)
- Added extended brightness presets and per-screen brightness -> [Original](https://github.com/DullPointer/Luma3DS/commit/83e8d471a377bc6960fae00d6694f5fe86dcca42) WARNING: a little broken and can exceed the limits!
- Added permanent brightness calibration -> [Original](https://github.com/DullPointer/Luma3DS/commit/0e67a667077f601680f74ddc10ef88a799a5a7ad)
- Added a option to cut wifi while in sleep mode allowing to save battery -> [Original](https://github.com/DullPointer/Luma3DS/commit/174ed486ab59bd249488c9035682fa7d058d1e80)
- Added the ability to redirect layeredFS path -> [Original](https://github.com/DeathChaos25/Luma3DS/commit/8f68d0a19d2ed80fb41bbe8499cb2b7b027e8a8c)
- Added loading of custom logo while launching a app from luma/logo.bin  -> [Original](https://github.com/Pixel-Pop/Luma3DS/commit/d225d9fa507dcccce3a6c86d0a38f7998f39b7a2)
- Added loading of external decrypted otp from luma/otp.bin -> [Original](https://github.com/truedread/Luma3DS/commit/aa395a5910113b991e6ad7edc3415152be9bbb03#diff-ef6e6ba78a0250ac4b86068018f17d423fe816bb00fb3b550725f1cb6f983d29)
- Changed colors on config menu because why not
- Continue running after a errdisp error happens, this is the same option as instant reboot because they kinda go together (you decide when to reboot after an error occur)
- Added play coin maximize to rosalina menu -> [Original](https://github.com/Gruetzig/Luma3DS/commit/1e329b55dade61ba74a0bb1cc6e59d2504d0bde1)
- Plugin Selector -> [Original](https://github.com/Tekito-256/Luma3DS)

## Compiling

To build Starlight3DS:
1. Get the prerequites:
* git
* up-to-date devkitARM and libctru
* [makerom](https://github.com/jakcron/Project_CTR) in PATH
* [firmtool](https://github.com/TuxSH/firmtool) installed
2. Clone the repository with `git clone https://github.com/cooolgamorg/Starlight3DS.git`
3. Run `make`.

The produced `boot.firm` is meant to be copied to the root of your SD card for usage with Boot9Strap.

## Setup / Usage / Features
See https://github.com/LumaTeam/Luma3DS/wiki (needs rework)

## Credits
See https://github.com/LumaTeam/Luma3DS/wiki/Credits for original Luma3DS credits

People who made this fork possible:
- [DullPointer](https://github.com/DullPointer)
- Sono
- Nutez
- [cooolgamer](https://github.com/cooolgamer)
- [DeathChaos25](https://github.com/DeathChaos25)
- [truedread](https://github.com/truedread)
- [Gruetzig](https://github.com/Gruetzig)
- [Tekito-256](https://github.com/Tekito-256)
- [exalented](https://github.com/exalented)
- [Alexyo21](https://github.com/Alexyo21)
- [Pixel-Pop](https://github.com/Pixel-Pop)

## Licensing
This software is licensed under the terms of the GPLv3. You can find a copy of the license in the LICENSE.txt file.

Files in the GDB stub are instead triple-licensed as MIT or "GPLv2 or any later version", in which case it's specified in the file header.

By contributing to this repository, you agree to license your changes to the project's owners.
