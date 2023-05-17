![BepInEx logo](assets/logo.png)

# BepInEx.SubnauticaZero

This is a [BepInEx](https://github.com/BepInEx/BepInEx) pack for Subnautica: Below Zero, preconfigured and ready to use.

BepInEx is a general purpose framework for Unity modding. BepInEx includes tools and libraries to

-   load custom code (hereafter _plugins_) into the game on launch;
-   patch in-game methods, classes and even entire assemblies without touching original game files;
-   configure plugins and log game to desired outputs like console or file;
-   manage plugin dependencies.

BepInEx is currently [one of the most popular modding tools for Unity on GitHub](https://github.com/topics/modding?o=desc&s=stars).

## This pack's contents

This pack is preconfigured and ready to use for Subnautica: Below Zero modding.  
In particular, this pack comes with 

- a preconfigured `BepInEx.cfg` that enables the BepInEx console and more extensive logging,
- a preconfigured `BepInEx.legacy.cfg` for compatibility with legacy QModManager mods. Simply rename to `BepInEx.cfg` when using QModManager,
- [Tobey.UnityAudio](https://github.com/toebeann/Tobey.UnityAudio), a configurable BepInEx patcher to automatically add Unity audio support when mods need it. Also includes a preconfigured `Tobey.UnityAudio.cfg` for use with Subnautica: Below Zero, and
- [Tobey.BZMacProcessFix](https://github.com/toebeann/Tobey.BZMacProcessFix), a BepInEx patcher which resolves an issue for macOS users were some BepInEx plugins will not load due to process name mismatch between the Windows and macOS versions of the game.

## Compatibility with QModManager

The TL;DR is that QModManager is compatibile with BepInEx, [but there are some things to bear in mind](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/Compatibility-with-QModManager).

## General FAQ

[There is an FAQ in the wiki.](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/FAQ)

## Installation (automatic, Windows only)

1. Install [Vortex Mod Manager](https://www.nexusmods.com/about/vortex/) and the [Subnautica Below Zero Support](https://www.nexusmods.com/site/mods/203) Vortex extension if you haven't already (Vortex should usually install the extension for you). Make sure they're fully up-to-date.
2. Click the Vortex button at the top of [the Nexus Mods mod page](https://www.nexusmods.com/subnauticabelowzero/mods/344) to install.
    - If you have QModManager installed, Vortex might notify you to reinstall/uninstall QModManager. Just do whatever it says.
3. Run the game. If everything runs correctly, you will see the BepInEx console pop up on your desktop.

## Installation on macOS for idiots

[Click here for an idiot's guide to macOS installation.](https://github.com/toebeann/BepInEx.SubnauticaZero/wiki/Idiot's-guide-to-macOS-installation)

## Installation (manual)

**IMPORTANT NOTE**: If you later install QModManager, please make sure to choose **NOT** to overwrite any files when you do.

This is because QModManager overwrites this pack's files with an old version of BepInEx, and many BepInEx plugins require the latest version. QModManager is compatible with this pack's version of BepInEx.

If you do overwrite files when you install QModManager, you will need to reinstall this pack for some BepInEx plugins to work.

***

To install manually, follow these instructions:

1. Download the relevant archive:
    - For Windows and Linux/SteamDeck, download the archive designated `x64`
    - For macOS, download the archive designated `*nix`
2. Extract the contents of the downloaded archive into the game folder:
    - On Windows and Linux/SteamDeck, the game folder is the folder containing the game executable `SubnauticaZero.exe`
    - On macOS, the game folder is the folder containing the game executable `SubnauticaZero.app`
3. If you are using legacy QModManager mods then follow these steps, otherwise skip to step 4:
   1. Navigate to `<path to game folder>\BepInEx\config`
   2. Rename the file `BepInEx.cfg` to `BepInEx.stable.cfg`
   3. Rename the file `BepInEx.legacy.cfg` to `BepInEx.cfg`
   
   **Note**: Please remember to undo these changes if you later stop using QModManager mods.
4. Depending on your operating system:
    - Windows users: Run the game. If everything runs correctly, you will see the BepInEx console pop up on your desktop.
    - Linux/SteamDeck & macOS users: Follow the configuration instructions for your operating system below:

### Configuration (Linux/SteamDeck)

1. In Steam, go to the game's properties and set the launch arguments to:
    ```
    WINEDLLOVERRIDES="winhttp=n,b" %command%
    ```
2. Run the game via Steam.

### Configuration (macOS)

1. Make the `run_bepinex.sh` executable by running this command in Terminal:
    ```
    chmod u+x "<path to game folder>/run_bepinex.sh"
    ```
    **Note**: Make sure to replace `<path to game folder>` with the path to the folder where Subnautica: Below Zero is installed!
2. In Steam, go to the game's properties and set the launch arguments to:
    ```
    "<path to game folder>/run_bepinex.sh" %command%
    ```
    **Note**: Make sure to replace `<path to game folder>` with the path to the folder where Subnautica: Below Zero is installed!
3. Run the game via Steam
4. At this point, you may see a prompt warning you that `libdoorstop_x64.dylib` cannot be opened because the developer is unverified. In this case:
   1. Open System Preferences
   2. Go to Security & Privacy and select the General tab
   3. Towards the bottom you should see a message saying that the program was blocked from opening. Click `Open Anyway` and confirm the prompt that pops up.
   4. Run the game via Steam

At this moment you will not see any clear indication that BepInEx is working. It is suggested to test by installing a simple plugin such as [Configuration Manager](https://www.nexusmods.com/subnautica/mods/1112) and then pressing F5 to open the Configuration Manager window.

If you also wish to use QModManager, you will need to additionally follow these steps to get QModManager to work on macOS:

1. Install QModManager if you haven't already - **DON'T OVERWRITE ANY FILES!**
2. Launch the game once, then quit once you get to the main menu
3. Navigate to `<path to game folder>\BepInEx\plugins\QModMAnager` in Finder
4. Rename the file `QModInstaller.dll` to `QModInstaller.dll.BACKUP`
5. Rename the file `QModInstaller.dll.PATCHED` to `QModInstaller.dll`

QModManager should now work on macOS!

## Useful links

-   [BepInEx: writing basic plugin walkthrough](https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/)
-   [BepInEx: useful plugins for modding](https://docs.bepinex.dev/articles/dev_guide/dev_tools.html)
-   [BepInEx: patching game methods at runtime](https://docs.bepinex.dev/articles/dev_guide/runtime_patching.html)

## Issues, questions, etc.

At this moment, you can use the following channels to ask for help

-   [BepInEx Discord](https://discord.gg/MpFEDAg) -- **Only technical support for THIS PACKAGE. No support for plugins.**
