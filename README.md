# Before you start

In this repo are three folders for three different packages. They will all install under separate directories in `/opt` so that they do not conflict with each other.

Before installing these packages, you must first make sure you've install the regular `dolphin-emu` package.

`pacman -S dolphin-emu`

You need this package because it provides the udev rules for the gc adapter (remember these packages will install under `/opt`, so I removed the udev rules from their PKGBUILDs)

Now you can install all of these packages.

# Installation

To install any of the packages, just use `makepkg`

For example

    cd dolphin-emu-faster-melee-4.3
    makepkg -si

# Gecko Codes

I'm not 100% sure what's all is required here, but I do know that you *at least* need to check these options for Faster Melee:

* Faster Melee Netplay Settings
* 60FPS + 4X VRH

For the 5.0 build you need to check this option:

* Netplay Community Settings

Check just those options and uncheck everything else. You will notice that when you switch between versions it will reset the options you have checked, so if you're ever having issues connecting just double check those options again.

If you can't find where they are, you can get to these options by opening Dolphin, right clicking on the Melee ISO -> properties -> gecko codes

Also, there are also some .ini files for each package, right next to the PKGBUILDs. I'm not sure what they do. But if you've done everything and it's still not working, copy them over to `~/.local/share/dolphin-emu/GameSettings`.
