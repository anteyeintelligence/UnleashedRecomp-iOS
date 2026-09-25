<p align="center">
    <img src="https://raw.githubusercontent.com/hedge-dev/UnleashedRecompResources/refs/heads/main/images/logo/Logo.png" width="512"/>
</p>

---

Unleashed Recompiled iOS is an unofficial iOS port of the Sonic Unleashed Recompiled project.

**This project does not include any game assets. You must provide the files from your own legally acquired copy of the game to install or build Unleashed Recompiled.**

[Check out the latest release here](https://github.com/hedge-dev/UnleashedRecomp/releases/latest).

## Table of Contents

- [Supported Devices](#minimum-system-requirements)
- [How to Install](#how-to-install)
- [Features](#features)
- [Update Roadmap](#update-roadmap)
- [Known Issues](#known-issues)
- [FAQ](#faq)
- [Building](#building)
- [Credits](#credits)

## Supported Devices

Since the game utilizes DXT/BC compressed textures, only very recent iOS devices are supported.

**Supported Chips**
- A17 Pro or later
- A18-series or later
- M-series chips (M1, M2, M3, M4 or newer)

**Supported Devices**
- iPhone 15 Pro
- iPhone 15 Pro Max
- iPhone 16
- iPhone 16 Plus
- iPhone 16 Pro
- iPhone 16 Pro Max
- iPhone 16e
- iPhone 17
- iPhone Air
- iPhone 17 Pro
- iPhone 17 Pro Max
- iPhone 18 Pro
- iPhone 18 Pro Max
- iPhone Duo
- iPad mini (A17 Pro)
- iPad Pro (M1)
- iPad Pro (M2)
- iPad Pro (M4)
- iPad Pro (M5)
- iPad Air (M1)
- iPad Air (M2)
- iPad Air (M3)
- iPad Air (M4)

> [!NOTE]
> More storage space may be required if uncompressed game files are provided during installation.

## How to Install

1) You must have access to the following:
   
     - A legally obtained US or EU Xbox 360 ROM of Sonic Unleashed.
        - Title Update required.
        - All available DLC (Adventure Packs) are optional, but **highly recommended**. **The DLC includes high quality lighting for the entire game**.

> [!TIP]
For instructions on obtaining the ROM file from an Xbox 360, see [here](https://github.com/hedge-dev/UnleashedRecomp#how-to-install)

2) write some shit here

3) Download [the latest release](https://github.com/hedge-dev/UnleashedRecomp/releases/latest) of Unleashed Recompiled iOS and extract it to where you'd like the game to be installed.

4) Run the executable and you will be guided through the installation process. You will be asked to provide the files you acquired in the previous step. When presented with options for how to do this:

    - **Add Files** will only allow you to provide **containers or images dumped from an Xbox 360**. These often come in the form of very large files without associated extensions. Don't worry if you're not aware of what's inside of them, the installer will automatically detect what type of content is inside the container.

    - **Add Folder** will only allow you to provide a **directory with the game's raw files** corresponding to the piece of content that is requested. **It will NOT scan your folder for compatible content!**

> [!NOTE]
> Please note that it is **not possible** to complete the installation if your files have been **modified**. In case of other problems such as black screens or crashes, **do not try to reinstall the game** as it is not possible for the process to result in an invalid installation.

## Features

### Easy to Use Installer

A built-in installation wizard will guide you through the process of installing the game with many integrity checks to ensure the process goes as smoothly as possible. The installer can also be accessed from the title screen, if you wish to add the DLC at a later time.

### Options Menu

A completely new options menu accessible from the title screen or pause menu, with an unprecedented level of fidelity to the game's design language. Get access to many quality of life features and graphics options directly within the game with full controller navigation.

### Achievements

You will be rewarded with achievements as you progress through the game just like on its original platform. Achievements are recreated with integrated notifications and a new menu also very faithful to the game's design language. Get all of them and you will be rewarded with a gold trophy!

> [!NOTE]
> Achievements cannot be used with platforms such as Steam or RetroAchievements.

### Custom Localization

All of the new menus in the port fully support localization for each of the game's originally supported languages; English, Japanese, German, French, Spanish and Italian. As a bonus, switching the game to Japanese also changes the title screen logo to its original Japanese counterpart.

### High Fidelity

Special care and attention was taken to recreate the game's visuals as accurately as possible and was always compared to the game running on the original hardware. The colors are as vibrant as those of the PlayStation 3 version, which did not use the color correction filter present in the Xbox 360 version, as was originally intended. Nevertheless, an option to recreate the original warm filter from the Xbox 360 version has been included as an option.


### High Frame Rate Support

The intended frame-rate cap is 60fps. Higher frame-rates up to 120fps are supported, but a high-power device is required (M4 iPad Pro or better) with significant cuts to 3D Resolution and Graphical Settings. Targeting 60fps is highly recommended.

> [!NOTE]
> Frame-rates above 60fps can cause bugs. This is an issue with Unleashed Recompiled in general, and not specific to this port. It may be fixed in the future.

### Aspect Ratio

As of now, only 16:9 aspect ratio is supported.

### Control schemes

As of now, Keyboard and Controller are the only supported input methods. Basic touch controls may be added in the future. It is highly recommended to only play with a controller.

### Asynchronous Shader Compilation

One of the biggest improvements that the recompilation features over emulators is the fact that Pipeline Compilation (commonly known as "Shader Compilation") is directly integrated into the game as part of the asset loading process. This means there's **no stutters during gameplay the first time new objects or effects appear**.

The renderer will traverse the game's rendering structures and automatically determine what pipelines must be compiled before it considers the asset is loaded. As a result, pipeline compilation is performed in parallel as part of the game's background workers that take care of streaming in the assets, either during regular gameplay or as part of the game's loading screens. This is an improvement that'd never be possible with an emulator, as it requires direct modification of the game to implement this feature.

While this system is very extensive, some special shaders such as post-processing effects or 2D elements are not detected ahead of time, so a list of pre-determined pipelines are compiled during the game's boot sequence. However, the amount is so low that this is done completely in the background and it was determined that there was no need to show a shader compilation screen on most systems that were tested.

> [!NOTE]
> While stutters from shader compilation are non-existent, please be aware that [some stutters](#unavoidable-stutters) may be encountered due to the way the game was programmed. If you encounter these, please keep in mind that **these are not related to shader compilation**. Some of these issues may be addressed in future updates.

### Support for Xbox and PlayStation Controller Icons

You can freely choose whether to use Xbox 360 or PlayStation 3 controller icons. By default, the game will automatically detect which to use based on your controller, but you can select a different option based on your personal preference from within the options menu.

Game objects that display controller icons such as Reaction Plates or Jump Selectors will automatically switch their textures to match the option in use. Even small details such as the Tornado Defense missions using different colors for the missiles have been accounted for.

### Quality of Life Options

Many options have been integrated to address some common quality of life improvements that were deemed to be essential to the port:

- Hint rings and other types of hints provided by the game during exploration or boss fights can be disabled.
- Control tutorials (as referred to by current Sonic games) can be disabled to remove button prompts that show up during gameplay to teach the player how to use certain moves.
- The Werehog's Battle Theme, commonly considered to be an annoyance in the original game due to its frequency and interruption of the stage's background music, can now be disabled.
- The day/night transformation cutscene in towns can use either the Xbox 360 or PlayStation 3 version, with the Xbox version artificially extending loading times for the full video play out, whilst the PlayStation version ends as soon as it's done loading.
- Music Attenuation is a feature that was originally present in the Xbox 360 version of the game, where it'd automatically mute the background music if the console's media player was in use. This feature has been implemented using information provided by the [Windows Media Control](https://learn.microsoft.com/en-us/uwp/api/windows.media.control?view=winrt-26100) APIs in [WinRT](https://en.wikipedia.org/wiki/Windows_Runtime). Applications that interface with Windows 10/11 to display media controls are supported.

> [!TIP]
> You may refer to Music Presence's [list of supported media players](https://github.com/ungive/discord-music-presence/blob/master/documentation/supported-media-players.md) for players that work with Music Attenuation out of the box.

> [!NOTE]
> Please note that Music Attenuation is not currently available on Linux. Support for this feature may be added in a future update.

### Mod Support

Mods are currently not supported. They may be added at a later date, but it is not expected.

## Known Issues

put here whatever known issues are if 2/3 fps and crashes are fixed idk

### Original Game Bugs

Game bugs present on the original hardware are intentionally preserved and will not be fixed. Please do not report issues for these bugs and verify that the issue does not occur on original hardware before reporting. Bug reports for issues found in the original game will be rejected. Bugs that only happen in Unleashed Recompiled must be accompanied by footage captured on original Xbox 360 hardware showing that the bug does not happen there.

## FAQ

### Do you have a website or Discord server?

Yes, Unleashed Recompiled iOS has a discord server for technical help and bug reporting. Join here: https://discord.gg/MRJRyFDEdU

**Please link here when directing anyone to the project.**

> [!CAUTION]
> Do not download builds of Unleashed Recompiled from anywhere but our [Releases](https://github.com/hedge-dev/UnleashedRecomp/releases/latest) page.
>
> **We will never distribute builds on other websites, via Discord servers or via third-party update tools.**

### Why does the installer say my files are invalid?

The installer may display this error for several reasons. Please check the following to ensure your files are valid:

- Please read the [How to Install](#how-to-install) section and make sure you've acquired all of the necessary files correctly.

- Verify that you're not trying to add compressed files such as `.zip`, `.7z`, `.rar` or other formats.

- Only use the **Add Folder** option if you're sure you have a directory with the content's files already extracted, which means it'll only contain files like `.xex`, `.ar.00`, `.arl` and others. **This option will not scan your folder for compatible content**.

- Ensure that the files you've acquired correspond to the same region. **Discs and Title Updates from different regions can't be used together** and will fail to generate a patch.

- The installer will only accept **original and unmodified files**. Do not attempt to provide modified files to the installer.

### What are the keyboard bindings?

Pad|Key
-|-
A (Cross)|S
B (Circle)|D
X (Square)|A
Y (Triangle)|W
D-Pad - Up|Unbound
D-Pad - Down|Unbound
D-Pad - Left|Unbound
D-Pad - Right|Unbound
Start|Return
Back (Select)|Backspace
Left Trigger (L2)|1
Right Trigger (R2)|3
Left Bumper (L1)|Q
Right Bumper (R1)|E
Left Stick - Up|Up Arrow
Left Stick - Down|Down Arrow
Left Stick - Left|Left Arrow
Left Stick - Right|Right Arrow
Right Stick - Up|Unbound
Right Stick - Down|Unbound
Right Stick - Left|Unbound
Right Stick - Right|Unbound

---

You can change the keyboard bindings by editing `config.toml` located in the [configuration directory](#where-is-the-save-data-and-configuration-file-stored), although using a controller is highly recommended until [Action Remapping](#action-remapping) is added in a future update.

Refer to the left column of [this enum template](https://github.com/hedge-dev/UnleashedRecomp/blob/main/UnleashedRecomp/user/config.cpp#L40) for a list of valid keys.

*The default keyboard layout is based on Devil's Details' keyboard layout for Sonic Generations (2011)*.

### Where is the save data and configuration file stored?

DO TS LATER

### I want to update the game. How can I avoid losing my save data? Do I need to reinstall the game?

You can update the game by simply downloading a newer version of the .ipa and installing it. Most sideloaded app managers, including LiveContainer, will have an option to replace the old app file with the new one. Your save data will be preserved.

### How can I install mods?

Do not install mods.

### How can I force the game to run the installation again?

idk if ts is even possible 

### How can I improve performance?

Make sure that you follow the recommended graphical settings provided.
Ensure that Low Power Mode is off and "Limit Frame Rate" is enabled in System Settings before launching Unleashed Recompiled iOS. If you followed these instructions and still fail to reach a consistent 60fps, join the [Discord Server](https://discord.gg/MRJRyFDEdU) and seek help.

### Can I install the game with a PlayStation 3 copy?

**You cannot use the files from the PlayStation 3 version of the game.** Supporting these files would require an entirely new recompilation, as they have proprietary formatting that only works on PS3 and the code for these formats is only present in that version. All significant differences present in the PS3 version of the game have been included in this project as options.

### Can I install the game with a Japanese copy?

The Japanese version of Sonic Unleashed has some minor differences in both file structure and content that make this version of the game incompatible with the international release. Furthermore, the US and EU versions of the game already support Japanese. Supporting this version would only cause mod compatibility issues in the future, so it is unlikely to be added to the update roadmap as it would also require its own recompilation.

## Building

[Check out the building instructions here](/docs/BUILDING.md).

## Credits

### iOS Port

- [MarkosTh09](https://github.com/Markos-Th09): Creator and Lead Developer of the port.

- [Çağan](https://github.com/yorgunkral31): Turkish dude who vibecoded shit and fixed everything

### Unleashed Recompiled

- [Skyth](https://github.com/blueskythlikesclouds): Creator and Lead Developer of the recompilation, as well as the developer of technologies created for it such as [XenonRecomp](https://github.com/hedge-dev/XenonRecomp) and [XenosRecomp](https://github.com/hedge-dev/XenosRecomp). Other responsibilities include the creation of the graphics and audio backends for the project, alongside custom menus, dynamic UI aspect ratio and various patches and new features added to the game.

- [Sajid](https://github.com/Sajidur78): Co-creator and Developer of the recompilation, as well as the developer of [XenonAnalyse](https://github.com/hedge-dev/XenonRecomp/?tab=readme-ov-file#XenonAnalyse). Other responsibilities include the implementation of core components for the project, like the Xbox 360 kernel translation layer used to make the game function.

- [Hyper](https://github.com/hyperbx): Developer of system level features, such as achievement support and the custom menus, alongside various other patches and features to make the game feel right at home on modern systems. Aided in the creation of concept art and the final options menu thumbnails.

- [Darío](https://github.com/DarioSamo): Creator of the graphics hardware abstraction layer [plume](https://github.com/renderbag/plume), used by the project's graphics backend. Alongside providing consultation for graphics and aiding with shader research and development, other responsibilities include the installer wizard and Linux support. Provided Spanish localization for the custom menus.

- [ĐeäTh](https://github.com/DeaTh-G): Supervisor of game accurate design philosophy regarding the custom menus. Aided in the implementation of annotation support for Japanese localization, whilst providing minor support for all localization.

- [RadiantDerg](https://github.com/RadiantDerg): Lead Artist behind the thumbnails used in the options menu. Other responsibilities include the creation of several debugging related codes for Hedge Mod Manager and providing aid with the research of the game's internals.

- [PTKay](https://github.com/PTKay): Lead Concept Artist for the custom menus. Aided in the development of the installer wizard's visuals.

- [SuperSonic16](https://github.com/thesupersonic16): Lead Developer of [Hedge Mod Manager](https://github.com/thesupersonic16/HedgeModManager), providing compatibility for modding with the recompilation. Aided in the creation of the deployment system for Linux builds.

- [NextinHKRY](https://github.com/NextinMono): Aided in researching the game's internals and creating concept art for some options menu thumbnails used in the final release. Provided Italian localization for the custom menus.

- [LadyLunanova](https://linktr.ee/ladylunanova): Artist behind the achievement trophy sprite and the keyboard and mouse icons used in the installer wizard. 

- [LJSTAR](https://github.com/LJSTARbird): Artist behind the project logo, along with several thumbnail designs used in the options menu and created new icons for the button guide for opening the achievements menu. Provided French localization for the custom menus.

- [saguinee](https://twitter.com/saguinee): Artist behind thumbnail designs used in the options menu such as Hints and Battle Theme.

- [Goalringmod27](https://linktr.ee/goalringmod27): Concept Artist behind the achievements overlay shown during gameplay. Aided in the creation of the Transparency Anti-Aliasing thumbnail.

- [RagdollClash](https://github.com/RagdollClash): Provisional support for dynamic UI aspect ratio.

- [DaGuAr](https://twitter.com/TheDaguar): Provided Spanish localization for the custom menus alongside Darío.

- [brianuuuSonic](https://github.com/brianuuu): Provided Japanese localization for the custom menus.

- [Kitzuku](https://github.com/Kitzuku): Provided German localization for the custom menus.

### Special Thanks
- [Mr-Wiseguy](https://github.com/Mr-Wiseguy): Creator of [N64: Recompiled](https://github.com/N64Recomp/N64Recomp), which was the inspiration behind the creation of this project. Provided information and assistance at the beginning of development.

- [xenia-project](https://github.com/xenia-project/xenia): Extraordinary amounts of research regarding the inner workings of the Xbox 360, which sped up the development of the recompilation.

- [Katlin Daigler](https://katlindaigler.carbonmade.com): Provided consultation for logo design.

- [ocornut](https://github.com/ocornut): Creator of [Dear ImGui](https://github.com/ocornut/imgui), which is used as the backbone of the custom menus.

- Raymond Chen: Useful resources on Windows application development with his blog ["The Old New Thing"](https://devblogs.microsoft.com/oldnewthing/).
