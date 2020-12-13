## Cactus ([Discord](https://discord.gg/t982a4qxN5))
##### By: Jonathan Vasquez (fearedbliss)
##### Build: 2020-12-13-1720

## Description / History

Cactus started out as just a simple application that allowed you to easily and
efficiently Time Travel between every version of Diablo II that ever came out,
while maximizing disk space and enabling full character isolation between versions.
However, even though Cactus itself still is just that, the Cactus Repository has
evolved to become a centralized and historical archive, that aims to preserve every
single Diablo II version that exists (Including the **`1.07 Beta`**).
Cactus is a complete rewrite from scratch of my previous application called:
Bliss Version Switcher. However, since Cactus is written in C#, it behaves as a
native Windows application and allows it to integrate natively with the system.
On the other hand, Bliss Version Switcher was written in Java and thus there were
many limitations that lead to the Cactus rewrite.

This repository also includes several other utilities that I have either created
or collected, which can help you play Vanilla Diablo II better. All Cactus
Platforms for versions below 1.12 already include the fix for removing the
CD requirement (Blizzard already removed this requirement for versions 1.12+).
**`Singling`** provides only non-gameplay modifications, things like CPU fixes,
Ladder Runewords, Multiple Instances, Hardcore Character Creation, Faster LAN
Creation/Joining, Etc. **`Alpaca`** provides an improved and stabilized Infinite
Stash Mod for **`1.13d`** on **`Classic`** and **`Expansion`**, and is stable
for LAN play. Lastly, a few renderers are included to improve video compatibility,
**`cnc-ddraw`** and **`glidewrapper`**. The choice is yours for how you want to play.

Cactus requires a purchased copy of Diablo II from Blizzard in order to have
all of the game assets stored in the MPQs. Once you have these, they will be
re-used for all Cactus Platforms.

For further information, please read the documentation below for anything you
are interested in exploring. If you wish to find players to play with, or just
to hang out and talk about Diablo II Single Player, please join the Cactus
Discord by clicking the link at the top of this page!

## Cactus Repository

The following opt-in modifications and utilities are available in this repository:

#### [Singling](README-SINGLING.md)

A collection of non-gameplay modifications and fixes in
order to improve the Vanilla Diablo II Single Player Experience.

To use Singling, simply copy the Singling files for the version you want to
play from the **`2. Singling/1. Files`** folder, and replace the ones for
the equivalent version in your Platforms directory. To revert, use the files
in **`2. Singling/2. Stock`** instead.

#### [Alpaca](README-ALPACA.md)

Alpaca is an Infinite Stash for **`Diablo II: 1.13d`** that was based off
Yohann Nicolas' **[PlugY](http://plugy.free.fr/en/index.html) 11.02**.
It has been massively refactored, stabilized, and has full support for
**`Diablo II Classic`**. All previous **`PlugY`** bugs that were related to
**`Multiplayer / LAN`** have also been fixed.

To use [Alpaca](https://github.com/fearedbliss/Alpaca), simply copy all the
files in the **`3. Alpaca`** folder into your 1.13d Platform. You can then
launch Diablo II with **`Alpaca.exe`** rather than **`Game.exe`**. In order
to have the best experience, please install Singling as well.

#### [Renderers](README-RENDERERS.md)

Cactus includes two alternative renderers for Diablo II which can help you
run the game on newer systems with a higher resolution (not a higher internal
resolution), and the ability to use shaders to upscale the quality of the
graphics in the game (**`cnc-ddraw`**). Both of these renderers are automatically
included as part of the Cactus Base Installation. **`cnc-ddraw`** should be used
in versions of Diablo II older than **`1.14`**, and **`glidewrapper`** should
be used for any newer versions. Please read the [**`README-RENDERERS`**](README-RENDERERS.md)
for further explanation on this, for information on how to set them up, or for any
known technical limitations.

- [**`cnc-ddraw`**](https://github.com/CnCNet/cnc-ddraw) - This renderer
  reimplements the DirectDraw API for GDI, OpenGL, and Direct 3D to improve
  compatibility with Windows XP - 10, and Wine (Linux). This renderer also
  supports the use of custom shaders - which will allow you to upscale the game
  so it looks a lot better - and even provides hotkeys (such as
  **`[Alt] + [Enter]`**) to switch between full screen and window mode.

- [**`GlideWrapper`**](http://www.svenswrapper.de/english/) - A simple glide to
  opengl wrapper which will allow you to enable **`Perspective`** mode.

## License

Released under the [Apache License 2.0](LICENSE.txt).

## Requirements

- .NET Framework 4.6.1 +

## Installation Instructions

### Install Cactus And Prepare MPQs

This section will help you install Cactus to the correct location and also help you
fix your MPQs so that they are compatible with the older versions of Diablo II.

1. Copy all of the files in the **`1. Files`** folder into your Diablo II root folder.
2. Run the **`FIX_MPQS_RUN_AS_ADMIN.bat`** inside the **`MpqFixer`** that you copied, as
   **`Administrator`**. This will fix your MPQ files so that they work with the older versions
   of the game.

### Adding/Running A Platform

1. Run **`Cactus.exe`**
2. Click **`Add`**
3. Type in the name of the Platform you want to run. This should match a folder in the **`Platforms`**
   folder. (Example: If you want to run **`1.09b`**, type **`1.09b`**).
4. Enter the path to the executable you want to launch in your Diablo II **`root`** folder.
   Cactus copies all of the files from the **`Platforms/[NAME]`** folder to the Diablo II root folder,
   so most of your entries will have identical paths (Example: **`D:\Games\Diablo II\Game.exe`**).
   Do not put something that points to an executable in the **`Platforms`** folder since that will not work
   and will give you an **`Object reference not set to an instance of an object`** error. The executable has
   to be in the root of the Diablo II folder as described above.
5. Enter the Flags you want (Example: **`-ns`**)
6. Make sure **`Expansion`** is selected (Unless you are playing **`1.00-1.06b`** or didn't purchase **`Lord of Destruction`**).
7. Click **`Add`**.
8. Select your newly added Platform and press **`Launch`**.

The game should start. If you are having video issues, please make sure you
have read the [**`README-RENDERERS`**](README-RENDERERS.md) and ensure that
it was configured properly.

## Moving Cactus To A New Computer

If you want to move all of your Platforms, Characters, and Diablo II folder
to another machine, you will need to:

1. Copy your entire Diablo II folder to your new machine.
2. Edit the **`Entries.json`** file and change the **`Path`** for all of your entries
   so that it now has the **`Path`** on your new machine.
   - The **`Base Directory`** for all Paths need to match. The exes can be different.
   		- GOOD: **`D:\Games\Diablo II\Game.exe`** and **`D:\Games\Diablo II\Alpaca.exe`**.
   		- BAD: **`D:\Games\Diablo II\Game.exe`** and **`D:\Diablo Immortal For PC\Game.exe`**.
3. Open **`Cactus`** and edit the **`Last Ran Platform`**.
4. Uncheck the **`Last Ran`** box and Click **`Edit`**.
5. Now **`Launch`** whatever Platform you want.

Unchecking the **`Last Ran`** box will cause Cactus to reconfigure itself (Including registry locations).

## Updating Files In The Platforms folder

If you update any files in your Platforms folder, then uncheck the **`Last Ran`**
box from the corresponding platform, and run it again. This will cause Cactus
to re-install the files with the new ones.
