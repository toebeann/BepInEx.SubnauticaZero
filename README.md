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
In particular, this pack comes with preconfigured `BepInEx.cfg` that enables the BepInEx console and more extensive logging.

## Installation (manual)

To install manually, follow these instructions:

1. Download the relevant archive:
    - For Windows and Linux/SteamDeck, download the archive designated `x64`
    - For macOS, download the archive designated `*nix`
2. Extract the contents of the downloaded archive into the game folder:
    - On Windows and Linux/SteamDeck, the game folder is the folder containing the game executable `SubnauticaZero.exe`
    - On macOS, the game folder is the folder containing the game executable `SubnauticaZero.app`
3. Depending on your operating system:
    - Windows users: Run the game. If everything runs correctly, you will see the BepInEx console pop up on your desktop.
    - Linux/SteamDeck & macOS users: Follow the configuration instructions for your operating system below:

### Configuration (Linux/SteamDeck)

1. In Steam, go to the game's properties and set the launch arguments to:
    ```
    WINEDLLOVERRIDES="winhttp=n,b" %command%
    ```
2. Run the game via Steam.

### Configuration (macOS)

1. Make the `run_bepinex.sh` executable in Terminal with `chmod u+x run_bepinex.sh`
2. In Steam, go to the game's properties and set the launch arguments to:
    ```
    "<path to game folder>/run_bepinex.sh" %command%
    ```
    Make sure to replace `<path to game folder>` with the path to the folder where Subnautica: Below Zero is installed!
3. Run the game via Steam
4. At this point, you may see a prompt warning you that `libdoorstop_x64.dylib` cannot be opened because the developer is unverified. In this case:
   1. Open System Preferences
   2. Go to Security & Privacy and select the General tab
   3. Towards the bottom you should see a message saying that the program was blocked from opening. Click `Open Anyway` and confirm the prompt that pops up.
   4. Run the game via Steam

At this moment you will not see any clear indication that BepInEx is working. It is suggested to test by installing a simple plugin such as [Configuration Manager](https://www.nexusmods.com/subnautica/mods/1112) and then pressing F5 to open the Configuration Manager window.

## Useful links

-   [BepInEx: writing basic plugin walkthrough](https://docs.bepinex.dev/articles/dev_guide/plugin_tutorial/)
-   [BepInEx: useful plugins for modding](https://docs.bepinex.dev/articles/dev_guide/dev_tools.html)
-   [BepInEx: patching game methods at runtime](https://docs.bepinex.dev/articles/dev_guide/runtime_patching.html)

## Issues, questions, etc.

At this moment, you can use the following channels to ask for help

-   [Subnautica Modding Community Discord](https://discord.gg/UpWuWwq)
-   [BepInEx Discord](https://discord.gg/MpFEDAg) -- **Only technical support for THIS PACKAGE. No support for plugins.**
