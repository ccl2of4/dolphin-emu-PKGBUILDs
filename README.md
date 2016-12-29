# Before you start

In this repo are three folders for three different packages. They will all install under separate directories in `/opt` so that they do not conflict with each other.

Before installing these packages, you must first make sure you've installed the regular `dolphin-emu` package.

`pacman -S dolphin-emu`

You need this package because it provides the udev rules for the gc adapter (remember these packages will install under `/opt`, so I removed the udev rules from their PKGBUILDs)

Now you can install all of these packages.

# Installation

To install any of the packages, just use `makepkg`

For example

    cd dolphin-emu-faster-melee-4.3
    makepkg -si

# Gecko Codes

## Faster Melee (4.3 and 4.4)

A file, `GALE01.ini` is provided next to the PKGBUILD. You can either copy it directly to `~/.dolphin-emu/GameSettings` or do the following in dolphin's GUI:

Right click Melee ISO -> properties -> Gecko Codes

* Check Faster Melee Netplay Settings
* Check 60FPS + 4X VRH
* Uncheck everything else

Right click Melee ISO -> properties -> GameConfig

* Uncheck "Half Audio Rate"
* Click "Video Rate Hack" so that it says "4x"

## Netplay 5.0-321

Right click Melee ISO -> properties -> Gecko Codes

* Netplay Community Settings
* Uncheck everything else

## Beware

You will notice that when you switch between versions it will reset the options you have checked, so if you're ever having issues connecting just double check those options again.
