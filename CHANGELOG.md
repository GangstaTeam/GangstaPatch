# Changelog

- All updates related to GangstaPatch will be documented in this file.

## 2024-09-19
### Removed
- All XOR encryption related to addresses/string.

## 2024-08-25
### Fixed
- Controller accept button not working at the main startup screen asking for press "A/X" button to continue.
### Added
- Saving support for Captions.
### Changed
- Float multiplier in Skin Vertex Shader to get nearest joint damage for blood visualization.

## 2024-08-24
### Updated
- Dynamic blood is handled on individual joints.
### Modified
- Skin Vertex Shader to pass blood damage constants directly to Pixel Shader.

## 2024-08-23
### Added
- Option to change Refresh Rate.
- Option to change Vertical Synchronization.
### Fixed
- Mortar UpForce physics been wrongly calculated above 30 FPS. 

## 2024-08-21
### Added
- Sniper Rifle can be zoomed with mouse wheel.
### Fixed
- Grenade shells ammo indicator not been offset.

## 2024-08-19
### Added
- Optional Doug Lea's memory allocator replacement for default system's malloc/free.

## 2024-08-18
### Fixed
- Language ID been set to 0 instead defaulting to English when not set.

## 2024-08-17
### Added
- Reverse-Z that fixes z fighting issues.
- Option to change language ID.

## 2024-08-16
### Fixed
- Fixed issue since last update that would cause game to instantly crash due to dynamic blood changes.

## 2024-08-15
### Fixed
- Dynamic blood not working on Tony in certain cutscene.
- Dynamic blood texture filtering.
### Changed
- Dynamic blood behavior on certain joints.

## 2024-08-14
### Added
- Dynamic Blood on Tony & Peds has been restored to similar functionality as PS2 version.

## 2024-08-12
### Fixed
- Cop/Gang Heat text not been properly offset in Widescreen HUD.

## 2024-08-06
### Added
- Option to change emission rate for particle emitter.
### Fixed
- Random crash that could occur in function that generates random number (division by zero).

## 2024-08-05
### Added
- Option to change bind for Wall Cover & Walk.
### Fixed
- Icons in Empire been wrongly offset while using Widescreen HUD.

## 2024-08-04
### Fixed
- Vehicle glass having wrong transparency for base texture.

## 2024-08-03
### Added
- Post-process FX settings in game options.
### Changed
- Affinity mode has been modified and option to change the behavior is no longer available, the current way should be final as this will behave mostly as the game wanted while keeping other non-game related thread unaffected. (This should also fix issues with profiles not loading at start of the game)
### Fixed
- Issue with bullet rattle that would cause camera to continuously spin around.

## 2024-07-31
### Added
- Mouse wheel weapon switching.

## 2024-07-30
### Added
- Crash Handler.

## 2024-07-28
### Fixed
- 3D Audio pitch issues.
- Changing resolution while using windowed mode.

## 2024-07-27
### Added
- Added in-game settings integration for certain settings.
- Fixed option 'Tape Player' not been saved.
- Basic file logger for some basic stuff.