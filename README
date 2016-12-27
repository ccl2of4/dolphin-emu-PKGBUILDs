# Before you start

In this repo are three folders for three different packages. They will all install under separate directories in `/opt` so that they do not conflict with each other.

Before installing these packages, you must first make sure you've install the regular `dolphin-emu` package.

`pacman -S dolphin-emu`

You need this package because it provides the udev rules for the gc adapter (remember these packages will install under `/opt`, so I removed the udev rules from their PKGBUILDs)

Now you can install all of these packages.

# Instructions

To install any of the packages, just use `makepkg`

For example

    cd dolphin-emu-faster-melee-4.3
    makepkg -si

Now you have that package installed. For each package, there should be a .desktop file located at /opt/${package-name}/share/applications/dolphin-emu.desktop

To get this .desktop file to be detected by whatever launcher/desktop environment you use, just create a symlink to it, e.g.

    ln -s /opt/dolphin-emu-git-netplay/share/applications/dolphin-emu.desktop /usr/local/share/applications/dolphin-emu-git-netplay
