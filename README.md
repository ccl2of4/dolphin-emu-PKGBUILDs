# Before you start

In this repo are two folders for two different packages. They will both install under separate directories in `/opt` so that they do not conflict with each other.

Before installing these packages, you must first make sure you've installed the regular `dolphin-emu` package.

`pacman -S dolphin-emu`

You need this package because it provides the udev rules for the gc adapter (remember these packages will install under `/opt`, so I removed the udev rules from their PKGBUILDs)

Now you can install these packages.

# Installation

To install either of the packages, just use `makepkg`

For example

    cd dolphin-emu-faster-melee
    makepkg -si

# Gecko Codes

For whichever build you decide to use, you must make sure you have "Enable Cheats" checked by going to Config->General.

## Faster Melee (5.0.3)

A file, `GALE01.ini` is provided next to the PKGBUILD. You can either copy it directly to `~/.dolphin-emu/GameSettings` or do the following in dolphin's GUI:

Right click Melee ISO -> properties -> Gecko Codes

* Check Faster Melee Netplay Settings
* Check 60FPS + 4X VRH
* Uncheck everything else

Right click Melee ISO -> properties -> GameConfig

* Uncheck "Half Audio Rate"
* Click "Video Rate Hack" so that it says "4x"

## Netplay (5.0-321)

Right click Melee ISO -> properties -> Gecko Codes

* Netplay Community Settings
* Uncheck everything else

## Beware

You will notice that when you switch between versions it will reset the options you have checked due to them both using the same config file, so if you're ever having issues connecting just double check those options again. Alternatively, you could configure the different installations to run using different config files.
