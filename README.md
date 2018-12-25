# Goldleaf

![Logo](Logo.png)

> Easy-to-use title installer & manager for Nintendo Switch

- **If you are looking for Tinfoil, this is Tinfoil's safer and way more extended evolution.**

## Brief description

Goldleaf is a multipurpose tool, specialized on title installing from NSP packages, but with other utilities, such as NAND/SD browsing, 

You can easily manage title-related stuff, like install titles via NSP packages or uninstall already installed titles.

If you know what FBI is (related to 3DS homebrew), this is a similar project for Nintendo Switch.

## Disclaimer

Installing NSP packages can be dangerous.

Keep in mind that there will always be a ban risk, and that NSPs with tickets are specially dangerous.

If you want to be safe, avoid connecting to the internet via airplane mode, or block Nintendo's services via special tools such as 90DNS.

Goldleaf simply provides support for a normal NSP and/or ticket installation. The way you use them or the risks you are taking are your problem.

## Goldleaf's features

- Browse and explore SD card's and NAND partitions' (SAFE, USER and SYSTEM) files and directories. Goldleaf provides the functionality of a basic file explorer, with options to browse, delete and copy files or directories between NAND partitions and SD. (writing or deleting content in NAND will always warn the user before doing so).

- The previously mentioned SD/NAND browser also supports NSP installing and NRO launching.

- Manage currently installed titles, being able to see where are they installed, or uninstalling them.

- Manage currently installed tickets, being able to see the application they belong to (their application ID and the key generation), or removing them. (removing tickets can be dangerous anyway)

- Show SD card's and NAND partitions' space, and the firmware version (number and display name) of the current console.

- As some other miscellaneous options, you can easily reboot or shut down your console from Goldleaf.

## Installation

You have two options to use Goldleaf: load it as **regular homebrew via hbmenu** as a **NRO** binary, or install the **NSP** as a **regular title**. Ironically, you would need to install Goldleaf's NSP via Goldleaf as a NRO (or older installers like the original Tinfoil)

For both options, you will have to get the latest release of the **NRO**/**NSP** from [here](https://github.com/XorTroll/Goldleaf/releases).

### Getting ready for USB installations

USB installations require a few extra things to be available:

- Download Zadig tool from [here](https://zadig.akeo.ie/)

- Open Goldleaf and select the USB install option, with the Switch connected to the PC via a USB-C cable.

- Open Zadig, and select the device of your Nintendo Switch, and install libusbK there.

Nothing else is required. No external files, or extra configuration are required for Goldleaf but the NRO/NSP.

- **NRO** binary

  Simply place the NRO anywhere in the SD card (people use to place NROs in `switch` folder) and launch it!

- **NSP** (installable title)

  Goldleaf's NSP title has application ID / title ID `050032A5CF12E000`. (as an extra piece of information)

  You need a homebrew to install the NSP. The best solution would be to download both the NRO and the NSP, and install the NSP via the NRO. (ironically)

  Having it installed, you should be able to launch Goldleaf as a normal title.

## Goldtree

Goldtree is a C# CLI tool for USB installations. Currently it's only available for Windows systems, but it simplifies the process.

USB communication is slightly different from Tinfoil's one, so Tinfoil's old Python script, AluminumFoil nor other tools won't work properly.

Goldtree will ask you to choose a NSP after establishing connection with Goldleaf, and it will be received and installed by Goldleaf.

## Basic controls

The controls are quite intuitive in Goldleaf, but here you have a brief explanation of them:

- Press A to select options from menus, browse folders, or in case it's a file, to browse a menu with file options (copy, delete...)

- Press B to cancel a dialog or to go back to the previous page / menu.

- Press X to paste the path of the clipboard. Obviously, this option is only available on file browsers. (SD or NAND)

- Press Y to browse a menu with directory options, similar to the one used with files, instead of browsing the directory. Obviously, this option is only available on file browsers. (SD or NAND)

- Press ZL or ZR anywhere to browse a menu with reboot / shut down options, in case you want to reboot or shut down the console.

- Press Plus (+) or Minus (-) to exit Goldleaf and return to hbmenu. This option is only available if Goldleaf is loaded as a NRO binary. (more special cases like this one below)

- Movement is quite obvious. Using the L-stick, the D-pad you can move through menu or dialog options. On menus (like the file browsers or the main menu) the R-stick provides a faster scrolling.

## Special features

Goldleaf differs on some features depending on whether it is loaded as a NRO or as an installed title:

- Goldleaf can be exited via Plus (+) or Minus (-) buttons if it's loaded as a NRO, but as regular titles have to be exited from the Home Menu, this feature is not available as a title.

- Goldleaf disables Home button pressing while installing a NSP if it's loaded as a title, but this feature isn't available as a NRO binary for technical reasons related to applets.

- Goldleaf cannot launch NRO binaries if it's loaded as a title due to technical reasons. They can only be launched from another NRO binary.

## Issues and support

In case you find a bug or you need help with Goldleaf, you have several places to ask.

Many errors are very common and can be misunderstood, and you should document a bit for some errors instead of directly calling them issues:

- It's a common issue for some NSPs, although they are completely valid ones, being detected as wrong NSPs. Although they can be really wrong NSPs, it is usually caused by firmware mismatch. For instance, in case you are trying to install a title which requires at least 5.1.0 version (which uses key generation 4) on a lower firmware version, it won't be recognised as a valid NSP for cryptographical reasons. (the console cannot decrypt the NSP because it is encrypted with unknown keys which are within 5.1.0 update)

## Possible future features

- Savedata mounting and browsing (and maybe exporting)

- Dark themeing?

## Credits

- Adubbz and all the (old) Tinfoil contributors, for their huge work with title installing.

- exelix and Qcean team for all their huge support with Home Menu themes. Goldleaf uses (adapted) SwitchThemesCommon libraries to handle theme installs.

- C4Phoenix, for his awesome work doing this project's logo.

- All the icons except Goldleaf's one (see credit above) were grabbed from [Icons8](https://icons8.com).

- The-4n for [hacBrewPack](https://github.com/The-4n/hacBrewPack), to make completely legal NSPs

- All the testers, for reporting bugs and helping with the project's development.

## Patreon

If you like my work, you should take a look at my [Patreon](https://patreon.com/xortroll)!