![BepInEx logo](assets/logo.png)

# Tobey's BepInEx Pack for Subnautica: Below Zero

This is a [BepInEx](https://github.com/BepInEx/BepInEx) pack for Subnautica: Below Zero, preconfigured and ready to use on Windows, macOS and Linux (including SteamOS)!

BepInEx is a general purpose framework for Unity modding. BepInEx includes tools and libraries to

-   load custom code (hereafter _plugins_) into the game on launch;
-   patch in-game methods, classes and even entire assemblies without touching original game files;
-   configure plugins and log game to desired outputs like console or file;
-   manage plugin dependencies.

BepInEx is currently [one of the most popular modding tools for Unity on GitHub](https://github.com/topics/modding?o=desc&s=stars).

## This pack's contents

This pack is preconfigured and ready to use for Subnautica: Below Zero modding.  
In particular, this pack comes with

-   [Tobey.Subnautica.ConfigHandler](https://github.com/toebeann/Tobey.Subnautica.ConfigHandler), a configurable BepInEx patcher to automatically take care of BepInEx configuration for QModManager compatibility,
-   [Tobey.UnityAudio](https://github.com/toebeann/Tobey.UnityAudio), a configurable BepInEx patcher to automatically add Unity audio support when mods need it,
-   [Tobey.PluginDoctor](https://github.com/toebeann/Tobey.PluginDoctor), a BepInEx plugin & patcher combo which diagnoses and reports advice on how to handle common problems with BepInEx 5 plugins,
-   [Tobey.FileTree](https://github.com/toebeann/Tobey.FileTree), a configurable BepInEx plugin which logs the game's file tree to aid in troubleshooting issues, and
-   [Tobey.BZMacProcessFix](https://github.com/toebeann/Tobey.BZMacProcessFix), a BepInEx patcher which allows BepInEx plugins with the process filter `SubnauticaZero` to load on macOS - it is finally possible for macOS users to run QModManager!

## Compatibility with QModManager

The TL;DR is that QModManager is compatibile with BepInEx, [but there are some things to bear in mind](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/Compatibility-with-QModManager).

## General FAQ

[There is an FAQ in the wiki](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/FAQ).

## Easy Automated Installation

### Windows (Vortex)

[Vortex](https://www.nexusmods.com/about/vortex/) is a tool for installing and managing mods on Windows. It can install all kinds of mods for Subnautica and other games, including this pack.

1. Install [Vortex Mod Manager](https://www.nexusmods.com/about/vortex/) if you haven't already. Make sure it's fully up-to-date.
1. Click the Vortex button at the top of [the Nexus Mods mod page](https://www.nexusmods.com/subnauticabelowzero/mods/344) to install.
1. Check the 🔔 notifications area at the top right of Vortex:
    - If you have QModManager installed, Vortex might notify you to reinstall/uninstall QModManager. Just do whatever it says.
    - If you see a notification saying "Elevation needed to deploy," click `Elevate` and authorize the elevation.
    - If you see any other notifications saying "Deployment needed" or similar, click `Deploy`.
1. Run the game. If everything runs correctly, you will see the BepInEx console pop up on your desktop.

### macOS (gib)

[gib](https://github.com/toebeann/gib) is a command-line tool which automates installation of BepInEx on macOS, as installing it manually is quite cumbersome and error-prone. gib makes it easy.

1. [Download Tobey's BepInEx Pack for Subnautica: Below Zero](https://github.com/toebeann/BepInEx.SubnauticaZero/releases/latest/download/BepInEx.zip). Make sure to unzip it in your Downloads folder if your browser doesn't do this automatically.
1. Open Terminal with Launchpad (`⌘ Space`, type `terminal`).
1. Copy the command from [the Usage section of the gib README](https://github.com/toebeann/gib#usage) and paste it into the Terminal with `⌘ V`, and press `Enter` to run it.

If you get stuck, refer to the [gib README](https://github.com/toebeann/gib#readme) for help.

## Manual Installation

**ℹ️** macOS users should follow [the idiot's guide to macOS installation](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/Idiot's-guide-to-macOS-installation).

***

**⚠️ IMPORTANT NOTE ⚠️**

If you later install QModManager, please make sure to choose **NOT** to overwrite any files when you do.

This is because QModManager overwrites this pack's files with an old version of BepInEx, and many BepInEx plugins require the latest version. QModManager is compatible with this pack's version of BepInEx.

If you do overwrite files when you install QModManager, you will need to reinstall this pack for some BepInEx plugins to work.

***

To install manually, follow these instructions:

1. [Download Tobey's BepInEx Pack for Subnautica: Below Zero](https://github.com/toebeann/BepInEx.SubnauticaZero/releases/latest/download/BepInEx.zip).
1. Extract the contents of the downloaded archive into the game folder:
    - On Windows and Linux (SteamOS etc.), the game folder is the folder containing the game executable `SubnauticaZero.exe`
    - On macOS, the game folder is the folder containing the game executable `SubnauticaZero.app`
1. Depending on your operating system:
    - Windows users: Run the game. If everything runs correctly, you will see the BepInEx console pop up on your desktop.
    - Linux (SteamOS etc.) & macOS users: Follow the configuration instructions for your operating system below:

### Configuration on Linux (SteamOS etc.)

1. In Steam, go to the game's properties and set the launch arguments to:
    ```
    WINEDLLOVERRIDES="winhttp=n,b" %command%
    ```
1. Run the game via Steam.

### Configuration on macOS

[Follow the idiot's guide to macOS installation](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/Idiot's-guide-to-macOS-installation).

## Useful links

-   [BepInEx: writing basic plugin walkthrough](https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/)
-   [BepInEx: useful plugins for modding](https://docs.bepinex.dev/articles/dev_guide/dev_tools.html)
-   [BepInEx: patching game methods at runtime](https://docs.bepinex.dev/articles/dev_guide/runtime_patching.html)

## Issues, questions, etc.

[First, check the FAQ to see if there is an answer to your question/issue](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/FAQ).

If not, at this moment, you can use the following channels to ask for help

-   [Subnautica Modding Community Discord](https://discord.gg/UpWuWwq)
-   [BepInEx Discord](https://discord.gg/MpFEDAg) -- **Only technical support for THIS PACKAGE. No support for plugins.**
