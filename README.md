## GangstaPatch
[![Download Latest Release](https://img.shields.io/github/v/release/GangstaTeam/GangstaPatch?display_name=release&label=Download%20latest%20release&color=21abc7)](https://github.com/GangstaTeam/GangstaPatch/releases/latest/download/GangstaPatch.asi)&nbsp;
[![Changelog](https://img.shields.io/badge/Changelog-ED1459)](CHANGELOG.md)&nbsp;
[![Patches](https://img.shields.io/badge/Patches-21abc7)](PATCHES.md)

- Unofficial patch for v1.00.2 to make the game playable on modern systems and various improvements to the gameplay.
- This patch will never have versioning because it's continuous work and latest build should be used as "stable" build.
- If there is some issue/request just open new issue and fill out the predefined template.

## Installation
1. Download [Simple ASI Loader (vorbisfile.dll)](https://github.com/sneakyevil/SimpleASILoader/releases/download/vorbisfile/vorbisfile.dll).
2. Rename `vorbisfile.dll` to `vorbisfile_original.dll` inside game folder.
3. Place Simple ASI Loader (vorbisfile.dll) in game folder.
4. Download latest build of [GangstaPatch.asi](https://github.com/GangstaTeam/GangstaPatch/releases/latest/download/GangstaPatch.asi).
5. Place asi file in game folder or plugins folder.

## Controller Prompts Installation
1. Download png pack of button prompts: 
    - [PlayStation](Files/controller_playstation.png)
    - [Xbox](Files/controller_xbox.png)
    - [Steam Deck](Files/controller_steamdeck.png)
2. Place the file inside game folder under folder `patch`, create one if doesn't exist.
3. Rename the file to `controller.png`.

## Known Issues
- Controller doesn't work at start of the game:
    - You're not able to press accept button at main screen while controller is plugged, temporary solution that works is to move right analog around for some time and try spamming the accept button.

## INI Settings
- All those options are configurable in 'settings.ini'. The file is automatically created when launching game for the first time with the patch otherwise you can create it manually.
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
Vibrance=50             ; Adjustable vibrance (0 - 100) (50 -> Default)
ShowFPS=0	            ; Shows FPS at left corner.
SkipLicenseScreen=0	    ; Skips license screen while starting up game.
SkipMovies=0	        ; Skips intro movies while starting up game.
WidescreenHUD=1         ; Modifies 4:3 HUD to 16:9 Ratio.

[Windowed]
Mode=0	                ; 0: None, 1: Windowed, 2: Windowed Borderless

[PostProcessFX]
Enable=0                ; Enables blur & bloom.
Bloom=50                ; The game uses dynamic value, using this option will force the value to be always same

[Patch]
DebugMenu=0             ; Shows debug option in the pause menu.
```