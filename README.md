## GangstaPatch
[![Download Latest Release](https://img.shields.io/github/v/release/GangstaTeam/GangstaPatch?display_name=release&label=Download%20latest%20release&color=21abc7)](https://github.com/GangstaTeam/GangstaPatch/releases/latest/download/GangstaPatch.asi)&nbsp;
[![Changelog](https://img.shields.io/badge/Changelog-ED1459)](CHANGELOG.md)&nbsp;

- Unofficial patch for v1.00.2 to make the game playable on modern systems and various improvements to the gameplay.
- This patch will never have versioning because it's continuous work and latest build should be used as "stable" build.
- If there is some issue/request just open new issue and fill out the predefined template.

## Installation
1. Download [Simple ASI Loader (vorbisfile.dll)](https://github.com/sneakyevil/SimpleASILoader/releases/download/vorbisfile/vorbisfile.dll).
2. Rename `vorbisfile.dll` to `vorbisfile_original.dll` inside game folder.
3. Place Simple ASI Loader (vorbisfile.dll) in game folder.
4. Download latest build of [GangstaPatch.asi](https://github.com/GangstaTeam/GangstaPatch/releases/latest/download/GangstaPatch.asi).
5. Place asi file in game folder or plugins folder.
- If you get error that you're using wrong executable you can try [download v1.00.2 executable](https://mega.nz/file/3CRi2B5A#jL8v6fhbSQrnctYppNIXzozoV9yFVOTsUUssJWODb5g), if that causes game to crash you should download the (Full RIP patched to v1.00.2) from abandonware.

## Controller Prompts Installation
1. Download png pack of button prompts: 
    - [PlayStation](Files/controller_playstation.png)
    - [Xbox](Files/controller_xbox.png)
    - [Steam Deck](Files/controller_steamdeck.png)
2. Place the file inside game folder under folder `patch`, create one if doesn't exist.
3. Rename the file to `controller.png`.

## Known Issues
...

## INI Settings
- All these options are configurable in 'settings.ini'. The file is automatically created when launching game for the first time with the patch otherwise you can create it manually.
- Most options are configurable in game options.
```ini
[Scarface]
ScreenWidth=640         ; Width of the window
ScreenHeight=480        ; Height of the window
MSAA=8                  ; Anti-aliasing (8 is max)
DrawDistance=2          ; 0 to 2 (Far)
EnableSFX=1             ; Enable special FX (Sun, lens flare, etc...
Aniso=16                ; Anisotropic Filtering (16 is max)
Trilinear=0             ; Trilinear filtering
Brightness=5
Mouse=10                ; Mouse speed

; Additional Patch options:
Captions=0              ; 0: Disabled (Default), 1: Enabled
RefreshRate=60          ; Monitor refresh-rate (Full-screen Only)
VSync=1                 ; 0: Disable (Unlocks FPS), 1: Enable
LanguageID=E            ; E (English, Czech, German, Polish, Russian), F (France), I (Italian), S (Spanish) -> Requires specific game files for functionality
Vibrance=50             ; Adjustable vibrance (0 - 100) (50 -> Default)
ShowFPS=0	            ; Shows FPS at left corner.
SkipLicenseScreen=0	    ; Skips license screen while starting up game.
SkipMovies=0	        ; Skips intro movies while starting up game.
WidescreenHUD=1         ; Modifies 4:3 HUD to 16:9 Ratio.

[Bind]
WallCover=H             ; Changed to 'H', game's default is 'Enter'
Walk=ALT

[Windowed]
Mode=0	                ; 0: None, 1: Windowed, 2: Windowed Borderless

[ParticleEmitter]
EmissionRate=2          ; 0: Disabled, 1: Quality, 2: Balanced, 3: Performance, 4: Potato

[PostProcessFX]
Enable=0                ; Enables blur & bloom.
Bloom=50                ; The game uses dynamic value, using this option will force the value to be always same

[Camera]
FOV=100                 ; Percentage from original FOV (50 to 200)
Acceleration=1
SlowOverTarget=1

[Patch]
EnableMemoryAllocator=0   ; 0: Use system's default malloc/free, 1: Use Doug Lea Memory Allocator
DebugMenu=0             ; Shows debug option in the pause menu.
```

## List of Patches
- Additions
    - Ability to walk with keyboard.
    - Controller Button Prompts with support of creating own buttons.
    - Dynamic Blood similar to PS2 Version.
    - Native way of running game in windowed/windowed borderless.
    - Widescreen HUD (Work in progress).
    - Changing vibrance of display.
    - Option to change emission rate for Particle Emitter.
    - Option to toggle unused Post-Process FX.
    - Option to skip license screen & movies.
    - Cheat codes for blue suit outfits:
        - BLUE, BLUEPIN
    - Option to change language ID.
    - Optional Doug Lea's memory allocator.
        - Game is calling malloc/free each frame even when rendering basic scene and using memory allocator will re-use already allocated pages and prevent calling system functions.
        - If you're having frametime spikes you might consider enabling this.
    - Controlling sniper rifle zoom with mouse wheel.
    - Option to change Refresh Rate.
    - Option to change Vertical Synchronization.
    - Option to change Field Of View
- Fixes
    - 3D Audio causing pitch changes.
    - Captions, Auto Player/Vehicle Tape not been saved between game sessions.
    - Character animations frametime been clamped while playing on high FPS causing animations to play in fast-motion.
    - Character movement having inconsistent speed.
    - Culling mode causing certain parts of model render as invisible.
    - Mouse input been clamped as analog stick.
    - Ocean animation playing too fast/slow depeding on FPS.
    - Rendering issues causing game not to render properly at all.
    - Shadow color glitching in certain areas of map.
    - Vehicle collision with objects would cause it to launch to air at high FPS.
    - Weapon bullet rattle sometimes causing camera to spin continuously.
    - Weapon bullet rattle missing maximum side value.
    - Shaders with alpha been incorrectly rendered.
- Improvements
    - Reverse-Z that fixes z-fighting issues.
    - Properly handle process & thread affinity without hurting performance of the game.
    - Registry settings moved to ini file in the game folder.
    - Removed camera blending, because it interferes with mouse input.
    - Lack of display resolutions in game option.
    - Vehicle glass shader rewritten to support windshield & window damage and better reflection to match console versions.
    - Vehicle shininess modified to match console versions.
    - Better support for Xbox controller mapping.
    - Multiple performance improvements:
        - Due to decision of using v1.00.2 (ActiveMARK protected) version of game, there are bunch of left-over checks that has been removed. There are also some left-over stuff that has been removed that could cause micro-stutters and much more.
    - Mortar UpForce physics been wrongly calculated above 30 FPS.