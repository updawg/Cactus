## Singling
##### By: Jonathan Vasquez (fearedbliss)
##### Build: 2020-09-17-1030

## Description

A collection of non-gameplay modifications and fixes in
order to improve the Vanilla Diablo II Single Player Experience.

## Supported Versions

- **`1.00`**
- **`1.05b`**
- **`1.07`**
- **`1.08`**
- **`1.09b`**
- **`1.13d`**

## Features

- You can now run multiple clients of Diablo II.
- You are now able to quickly join LAN games.
- Fixed CPU usage bug in Main Menu, Single Player, and LAN games.
- The Battle.net button has been disabled for safety reasons.
- The introduction cinematics are now automatically skipped.

- **`[1.00-1.09b]`** You no longer need the CD in order to play the game.
- **`[1.00-1.09b]`** You can now make Hardcore characters without beating Softcore.

- **`[1.08/1.13d]`** Battle.net-only Runewords are now enabled on Single Player.

- **`[1.08-1.13d]`** The game will now work with the MPQ files included in the
  new Blizzard Installer.

## Notes

- **`The massive slowdown when the letters on the top left appears`** affects
  both glide and non-glide code paths, however, it is much more severe on the
  glide side in versions before **`1.14`** and is no longer included in
  Singling. My recommendation is to use **`cnc-ddraw`** rather than
  **`glidewrapper`** for these versions since it will pretty much completely fix
  the issue by using **`DirectDraw`** instead. It will make the game look a lot
  better through the use of shaders, and provides other options such as changing
  the resolution to any resolution you want (Not the internal resolution).
  **`glidewrapper`** should only be used in versions that no longer support
  **`DirectDraw`** such as **`1.14+`**. Cactus comes with **`cnc-ddraw`** and
  **`glidewrapper`**, so both options are available to you.

- When using **`cnc-ddraw`**, you will also automatically gain the ability for
  the window to no longer minimize when you click out of it when using its
  window mode capabilities. Do not use Diablo II's **`-w`** flag since it will
  interfere with **`cnc-ddraw`**. You will also gain the minimize/maximize
  buttons, and the ability to dynamically resize the window as well.

- The Main Menu CPU fix will only be applied for **`v1.10+`**. Most people
  don't spend their time sitting in the Main Menu so this isn't a big deal.
  Also, the CPU fix for LAN in general, doesn't seem to fully drop the CPU usage
  as much as it gets dropped on the Single Player side. This can possibly be
  related to other code (such as networking, video, etc) affecting the game.

- If you are using **`OBS Studio`**, make sure you use **`Window Capture`**
  rather than **`Game Capture`**. The latter will make the game crash when you
  exit the game. This is not a bug caused by Singling, it also happens with
  Vanilla D2.

## Patch Rationale

#### Patch 1.00

This patch was selected due to it simply being the first version of Diablo II
released. There are some things possible in this version that were quickly
patched out, however, there are also many instabilities in the game that may
result in crashes or even the character becoming corrupted.

#### Patch 1.05b

This patch was picked because it is the most stable and balanced version
of the game before **`Lord of Destruction`**. It was also picked over
**`1.06`** since the main reason **`1.06`** was released was to implement
anti-duping code. Due to the way item generation works in these patches,
you can legitimately find items that have the same fingerprint, and the
anti-duping code would delete those items.

#### Patch 1.07

This patch was selected because it is the first version of
**`Lord of Destruction`** that was released and was the first massive change to
Diablo II. Due to this, it contains a lot of features, behaviors, and item
generation combinations that were immediately patched out in patches **`1.08`**
and **`1.09`**. It also contains some bugs that are fun to play with such as the
Rejuvenation Potion Bug or Mana Per Kill (MPK) rings. Overall, **`1.07`** at
this stage is still basically a beta patch and this was why this patch was never
played on the realms (immediately patched to **`1.08`**) and was only available
on Single Player from the Expansion CD upon release.

#### Patch 1.08

This patch was selected because it is a more stable version of **`1.07`**
but still contains a lot of bugs, the famous **`1.08`** unique items, and a lot
of crafting recipes that were disabled in **`1.09`**. It is still less stable
than **`1.09`**, but the game definitely still has a feeling that's between
**`1.07`** and **`1.09`**. This patch is sometimes considered the best patch
to craft in.

#### Patch 1.09b

This patch was picked over **`1.09d`** because it is the most stable version of
Diablo II before the massive changes implemented in 1.10, and also because it
contains **`players 64`** and working CtC. **`1.09d`** has broken CtC which
means that you will see the animation of your CtC effect, but it actually won't
do anything.

#### Patch 1.13d

This patch was selected because it is the last patch released by Blizzard
that is the fully developed version of the game with all quality of life
improvements (respecs, higher rune drop rates, etc), window improvements, etc.
It was also selected because it is the last patch that contained the original
program architecture, which contained all code in their own separate dlls.
Thus this will be the last supported version by Singling.