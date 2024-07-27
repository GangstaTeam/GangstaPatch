## GangstaPatch
[![Download Latest Release](https://img.shields.io/github/v/release/GangstaTeam/GangstaPatch?display_name=release&label=Download%20latest%20release&color=21abc7)](https://github.com/GangstaTeam/GangstaPatch/releases/latest/download/GangstaPatch.asi)
[![Changelog](https://img.shields.io/badge/Changelog-ED1459)](CHANGELOG.md)

- Unofficial patch for v1.00.2 to make the game playable on modern systems and various improvements to the gameplay.
- This is patch will never have versioning because it's continuous work and latest build should be used as "stable" build.
- If there is some issue/request just open new issue and fill out the predefined template.

## Installation
1. Download latest release.
2. Download ASI Loader or [Simple ASI Loader](https://github.com/sneakyevil/SimpleASILoader/releases/download/vorbisfile/vorbisfile.dll).
3. Place asi file of the patch in game folder / plugins folder.

## Controller Prompts Installation
1. Download png pack of button prompts: 
    - [PlayStation](Files/controller_playstation.png)
    - [Xbox](Files/controller_xbox.png)
    - [Steam Deck](Files/controller_steamdeck.png)
2. Place the file inside game folder under folder `patch`, create one if doesn't exist.
3. Rename the file to `controller.png`.

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
Vibrance=50             ; Adjustable vibrance (1 - 100) (50 -> Default)
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
AffinityMode=0          ; 0: None, 1: All besides core 0 (Might improve performance on Hyper-threaded CPU), 2: Game Handled (Default)
DebugMenu=0             ; Shows debug option in the pause menu.
```