# Minecraft Bedrock Edition Command Reference

This documentation was generated with AI assistance. Generated from BDS Commands and localized with `en_US.lang`. Commands included: **83**.

This document lists every command overload found in the source data, each overload's full syntax, and parameter-level details with candidate values. However, there is some inappropriate candidates, such as camera time.

**Documentation Version:** Minecraft Bedrock Edition 1.26.0

## Command Index

### Standard Commands

- [/aimassist](#aimassist)
- [/allowlist](#allowlist)
- [/camera](#camera)
- [/camerashake](#camerashake)
- [/changesetting](#changesetting)
- [/clear](#clear)
- [/clearspawnpoint](#clearspawnpoint)
- [/clone](#clone)
- [/controlscheme](#controlscheme)
- [/damage](#damage)
- [/daylock](#daylock)
- [/deop](#deop)
- [/dialogue](#dialogue)
- [/difficulty](#difficulty)
- [/effect](#effect)
- [/enchant](#enchant)
- [/event](#event)
- [/execute](#execute)
- [/fill](#fill)
- [/fog](#fog)
- [/function](#function)
- [/gamemode](#gamemode)
- [/gamerule](#gamerule)
- [/gametest](#gametest)
- [/give](#give)
- [/hud](#hud)
- [/inputpermission](#inputpermission)
- [/kick](#kick)
- [/kill](#kill)
- [/list](#list)
- [/locate](#locate)
- [/loot](#loot)
- [/me](#me)
- [/mobevent](#mobevent)
- [/music](#music)
- [/op](#op)
- [/packstack](#packstack)
- [/particle](#particle)
- [/permission](#permission)
- [/place](#place)
- [/playanimation](#playanimation)
- [/playsound](#playsound)
- [/recipe](#recipe)
- [/reload](#reload)
- [/reloadconfig](#reloadconfig)
- [/reloadpacketlimitconfig](#reloadpacketlimitconfig)
- [/replaceitem](#replaceitem)
- [/ride](#ride)
- [/save](#save)
- [/say](#say)
- [/schedule](#schedule)
- [/scoreboard](#scoreboard)
- [/sendshowstoreoffer](#sendshowstoreoffer)
- [/setblock](#setblock)
- [/setmaxplayers](#setmaxplayers)
- [/setworldspawn](#setworldspawn)
- [/spawnpoint](#spawnpoint)
- [/spreadplayers](#spreadplayers)
- [/stop](#stop)
- [/stopsound](#stopsound)
- [/structure](#structure)
- [/summon](#summon)
- [/tag](#tag)
- [/teleport](#teleport)
- [/tell](#tell)
- [/tellraw](#tellraw)
- [/testfor](#testfor)
- [/testforblock](#testforblock)
- [/testforblocks](#testforblocks)
- [/tickingarea](#tickingarea)
- [/time](#time)
- [/title](#title)
- [/titleraw](#titleraw)
- [/toggledownfall](#toggledownfall)
- [/transfer](#transfer)
- [/weather](#weather)
- [/xp](#xp)

### WebSocket / Script Integration Commands

- [/script](#script)
- [/scriptevent](#scriptevent)
- [/wsserver](#wsserver)

### Education Edition-only Commands

- [/ability](#ability)
- [/immutableworld](#immutableworld)
- [/worldbuilder](#worldbuilder)

## Standard Commands

### /aimassist

Enable Aim Assist

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/aimassist <players> set [<x_angle>] [<y_angle>] [<max_distance>] [<target_mode>] [<preset_id>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (AimAssistActionSet) | Literal keyword. | `set`<br>[enum reference](#static-enum-aimassistactionset-34) |
   | 3 | `x angle` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 4 | `y angle` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `max distance` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 6 | `target mode` | No | Static Enum (AimAssistTargetMode) | Value from static enum `AimAssistTargetMode`. | `distance`, `angle`<br>[enum reference](#static-enum-aimassisttargetmode-33) |
   | 7 | `preset id` | No | String (id:56) | Single string token. | `example_text` |

2. `/aimassist <players> clear`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `clear` | Yes | Static Enum (AimAssistActionClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-aimassistactionclear-35) |

### /allowlist

Manages the server allowlist.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

**Aliases:** `/whitelist`

1. `/allowlist <action> [<name>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (AllowListAction) | Value from static enum `AllowListAction`. | `add`, `remove`, `list`, `reload`, `on`, `off`<br>[enum reference](#static-enum-allowlistaction-244) |
   | 2 | `name` | No | String (id:56) | Single string token. | `example_text` |

### /camera

Issues a camera instruction

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 38

1. `/camera <players> set <preset> ease <easeTime> <easeType> pos <position> rot <xRot> <yRot>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
   | 8 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 9 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
   | 10 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 11 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |

2. `/camera <players> set <preset> ease <easeTime> <easeType> pos <position> facing <lookAtEntity>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
   | 8 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 9 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
   | 10 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

3. `/camera <players> set <preset> ease <easeTime> <easeType> pos <position> facing <lookAtPosition>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
   | 8 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 9 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
   | 10 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

4. `/camera <players> set <preset> ease <easeTime> <easeType> pos <position>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
   | 8 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

5. `/camera <players> set <preset> ease <easeTime> <easeType> rot <xRot> <yRot>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
   | 8 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 9 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |

6. `/camera <players> set <preset> ease <easeTime> <easeType> facing <lookAtEntity>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
   | 8 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

7. `/camera <players> set <preset> ease <easeTime> <easeType> facing <lookAtPosition>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
   | 8 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

8. `/camera <players> set <preset> ease <easeTime> <easeType> [default]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
   | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
   | 7 | `default` | No | Static Enum (default) | Literal keyword. | `default`<br>[enum reference](#static-enum-default-48) |

9. `/camera <players> set <preset> pos <position> rot <xRot> <yRot>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
   | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
   | 4 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
   | 5 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 6 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
   | 7 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 8 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |

10. `/camera <players> set <preset> pos <position> facing <lookAtEntity>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
    | 5 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 6 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
    | 7 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

11. `/camera <players> set <preset> pos <position> facing <lookAtPosition>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
    | 5 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 6 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
    | 7 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

12. `/camera <players> target_entity <entity>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `targetEntity` | Yes | Static Enum (target_entity) | Literal keyword. | `target_entity`<br>[enum reference](#static-enum-targetentity-43) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

13. `/camera <players> target_entity <entity> target_center_offset <xTargetCenterOffset> <yTargetCenterOffset> <zTargetCenterOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `targetEntity` | Yes | Static Enum (target_entity) | Literal keyword. | `target_entity`<br>[enum reference](#static-enum-targetentity-43) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `targetCenterOffset` | Yes | Static Enum (target_center_offset) | Literal keyword. | `target_center_offset`<br>[enum reference](#static-enum-targetcenteroffset-44) |
    | 5 | `xTargetCenterOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `yTargetCenterOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 7 | `zTargetCenterOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

14. `/camera <players> remove_target`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `removeTarget` | Yes | Static Enum (remove_target) | Literal keyword. | `remove_target`<br>[enum reference](#static-enum-removetarget-45) |

15. `/camera <players> set <preset> view_offset <xViewOffset> <yViewOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 5 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

16. `/camera <players> set <preset> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 5 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 7 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

17. `/camera <players> set <preset> rot <xRot> <yRot> view_offset <xViewOffset> <yViewOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 5 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 6 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 7 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 8 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

18. `/camera <players> set <preset> rot <xRot> <yRot> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 5 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 6 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 7 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 8 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 10 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

19. `/camera <players> set <preset> view_offset <xViewOffset> <yViewOffset> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 5 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 7 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 8 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 10 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

20. `/camera <players> set <preset> rot <xRot> <yRot> view_offset <xViewOffset> <yViewOffset> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 5 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 6 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 7 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 8 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 10 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 11 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 12 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 13 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

21. `/camera <players> set <preset> ease <easeTime> <easeType> view_offset <xViewOffset> <yViewOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 8 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

22. `/camera <players> set <preset> ease <easeTime> <easeType> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 8 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 10 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

23. `/camera <players> set <preset> ease <easeTime> <easeType> rot <xRot> <yRot> view_offset <xViewOffset> <yViewOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 8 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 9 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 10 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 11 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 12 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

24. `/camera <players> set <preset> ease <easeTime> <easeType> rot <xRot> <yRot> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 8 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 9 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 10 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 11 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 12 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 13 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

25. `/camera <players> set <preset> ease <easeTime> <easeType> view_offset <xViewOffset> <yViewOffset> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 8 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 9 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 10 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 11 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 12 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 13 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

26. `/camera <players> set <preset> ease <easeTime> <easeType> rot <xRot> <yRot> view_offset <xViewOffset> <yViewOffset> entity_offset <xEntityOffset> <yEntityOffset> <zEntityOffset>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `ease` | Yes | Static Enum (ease) | Literal keyword. | `ease`<br>[enum reference](#static-enum-ease-37) |
    | 5 | `easeTime` | Yes | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 6 | `easeType` | Yes | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |
    | 7 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 8 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 9 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 10 | `view_offset` | Yes | Static Enum (view_offset) | Literal keyword. | `view_offset`<br>[enum reference](#static-enum-viewoffset-46) |
    | 11 | `xViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 12 | `yViewOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 13 | `entity_offset` | Yes | Static Enum (entity_offset) | Literal keyword. | `entity_offset`<br>[enum reference](#static-enum-entityoffset-47) |
    | 14 | `xEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 15 | `yEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 16 | `zEntityOffset` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

27. `/camera <players> set <preset> pos <position>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `pos` | Yes | Static Enum (pos) | Literal keyword. Coordinate argument. | `pos`<br>[enum reference](#static-enum-pos-38) |
    | 5 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

28. `/camera <players> set <preset> rot <xRot> <yRot>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `rot` | Yes | Static Enum (rot) | Literal keyword. | `rot`<br>[enum reference](#static-enum-rot-39) |
    | 5 | `xRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
    | 6 | `yRot` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |

29. `/camera <players> set <preset> facing <lookAtEntity>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
    | 5 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

30. `/camera <players> set <preset> facing <lookAtPosition>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `facing` | Yes | Static Enum (facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-facing-42) |
    | 5 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

31. `/camera <players> set <preset> [default]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `set` | Yes | Static Enum (set) | Literal keyword. | `set`<br>[enum reference](#static-enum-set-36) |
    | 3 | `preset` | Yes | Dynamic Enum (CameraPresets) | Runtime or registry-backed value from dynamic enum `CameraPresets`. | `minecraft:first_person`, `minecraft:fixed_boom`, `minecraft:follow_orbit`, `minecraft:free`, `minecraft:third_person`, `minecraft:third_person_front`<br>[enum reference](#dynamic-enum-camerapresets-8) |
    | 4 | `default` | No | Static Enum (default) | Literal keyword. | `default`<br>[enum reference](#static-enum-default-48) |

32. `/camera <players> clear`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `clear` | Yes | Static Enum (clear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-clear-49) |

33. `/camera <players> fade time <fadeInSeconds> <holdSeconds> <fadeOutSeconds> color <red> <green> <blue>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fade` | Yes | Static Enum (fade) | Literal keyword. | `fade`<br>[enum reference](#static-enum-fade-50) |
    | 3 | `time` | Yes | Static Enum (time) | Literal keyword. Time value. | `time`<br>[enum reference](#static-enum-time-51) |
    | 4 | `fadeInSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 5 | `holdSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `fadeOutSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 7 | `color` | Yes | Static Enum (color) | Literal keyword. | `color`<br>[enum reference](#static-enum-color-52) |
    | 8 | `red` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |
    | 9 | `green` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |
    | 10 | `blue` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |

34. `/camera <players> fade time <fadeInSeconds> <holdSeconds> <fadeOutSeconds>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fade` | Yes | Static Enum (fade) | Literal keyword. | `fade`<br>[enum reference](#static-enum-fade-50) |
    | 3 | `time` | Yes | Static Enum (time) | Literal keyword. Time value. | `time`<br>[enum reference](#static-enum-time-51) |
    | 4 | `fadeInSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 5 | `holdSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 6 | `fadeOutSeconds` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

35. `/camera <players> fade color <red> <green> <blue>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fade` | Yes | Static Enum (fade) | Literal keyword. | `fade`<br>[enum reference](#static-enum-fade-50) |
    | 3 | `color` | Yes | Static Enum (color) | Literal keyword. | `color`<br>[enum reference](#static-enum-color-52) |
    | 4 | `red` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |
    | 5 | `green` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |
    | 6 | `blue` | Yes | Integer (id:1) | Whole number. Color channel (commonly 0-255). | `0`, `1`, `-1` |

36. `/camera <players> fade`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fade` | Yes | Static Enum (fade) | Literal keyword. | `fade`<br>[enum reference](#static-enum-fade-50) |

37. `/camera <players> fov_set <fov_value> [<fovEaseTime>] [<fovEaseType>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fov_set` | Yes | Static Enum (fov_set) | Literal keyword. | `fov_set`<br>[enum reference](#static-enum-fovset-40) |
    | 3 | `fov_value` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
    | 4 | `fovEaseTime` | No | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 5 | `fovEaseType` | No | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |

38. `/camera <players> fov_clear [<fovEaseTime>] [<fovEaseType>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `fov_clear` | Yes | Static Enum (fov_clear) | Literal keyword. | `fov_clear`<br>[enum reference](#static-enum-fovclear-41) |
    | 3 | `fovEaseTime` | No | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
    | 4 | `fovEaseType` | No | Static Enum (Easing) | Value from static enum `Easing`. | `linear`, `spring`, `in_quad`, `out_quad`, `in_out_quad`, `in_cubic`, `out_cubic`, `in_out_cubic`, `in_quart`, `out_quart` ... (32 total)<br>[enum reference](#static-enum-easing-32) |

### /camerashake

Applies shaking to the players' camera with a specified intensity and duration.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/camerashake add <player> [<intensity>] [<seconds>] [<shakeType>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (CameraShakeActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-camerashakeactionadd-53) |
   | 2 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `intensity` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 4 | `seconds` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `shakeType` | No | Static Enum (CameraShakeType) | Value from static enum `CameraShakeType`. | `positional`, `rotational`<br>[enum reference](#static-enum-camerashaketype-55) |

2. `/camerashake stop [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (CameraShakeActionStop) | Literal keyword. | `stop`<br>[enum reference](#static-enum-camerashakeactionstop-54) |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /changesetting

Changes a setting on the dedicated server while it's running.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 3

1. `/changesetting allow-cheats <value>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `setting` | Yes | Static Enum (BoolSettingName) | Literal keyword. | `allow-cheats`<br>[enum reference](#static-enum-boolsettingname-246) |
   | 2 | `value` | Yes | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

2. `/changesetting difficulty <value>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `setting` | Yes | Static Enum (DifficultySettingName) | Literal keyword. | `difficulty`<br>[enum reference](#static-enum-difficultysettingname-247) |
   | 2 | `value` | Yes | Static Enum (Difficulty) | Value from static enum `Difficulty`. | `normal`, `peaceful`, `easy`, `hard`, `p`, `e`, `n`, `h`<br>[enum reference](#static-enum-difficulty-68) |

3. `/changesetting difficulty <value>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `setting` | Yes | Static Enum (DifficultySettingName) | Literal keyword. | `difficulty`<br>[enum reference](#static-enum-difficultysettingname-247) |
   | 2 | `value` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /clear

Clears items from player inventory.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/clear [<player>] [<itemName>] [<data>] [<maxCount>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `itemName` | No | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 3 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `maxCount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /clearspawnpoint

Removes the spawn point for a player.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/clearspawnpoint [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /clone

Clones blocks from one region to another.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/clone <begin> <end> <destination> [<maskMode>] [<cloneMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `begin` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `end` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `destination` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `maskMode` | No | Static Enum (MaskMode) | Value from static enum `MaskMode`. | `replace`, `masked`<br>[enum reference](#static-enum-maskmode-56) |
   | 5 | `cloneMode` | No | Static Enum (CloneMode) | Value from static enum `CloneMode`. | `normal`, `force`, `move`<br>[enum reference](#static-enum-clonemode-58) |

2. `/clone <begin> <end> <destination> filtered <cloneMode> <tileName> [<blockStates>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `begin` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `end` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `destination` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `maskMode` | Yes | Static Enum (MaskModeFiltered) | Literal keyword. | `filtered`<br>[enum reference](#static-enum-maskmodefiltered-57) |
   | 5 | `cloneMode` | Yes | Static Enum (CloneMode) | Value from static enum `CloneMode`. | `normal`, `force`, `move`<br>[enum reference](#static-enum-clonemode-58) |
   | 6 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 7 | `blockStates` | No | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |

### /controlscheme

Sets or clears control scheme.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/controlscheme <players> set <control_scheme>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `set` | Yes | Static Enum (CameraControlSchemeSet) | Literal keyword. | `set`<br>[enum reference](#static-enum-cameracontrolschemeset-59) |
   | 3 | `control scheme` | Yes | Static Enum (controlscheme) | Value from static enum `controlscheme`. | `camera_relative_strafe`, `camera_relative`, `player_relative_strafe`, `player_relative`, `locked_player_relative_strafe`<br>[enum reference](#static-enum-controlscheme-61) |

2. `/controlscheme <players> clear`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `clear` | Yes | Static Enum (CameraControlSchemeClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-cameracontrolschemeclear-60) |

### /damage

Apply damage to the specified entities.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/damage <target> <amount> [<cause>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `amount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 3 | `cause` | No | Static Enum (DamageCause) | Value from static enum `DamageCause`. | `piston`, `lava`, `campfire`, `fire`, `anvil`, `magma`, `soul_campfire`, `wither`, `falling_block`, `fireworks` ... (36 total)<br>[enum reference](#static-enum-damagecause-62) |

2. `/damage <target> <amount> <cause> entity <damager>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `amount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 3 | `cause` | Yes | Static Enum (DamageCause) | Value from static enum `DamageCause`. | `piston`, `lava`, `campfire`, `fire`, `anvil`, `magma`, `soul_campfire`, `wither`, `falling_block`, `fireworks` ... (36 total)<br>[enum reference](#static-enum-damagecause-62) |
   | 4 | `origin` | Yes | Static Enum (DamageOriginActor) | Literal keyword. | `entity`<br>[enum reference](#static-enum-damageoriginactor-64) |
   | 5 | `damager` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /daylock

Locks and unlocks the day-night cycle.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

**Aliases:** `/alwaysday`

1. `/daylock [<lock>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `lock` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /deop

Revokes operator status from a player.

**Permission:** 2 (Admin) | **Flags:** 128 | **Overloads:** 1

1. `/deop <player>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /dialogue

Opens NPC dialogue for a player.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/dialogue open <npc> <player> [<sceneName>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `open` | Yes | Static Enum (DialogueOpenAction) | Literal keyword. | `open`<br>[enum reference](#static-enum-dialogueopenaction-66) |
   | 2 | `npc` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `sceneName` | No | String (id:56) | Single string token. | `example_text` |

2. `/dialogue change <npc> <sceneName> [<players>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `change` | Yes | Static Enum (DialogueChangeAction) | Literal keyword. | `change`<br>[enum reference](#static-enum-dialoguechangeaction-67) |
   | 2 | `npc` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `sceneName` | Yes | String (id:56) | Single string token. | `example_text` |
   | 4 | `players` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /difficulty

Sets the difficulty level.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/difficulty <difficulty>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `difficulty` | Yes | Static Enum (Difficulty) | Value from static enum `Difficulty`. | `normal`, `peaceful`, `easy`, `hard`, `p`, `e`, `n`, `h`<br>[enum reference](#static-enum-difficulty-68) |

2. `/difficulty <difficulty>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `difficulty` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /effect

Add or remove status effects.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 3

1. `/effect <player> clear [<effect>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `Mode` | Yes | Static Enum (ClearEffects) | Literal keyword. | `clear`<br>[enum reference](#static-enum-cleareffects-69) |
   | 3 | `effect` | No | Static Enum (Effect) | Value from static enum `Effect`. | `wither`, `speed`, `slowness`, `haste`, `mining_fatigue`, `strength`, `instant_health`, `instant_damage`, `jump_boost`, `nausea` ... (37 total)<br>[enum reference](#static-enum-effect-71) |

2. `/effect <player> <effect> [<seconds>] [<amplifier>] [<hideParticles>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `effect` | Yes | Static Enum (Effect) | Value from static enum `Effect`. | `wither`, `speed`, `slowness`, `haste`, `mining_fatigue`, `strength`, `instant_health`, `instant_damage`, `jump_boost`, `nausea` ... (37 total)<br>[enum reference](#static-enum-effect-71) |
   | 3 | `seconds` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `amplifier` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `hideParticles` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

3. `/effect <player> <effect> infinite [<amplifier>] [<hideParticles>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `effect` | Yes | Static Enum (Effect) | Value from static enum `Effect`. | `wither`, `speed`, `slowness`, `haste`, `mining_fatigue`, `strength`, `instant_health`, `instant_damage`, `jump_boost`, `nausea` ... (37 total)<br>[enum reference](#static-enum-effect-71) |
   | 3 | `Mode` | Yes | Static Enum (AddInfiniteEffect) | Literal keyword. | `infinite`<br>[enum reference](#static-enum-addinfiniteeffect-70) |
   | 4 | `amplifier` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `hideParticles` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /enchant

Adds an enchantment to a player's selected item.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/enchant <player> <enchantmentName> [<level>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `enchantmentName` | Yes | Static Enum (Enchant) | Value from static enum `Enchant`. | `protection`, `fire_protection`, `feather_falling`, `blast_protection`, `projectile_protection`, `thorns`, `respiration`, `depth_strider`, `aqua_affinity`, `sharpness` ... (42 total)<br>[enum reference](#static-enum-enchant-29) |
   | 3 | `level` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

2. `/enchant <player> <enchantmentId> [<level>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `enchantmentId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 3 | `level` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /event

Triggers an event for the specified object(s)

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/event entity <target> <eventName>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Static Enum (EventEntityAction) | Literal keyword. | `entity`<br>[enum reference](#static-enum-evententityaction-72) |
   | 2 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `eventName` | Yes | Dynamic Enum (EntityEvents) | Runtime or registry-backed value from dynamic enum `EntityEvents`. | `abort_sheltering`, `admire_item_started_event`, `admire_item_stopped_event`, `ageable_grow_up`, `attack_cooldown_complete_event`, `attacked`, `be_sheared`, `become_angry`, `become_angry_event`, `become_calm_event` ... (451 total)<br>[enum reference](#dynamic-enum-entityevents-7) |

### /execute

Executes a command on behalf of one or more entities.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 18

1. `/execute as <origin> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_As) | Literal keyword. | `as`<br>[enum reference](#static-enum-optionas-74) |
   | 2 | `origin` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

2. `/execute at <origin> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_At) | Literal keyword. | `at`<br>[enum reference](#static-enum-optionat-75) |
   | 2 | `origin` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

3. `/execute in <dimension> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_In) | Literal keyword. | `in`<br>[enum reference](#static-enum-optionin-76) |
   | 2 | `dimension` | Yes | Static Enum (Dimension) | Value from static enum `Dimension`. | `overworld`, `nether`, `the_end`<br>[enum reference](#static-enum-dimension-12) |
   | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

4. `/execute positioned <position> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Positioned) | Literal keyword. | `positioned`<br>[enum reference](#static-enum-optionpositioned-77) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

5. `/execute positioned as <origin> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Positioned) | Literal keyword. | `positioned`<br>[enum reference](#static-enum-optionpositioned-77) |
   | 2 | `secondary subcommand` | Yes | Static Enum (Option_As) | Literal keyword. | `as`<br>[enum reference](#static-enum-optionas-74) |
   | 3 | `origin` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

6. `/execute rotated <yaw> <pitch> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Rotated) | Literal keyword. | `rotated`<br>[enum reference](#static-enum-optionrotated-78) |
   | 2 | `yaw` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 3 | `pitch` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 4 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

7. `/execute rotated as <origin> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Rotated) | Literal keyword. | `rotated`<br>[enum reference](#static-enum-optionrotated-78) |
   | 2 | `secondary subcommand` | Yes | Static Enum (Option_As) | Literal keyword. | `as`<br>[enum reference](#static-enum-optionas-74) |
   | 3 | `origin` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

8. `/execute facing <position> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-optionfacing-79) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

9. `/execute facing entity <origin> <anchor> <command>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (Option_Facing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-optionfacing-79) |
   | 2 | `secondary subcommand` | Yes | Static Enum (Option_Entity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-optionentity-80) |
   | 3 | `origin` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `anchor` | Yes | Static Enum (ActorLocation) | Value from static enum `ActorLocation`. | `eyes`, `feet`<br>[enum reference](#static-enum-actorlocation-89) |
   | 5 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

10. `/execute align <axes> <command>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_Align) | Literal keyword. | `align`<br>[enum reference](#static-enum-optionalign-81) |
    | 2 | `axes` | Yes | String (id:56) | Single string token. | `example_text` |
    | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

11. `/execute anchored <anchored> <command>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_Anchored) | Literal keyword. | `anchored`<br>[enum reference](#static-enum-optionanchored-82) |
    | 2 | `anchored` | Yes | Static Enum (ActorLocation) | Value from static enum `ActorLocation`. | `eyes`, `feet`<br>[enum reference](#static-enum-actorlocation-89) |
    | 3 | `chainedCommand` | Yes | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

12. `/execute <subcommand> block <position> <block> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Block) | Literal keyword. | `block`<br>[enum reference](#static-enum-optionconditionblock-84) |
    | 3 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
    | 4 | `block` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
    | 5 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

13. `/execute <subcommand> block <position> <block> <blockStates> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Block) | Literal keyword. | `block`<br>[enum reference](#static-enum-optionconditionblock-84) |
    | 3 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
    | 4 | `block` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
    | 5 | `blockStates` | Yes | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |
    | 6 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

14. `/execute <subcommand> blocks <begin> <end> <destination> <scan_mode> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Blocks) | Literal keyword. | `blocks`<br>[enum reference](#static-enum-optionconditionblocks-85) |
    | 3 | `begin` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
    | 4 | `end` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
    | 5 | `destination` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
    | 6 | `scan mode` | Yes | Static Enum (BlocksScanMode) | Value from static enum `BlocksScanMode`. | `masked`, `all`<br>[enum reference](#static-enum-blocksscanmode-90) |
    | 7 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

15. `/execute <subcommand> entity <target> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Entity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-optionconditionentity-86) |
    | 3 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

16. `/execute <subcommand> score <target> <objective> <operation> <source> <objective> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Score) | Literal keyword. | `score`<br>[enum reference](#static-enum-optionconditionscore-87) |
    | 3 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
    | 5 | `operation` | Yes | Score Operator (id:7) | Score operation operator. | `+=`, `-=`, `*=`, `/=`, `%=`, `=`, `<`, `>`, `<>` |
    | 6 | `source` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 7 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
    | 8 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

17. `/execute <subcommand> score <target> <objective> matches <range> [<command>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_If_Unless) | Value from static enum `Option_If_Unless`. | `if`, `unless`<br>[enum reference](#static-enum-optionifunless-83) |
    | 2 | `secondary subcommand` | Yes | Static Enum (Option_Condition_Score) | Literal keyword. | `score`<br>[enum reference](#static-enum-optionconditionscore-87) |
    | 3 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
    | 5 | `matches` | Yes | Static Enum (ScoreRangeMode) | Literal keyword. | `matches`<br>[enum reference](#static-enum-scorerangemode-91) |
    | 6 | `range` | Yes | Range (id:23) | Range expression. | `10`, `5..`, `..20`, `5..20` |
    | 7 | `chainedCommand` | No | Command | Nested command to execute. | `/say hello`, `/tp @s ~ ~1 ~` |

18. `/execute run <command>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `subcommand` | Yes | Static Enum (Option_Run) | Literal keyword. | `run`<br>[enum reference](#static-enum-optionrun-88) |
    | 2 | `command` | Yes | Command (id:87) | Nested command string. | `/say hello` |

### /fill

Fills all or parts of a region with a specific block.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 4

1. `/fill <from> <to> <tileName> <blockStates> [<oldBlockHandling>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 4 | `blockStates` | Yes | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |
   | 5 | `oldBlockHandling` | No | Static Enum (FillMode) | Value from static enum `FillMode`. | `outline`, `hollow`, `destroy`, `keep`<br>[enum reference](#static-enum-fillmode-92) |

2. `/fill <from> <to> <tileName> [<oldBlockHandling>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 4 | `oldBlockHandling` | No | Static Enum (FillMode) | Value from static enum `FillMode`. | `outline`, `hollow`, `destroy`, `keep`<br>[enum reference](#static-enum-fillmode-92) |

3. `/fill <from> <to> <tileName> <blockStates> replace [<replaceTileName>] [<replaceBlockStates>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 4 | `blockStates` | Yes | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |
   | 5 | `oldBlockHandling` | Yes | Static Enum (Replace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-replace-93) |
   | 6 | `replaceTileName` | No | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 7 | `replaceBlockStates` | No | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |

4. `/fill <from> <to> <tileName> replace [<replaceTileName>] [<replaceBlockStates>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 4 | `oldBlockHandling` | Yes | Static Enum (Replace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-replace-93) |
   | 5 | `replaceTileName` | No | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 6 | `replaceBlockStates` | No | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |

### /fog

Add or remove fog settings file

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/fog <victim> push <fogId> <userProvidedId>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (add) | Literal keyword. | `push`<br>[enum reference](#static-enum-add-94) |
   | 3 | `fogId` | Yes | String (id:56) | Single string token. | `example_text` |
   | 4 | `userProvidedId` | Yes | String (id:56) | Single string token. | `example_text` |

2. `/fog <victim> <mode> <userProvidedId>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (delete) | Value from static enum `delete`. | `pop`, `remove`<br>[enum reference](#static-enum-delete-95) |
   | 3 | `userProvidedId` | Yes | String (id:56) | Single string token. | `example_text` |

### /function

Runs commands found in the corresponding function file.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/function <name>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `name` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

### /gamemode

Sets a player's game mode.

**Permission:** 1 (Game Directors) | **Flags:** 512 | **Overloads:** 2

1. `/gamemode <gameMode> [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `gameMode` | Yes | Static Enum (GameMode) | Value from static enum `GameMode`. | `default`, `creative`, `spectator`, `survival`, `adventure`, `d`, `c`, `s`, `a`<br>[enum reference](#static-enum-gamemode-0) |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

2. `/gamemode <gameMode> [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `gameMode` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /gamerule

Sets or queries a game rule value.

**Permission:** 1 (Game Directors) | **Flags:** 128 | **Overloads:** 3

1. `/gamerule`
   *No parameters.*
2. `/gamerule <rule> [<value>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `rule` | Yes | Static Enum (BoolGameRule) | Value from static enum `BoolGameRule`. | `commandblockoutput`, `dodaylightcycle`, `doentitydrops`, `dofiretick`, `recipesunlock`, `dolimitedcrafting`, `domobloot`, `domobspawning`, `dotiledrops`, `doweathercycle` ... (33 total)<br>[enum reference](#static-enum-boolgamerule-96) |
   | 2 | `value` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

3. `/gamerule <rule> [<value>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `rule` | Yes | Static Enum (IntGameRule) | Value from static enum `IntGameRule`. | `maxcommandchainlength`, `randomtickspeed`, `functioncommandlimit`, `spawnradius`, `playerssleepingpercentage`<br>[enum reference](#static-enum-intgamerule-97) |
   | 2 | `value` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /gametest

Interacts with gametest.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 10

1. `/gametest runthis`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeRunThis) | Literal keyword. | `runthis`<br>[enum reference](#static-enum-gametestmoderunthis-99) |

2. `/gametest run <testName> [<rotationSteps>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeRun) | Literal keyword. | `run`<br>[enum reference](#static-enum-gametestmoderun-98) |
   | 2 | `testName` | Yes | Dynamic Enum (GameTestName) | Runtime or registry-backed value from dynamic enum `GameTestName`. | [enum reference](#dynamic-enum-gametestname-9) |
   | 3 | `rotationSteps` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

3. `/gametest run <testName> <stopOnFailure> <repeatCount> [<rotationSteps>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeRun) | Literal keyword. | `run`<br>[enum reference](#static-enum-gametestmoderun-98) |
   | 2 | `testName` | Yes | Dynamic Enum (GameTestName) | Runtime or registry-backed value from dynamic enum `GameTestName`. | [enum reference](#dynamic-enum-gametestname-9) |
   | 3 | `stopOnFailure` | Yes | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 4 | `repeatCount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `rotationSteps` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

4. `/gametest runset [<tag>] [<rotationSteps>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeRunSet) | Literal keyword. | `runset`<br>[enum reference](#static-enum-gametestmoderunset-100) |
   | 2 | `tag` | No | Dynamic Enum (GameTestTag) | Runtime or registry-backed value from dynamic enum `GameTestTag`. | [enum reference](#dynamic-enum-gametesttag-10) |
   | 3 | `rotationSteps` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

5. `/gametest runsetuntilfail [<tag>] [<rotationSteps>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeRunSetUntilFail) | Literal keyword. | `runsetuntilfail`<br>[enum reference](#static-enum-gametestmoderunsetuntilfail-101) |
   | 2 | `tag` | No | Dynamic Enum (GameTestTag) | Runtime or registry-backed value from dynamic enum `GameTestTag`. | [enum reference](#dynamic-enum-gametesttag-10) |
   | 3 | `rotationSteps` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

6. `/gametest clearall`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeClearAll) | Literal keyword. | `clearall`<br>[enum reference](#static-enum-gametestmodeclearall-102) |

7. `/gametest pos`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeShowPosition) | Literal keyword. | `pos`<br>[enum reference](#static-enum-gametestmodeshowposition-103) |

8. `/gametest create <testName> [<width>] [<height>] [<depth>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestModeCreateTest) | Literal keyword. | `create`<br>[enum reference](#static-enum-gametestmodecreatetest-104) |
   | 2 | `testName` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `width` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `height` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `depth` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

9. `/gametest runthese`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (GameTestRunNearbyTests) | Literal keyword. | `runthese`<br>[enum reference](#static-enum-gametestrunnearbytests-105) |

10. `/gametest stopall`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `mode` | Yes | Static Enum (GameTestStopTests) | Literal keyword. | `stopall`<br>[enum reference](#static-enum-gameteststoptests-106) |

### /give

Gives an item to a player.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/give <player> <itemName> [<amount>] [<data>] [<components>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `itemName` | Yes | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 3 | `amount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `components` | No | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

### /hud

Changes the visibility of hud elements.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/hud <target> <visible> [<hud_element>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `visible` | Yes | Static Enum (HudVisibility) | Value from static enum `HudVisibility`. | `hide`, `reset`<br>[enum reference](#static-enum-hudvisibility-109) |
   | 3 | `hud_element` | No | Static Enum (HudElement) | Value from static enum `HudElement`. | `hunger`, `all`, `paperdoll`, `armor`, `tooltips`, `touch_controls`, `crosshair`, `hotbar`, `health`, `progress_bar` ... (14 total)<br>[enum reference](#static-enum-hudelement-108) |

### /inputpermission

Sets whether or not a player's input can affect their character.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/inputpermission set <targets> <permission> <state>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `option` | Yes | Static Enum (Option_Set) | Literal keyword. | `set`<br>[enum reference](#static-enum-optionset-110) |
   | 2 | `targets` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `permission` | Yes | Static Enum (permission) | Value from static enum `permission`. | `camera`, `movement`, `jump`, `lateral_movement`, `sneak`, `dismount`, `mount`, `move_backward`, `move_forward`, `move_left` ... (11 total)<br>[enum reference](#static-enum-permission-112) |
   | 4 | `state` | Yes | Static Enum (state) | Value from static enum `state`. | `enabled`, `disabled`<br>[enum reference](#static-enum-state-113) |

2. `/inputpermission query <targets> <permission> [<state>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `option` | Yes | Static Enum (Option_Query) | Literal keyword. | `query`<br>[enum reference](#static-enum-optionquery-111) |
   | 2 | `targets` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `permission` | Yes | Static Enum (permission) | Value from static enum `permission`. | `camera`, `movement`, `jump`, `lateral_movement`, `sneak`, `dismount`, `mount`, `move_backward`, `move_forward`, `move_left` ... (11 total)<br>[enum reference](#static-enum-permission-112) |
   | 4 | `state` | No | Static Enum (state) | Value from static enum `state`. | `enabled`, `disabled`<br>[enum reference](#static-enum-state-113) |

### /kick

Kicks a player from the server.

**Permission:** 1 (Game Directors) | **Flags:** 128 | **Overloads:** 1

1. `/kick <name> <reason>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `name` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `reason` | Yes | Message (id:68) | Greedy text message. | `hello world` |

### /kill

Kills entities (players, mobs, etc.).

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/kill [<target>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /list

Lists players on the server.

**Permission:** 0 (Any) | **Flags:** 128 | **Overloads:** 1

1. `/list`
   *No parameters.*

### /locate

Displays the coordinates for the closest structure or biome of a given type.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/locate structure <structure> [<useNewChunksOnly>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (LocateSubcommandStructure) | Literal keyword. | `structure`<br>[enum reference](#static-enum-locatesubcommandstructure-115) |
   | 2 | `structure` | Yes | Dynamic Enum (StructureFeature) | Runtime or registry-backed value from dynamic enum `StructureFeature`. | `minecraft:end_city`, `minecraft:fortress`, `minecraft:mineshaft`, `minecraft:monument`, `minecraft:stronghold`, `minecraft:temple`, `minecraft:village`, `minecraft:mansion`, `minecraft:shipwreck`, `minecraft:buried_treasure` ... (17 total)<br>[enum reference](#dynamic-enum-structurefeature-5) |
   | 3 | `useNewChunksOnly` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

2. `/locate biome <biome>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `subcommand` | Yes | Static Enum (LocateSubcommandBiome) | Literal keyword. | `biome`<br>[enum reference](#static-enum-locatesubcommandbiome-116) |
   | 2 | `biome` | Yes | Static Enum (Biome) | Value from static enum `Biome`. | `minecraft:ocean`, `minecraft:plains`, `minecraft:desert`, `minecraft:extreme_hills`, `minecraft:forest`, `minecraft:taiga`, `minecraft:swampland`, `minecraft:river`, `minecraft:hell`, `minecraft:the_end` ... (86 total)<br>[enum reference](#static-enum-biome-28) |

### /loot

Drops the given loot table into the specified inventory or into the world.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 21

1. `/loot spawn <position> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetSpawn) | Literal keyword. | `spawn`<br>[enum reference](#static-enum-targetspawn-117) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
   | 4 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

2. `/loot spawn <position> kill <entity> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetSpawn) | Literal keyword. | `spawn`<br>[enum reference](#static-enum-targetspawn-117) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
   | 4 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

3. `/loot spawn <position> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetSpawn) | Literal keyword. | `spawn`<br>[enum reference](#static-enum-targetspawn-117) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
   | 4 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

4. `/loot give <players> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetGive) | Literal keyword. | `give`<br>[enum reference](#static-enum-targetgive-118) |
   | 2 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
   | 4 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

5. `/loot give <players> kill <entity> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetGive) | Literal keyword. | `give`<br>[enum reference](#static-enum-targetgive-118) |
   | 2 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
   | 4 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

6. `/loot give <players> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetGive) | Literal keyword. | `give`<br>[enum reference](#static-enum-targetgive-118) |
   | 2 | `players` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
   | 4 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

7. `/loot insert <position> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetInsert) | Literal keyword. | `insert`<br>[enum reference](#static-enum-targetinsert-119) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
   | 4 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

8. `/loot insert <position> kill <entity> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetInsert) | Literal keyword. | `insert`<br>[enum reference](#static-enum-targetinsert-119) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
   | 4 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

9. `/loot insert <position> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Static Enum (TargetInsert) | Literal keyword. | `insert`<br>[enum reference](#static-enum-targetinsert-119) |
   | 2 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
   | 4 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 5 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

10. `/loot replace entity <entity> <slotType> <slotId> <count> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
    | 8 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

11. `/loot replace entity <entity> <slotType> <slotId> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
    | 7 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

12. `/loot replace entity <entity> <slotType> <slotId> <count> kill <entity> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
    | 8 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

13. `/loot replace entity <entity> <slotType> <slotId> kill <entity> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
    | 7 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

14. `/loot replace entity <entity> <slotType> <slotId> <count> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
    | 8 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

15. `/loot replace entity <entity> <slotType> <slotId> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `entity` | Yes | Static Enum (TargetEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-targetentity-121) |
    | 3 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
    | 7 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

16. `/loot replace block <position> slot.container <slotId> <count> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
    | 8 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

17. `/loot replace block <position> slot.container <slotId> loot <loot_table> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceLoot) | Literal keyword. | `loot`<br>[enum reference](#static-enum-sourceloot-123) |
    | 7 | `loot_table` | Yes | String (id:56) | Single string token. | `example_text` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

18. `/loot replace block <position> slot.container <slotId> <count> kill <entity> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
    | 8 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

19. `/loot replace block <position> slot.container <slotId> kill <entity> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceKill) | Literal keyword. | `kill`<br>[enum reference](#static-enum-sourcekill-124) |
    | 7 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

20. `/loot replace block <position> slot.container <slotId> <count> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 7 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
    | 8 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 9 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

21. `/loot replace block <position> slot.container <slotId> mine <TargetBlockPosition> [<tool_or_mainhand_or_offhand>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `target` | Yes | Static Enum (TargetReplace) | Literal keyword. | `replace`<br>[enum reference](#static-enum-targetreplace-120) |
    | 2 | `block` | Yes | Static Enum (TargetBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-targetblock-122) |
    | 3 | `position` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 4 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
    | 5 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
    | 6 | `source` | Yes | Static Enum (SourceMine) | Literal keyword. | `mine`<br>[enum reference](#static-enum-sourcemine-125) |
    | 7 | `TargetBlockPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
    | 8 | `<tool>\|mainhand\|offhand` | No | Dynamic Enum (Tool) | Runtime or registry-backed value from dynamic enum `Tool`. | `mainhand`, `offhand`, `minecraft:wooden_spear`, `minecraft:bow`, `minecraft:brain_coral_fan`, `minecraft:waxed_exposed_copper_bulb`, `minecraft:purpur_block`, `minecraft:cooked_cod`, `minecraft:music_disc_ward`, `minecraft:enderman_spawn_egg` ... (1907 total)<br>[enum reference](#dynamic-enum-tool-11) |

### /me

Displays a message about yourself.

**Permission:** 0 (Any) | **Flags:** 192 | **Overloads:** 1

1. `/me <message>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `message` | Yes | Message (id:68) | Greedy text message. | `hello world` |

### /mobevent

Controls what mob events are allowed to run.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/mobevent <event> [<value>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `event` | Yes | Static Enum (MobEvent) | Value from static enum `MobEvent`. | `minecraft:pillager_patrols_event`, `minecraft:wandering_trader_event`, `minecraft:ender_dragon_event`, `events_enabled`<br>[enum reference](#static-enum-mobevent-127) |
   | 2 | `value` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /music

Allows you to control playing music tracks.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 4

1. `/music queue <trackName> [<volume>] [<fadeSeconds>] [<repeatMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (MusicQueueAction) | Literal keyword. | `queue`<br>[enum reference](#static-enum-musicqueueaction-128) |
   | 2 | `trackName` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `volume` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 4 | `fadeSeconds` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `repeatMode` | No | Static Enum (MusicRepeatMode) | Value from static enum `MusicRepeatMode`. | `play_once`, `loop`<br>[enum reference](#static-enum-musicrepeatmode-132) |

2. `/music play <trackName> [<volume>] [<fadeSeconds>] [<repeatMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (MusicPlayAction) | Literal keyword. | `play`<br>[enum reference](#static-enum-musicplayaction-129) |
   | 2 | `trackName` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `volume` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 4 | `fadeSeconds` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `repeatMode` | No | Static Enum (MusicRepeatMode) | Value from static enum `MusicRepeatMode`. | `play_once`, `loop`<br>[enum reference](#static-enum-musicrepeatmode-132) |

3. `/music stop [<fadeSeconds>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (MusicStopAction) | Literal keyword. | `stop`<br>[enum reference](#static-enum-musicstopaction-130) |
   | 2 | `fadeSeconds` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

4. `/music volume <volume>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (MusicVolumeAction) | Literal keyword. | `volume`<br>[enum reference](#static-enum-musicvolumeaction-131) |
   | 2 | `volume` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

### /op

Grants operator status to a player.

**Permission:** 2 (Admin) | **Flags:** 128 | **Overloads:** 1

1. `/op <player>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /packstack

Prints client or server pack stack to chat

**Permission:** 0 (Any) | **Flags:** 128 | **Overloads:** 1

1. `/packstack <stackType> [verbose] [exclude-vanilla]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `stackType` | Yes | Static Enum (stackType) | Value from static enum `stackType`. | `server`, `client`<br>[enum reference](#static-enum-stacktype-133) |
   | 2 | `verbose` | No | Static Enum (verbose) | Literal keyword. | `verbose`<br>[enum reference](#static-enum-verbose-134) |
   | 3 | `exclude-vanilla` | No | Static Enum (exclude-vanilla) | Literal keyword. | `exclude-vanilla`<br>[enum reference](#static-enum-exclude-vanilla-135) |

### /particle

Creates a particle emitter

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/particle <effect> [<position>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `effect` | Yes | String (id:56) | Single string token. | `example_text` |
   | 2 | `position` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

### /permission

Reloads and applies permissions.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

**Aliases:** `/ops`

1. `/permission <action>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (PermissionsAction) | Value from static enum `PermissionsAction`. | `list`, `reload`<br>[enum reference](#static-enum-permissionsaction-136) |

### /place

Places a jigsaw structure, feature, or feature rule in the world.

**Permission:** 2 (Admin) | **Flags:** 0 | **Overloads:** 4

1. `/place structure <structure> [<pos>] [<ignoreStartHeight>] [<keepJigsaws>] [<includeEntities>] [<liquidSettings>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (PlaceStructureAction) | Literal keyword. | `structure`<br>[enum reference](#static-enum-placestructureaction-139) |
   | 2 | `structure` | Yes | Dynamic Enum (JigsawStructure) | Runtime or registry-backed value from dynamic enum `JigsawStructure`. | `minecraft:trail_ruins`, `minecraft:trial_chambers`<br>[enum reference](#dynamic-enum-jigsawstructure-6) |
   | 3 | `pos` | No | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `ignoreStartHeight` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 5 | `keepJigsaws` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 6 | `includeEntities` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 7 | `liquidSettings` | No | Static Enum (LiquidSettings) | Value from static enum `LiquidSettings`. | `apply_waterlogging`, `ignore_waterlogging`<br>[enum reference](#static-enum-liquidsettings-141) |

2. `/place jigsaw <pool> <jigsawTarget> <maxDepth> [<pos>] [<keepJigsaws>] [<includeEntities>] [<liquidSettings>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (PlaceJigsawAction) | Literal keyword. | `jigsaw`<br>[enum reference](#static-enum-placejigsawaction-140) |
   | 2 | `pool` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |
   | 3 | `jigsawTarget` | Yes | String (id:56) | Single string token. | `example_text` |
   | 4 | `maxDepth` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `pos` | No | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 6 | `keepJigsaws` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 7 | `includeEntities` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 8 | `liquidSettings` | No | Static Enum (LiquidSettings) | Value from static enum `LiquidSettings`. | `apply_waterlogging`, `ignore_waterlogging`<br>[enum reference](#static-enum-liquidsettings-141) |

3. `/place feature <feature> [<position>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (PlaceFeatureAction) | Literal keyword. | `feature`<br>[enum reference](#static-enum-placefeatureaction-142) |
   | 2 | `feature` | Yes | Static Enum (features) | Value from static enum `features`. | `minecraft:optional_log_mushrooms_feature`, `minecraft:copper_ore_feature`, `minecraft:fixup_mesa_gold_position_feature`, `minecraft:silverfish_feature`, `minecraft:grass_double_plant_upper_feature`, `minecraft:scatter_warm_ocean_seagrass_feature`, `minecraft:random_oak_tree_from_sapling_feature`, `minecraft:underground_extra_cave_carver_feature`, `minecraft:scatter_fern_feature`, `minecraft:dirt_feature` ... (240 total)<br>[enum reference](#static-enum-features-25) |
   | 3 | `position` | No | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |

4. `/place featurerule <featurerule> [<position>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (PlaceFeatureRuleAction) | Literal keyword. | `featurerule`<br>[enum reference](#static-enum-placefeatureruleaction-143) |
   | 2 | `featurerule` | Yes | Static Enum (featureRules) | Value from static enum `featureRules`. | `minecraft:warped_fungus_feature`, `minecraft:nether_cave_carver_feature`, `minecraft:sculk_vein_feature`, `minecraft:small_dripstone_feature`, `minecraft:crimson_roots_feature`, `minecraft:warped_roots_feature`, `minecraft:bamboo_jungle_after_surface_bamboo_feature`, `minecraft:crimson_fungus_warped_feature`, `minecraft:crimson_roots_warped_feature`, `minecraft:savanna_surface_flowers_feature` ... (165 total)<br>[enum reference](#static-enum-featurerules-144) |
   | 3 | `position` | No | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |

### /playanimation

Makes one or more entities play a one-off animation. Assumes all variables are setup correctly.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/playanimation <entity> <animation> [<next_state>] [<blend_out_time>] [<stop_expression>] [<controller>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `animation` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `next_state` | No | String (id:56) | Single string token. | `example_text` |
   | 4 | `blend_out_time` | No | Float (id:3) | Decimal number. Time value. | `0`, `1.5`, `-2.0` |
   | 5 | `stop_expression` | No | String (id:56) | Single string token. | `example_text` |
   | 6 | `controller` | No | String (id:56) | Single string token. | `example_text` |

### /playsound

Plays a sound.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/playsound <sound> [<player>] [<position>] [<volume>] [<pitch>] [<minimumVolume>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `sound` | Yes | String (id:56) | Single string token. | `example_text` |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `position` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 4 | `volume` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `pitch` | No | Float (id:3) | Decimal number. Rotation angle in degrees. | `0`, `1.5`, `-2.0` |
   | 6 | `minimumVolume` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |

### /recipe

Unlocks recipe in the recipe book for a player.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/recipe give <player> <recipe>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `give` | Yes | Static Enum (Give) | Literal keyword. | `give`<br>[enum reference](#static-enum-give-219) |
   | 2 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `recipe` | Yes | Dynamic Enum (UnlockableRecipeValues) | Runtime or registry-backed value from dynamic enum `UnlockableRecipeValues`. | `*`, `minecraft:copper_spear`, `minecraft:diamond_spear`, `minecraft:golden_spear`, `minecraft:iron_spear`, `minecraft:stone_spear`, `minecraft:wooden_spear`, `minecraft:acacia_shelf_from_stripped_acacia_log`, `minecraft:bamboo_shelf_from_stripped_bamboo_block`, `minecraft:birch_shelf_from_stripped_birch_log` ... (2757 total)<br>[enum reference](#dynamic-enum-unlockablerecipevalues-2) |

2. `/recipe take <player> <recipe>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `take` | Yes | Static Enum (Take) | Literal keyword. | `take`<br>[enum reference](#static-enum-take-218) |
   | 2 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `recipe` | Yes | Dynamic Enum (UnlockableRecipeValues) | Runtime or registry-backed value from dynamic enum `UnlockableRecipeValues`. | `*`, `minecraft:copper_spear`, `minecraft:diamond_spear`, `minecraft:golden_spear`, `minecraft:iron_spear`, `minecraft:stone_spear`, `minecraft:wooden_spear`, `minecraft:acacia_shelf_from_stripped_acacia_log`, `minecraft:bamboo_shelf_from_stripped_bamboo_block`, `minecraft:birch_shelf_from_stripped_birch_log` ... (2757 total)<br>[enum reference](#dynamic-enum-unlockablerecipevalues-2) |

### /reload

Reloads all function and script files from all behavior packs, or optionally reloads the world and all resource and behavior packs.

**Permission:** 2 (Admin) | **Flags:** 0 | **Overloads:** 1

1. `/reload [all]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `all` | No | Static Enum (reload_all) | Literal keyword. | `all`<br>[enum reference](#static-enum-reloadall-146) |

### /reloadconfig

Reloads configuration files relating to variables, secrets, permissions, etc.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

1. `/reloadconfig`
   *No parameters.*

### /reloadpacketlimitconfig

Reload packet limit config from file

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

1. `/reloadpacketlimitconfig`
   *No parameters.*

### /replaceitem

Replaces items in inventories.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 4

1. `/replaceitem block <position> slot.container <slotId> <itemName> [<amount>] [<data>] [<components>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `block` | Yes | Static Enum (ReplaceItemBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-replaceitemblock-147) |
   | 2 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
   | 4 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `itemName` | Yes | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 6 | `amount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 7 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 8 | `components` | No | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

2. `/replaceitem entity <target> <slotType> <slotId> <itemName> [<amount>] [<data>] [<components>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Static Enum (ReplaceItemEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-replaceitementity-148) |
   | 2 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
   | 4 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `itemName` | Yes | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 6 | `amount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 7 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 8 | `components` | No | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

3. `/replaceitem block <position> slot.container <slotId> <oldItemHandling> <itemName> [<amount>] [<data>] [<components>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `block` | Yes | Static Enum (ReplaceItemBlock) | Literal keyword. | `block`<br>[enum reference](#static-enum-replaceitemblock-147) |
   | 2 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `slotType` | Yes | Static Enum (BlockEquipmentSlot) | Literal keyword. | `slot.container`<br>[enum reference](#static-enum-blockequipmentslot-126) |
   | 4 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `oldItemHandling` | Yes | Static Enum (ReplaceMode) | Value from static enum `ReplaceMode`. | `destroy`, `keep`<br>[enum reference](#static-enum-replacemode-149) |
   | 6 | `itemName` | Yes | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 7 | `amount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 8 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 9 | `components` | No | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

4. `/replaceitem entity <target> <slotType> <slotId> <oldItemHandling> <itemName> [<amount>] [<data>] [<components>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Static Enum (ReplaceItemEntity) | Literal keyword. | `entity`<br>[enum reference](#static-enum-replaceitementity-148) |
   | 2 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 3 | `slotType` | Yes | Static Enum (EntityEquipmentSlot) | Value from static enum `EntityEquipmentSlot`. | `slot.weapon.mainhand`, `slot.weapon.offhand`, `slot.armor.head`, `slot.armor.chest`, `slot.armor.legs`, `slot.armor.feet`, `slot.armor.body`, `slot.hotbar`, `slot.inventory`, `slot.enderchest` ... (14 total)<br>[enum reference](#static-enum-entityequipmentslot-10) |
   | 4 | `slotId` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `oldItemHandling` | Yes | Static Enum (ReplaceMode) | Value from static enum `ReplaceMode`. | `destroy`, `keep`<br>[enum reference](#static-enum-replacemode-149) |
   | 6 | `itemName` | Yes | Static Enum (Item) | Value from static enum `Item`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:polished_basalt`, `polished_basalt`, `minecraft:nether_gold_ore`, `nether_gold_ore` ... (3399 total)<br>[enum reference](#static-enum-item-9) |
   | 7 | `amount` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 8 | `data` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 9 | `components` | No | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

### /ride

Makes entities ride other entities, stops entities from riding, makes rides evict their riders, or summons rides or riders.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 5

1. `/ride <riders> start_riding <ride> [<teleportRules>] [<howToFill>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `riders` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (RideModeStart) | Literal keyword. | `start_riding`<br>[enum reference](#static-enum-ridemodestart-150) |
   | 3 | `ride` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `teleportRules` | No | Static Enum (TeleportRules) | Value from static enum `TeleportRules`. | `teleport_rider`, `teleport_ride`<br>[enum reference](#static-enum-teleportrules-156) |
   | 5 | `howToFill` | No | Static Enum (FillType) | Value from static enum `FillType`. | `until_full`, `if_group_fits`<br>[enum reference](#static-enum-filltype-155) |

2. `/ride <riders> stop_riding`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `riders` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (RideModeStop) | Literal keyword. | `stop_riding`<br>[enum reference](#static-enum-ridemodestop-151) |

3. `/ride <rides> evict_riders`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `rides` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (RideModeEvict) | Literal keyword. | `evict_riders`<br>[enum reference](#static-enum-ridemodeevict-152) |

4. `/ride <rides> summon_rider <entityType> [<spawnEvent>] [<nameTag>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `rides` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (RideModeSummonRider) | Literal keyword. | `summon_rider`<br>[enum reference](#static-enum-ridemodesummonrider-153) |
   | 3 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 4 | `spawnEvent` | No | String (id:56) | Single string token. | `example_text` |
   | 5 | `nameTag` | No | String (id:56) | Single string token. | `example_text` |

5. `/ride <riders> summon_ride <entityType> [<rideRules>] [<spawnEvent>] [<nameTag>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `riders` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `mode` | Yes | Static Enum (RideModeSummonRide) | Literal keyword. | `summon_ride`<br>[enum reference](#static-enum-ridemodesummonride-154) |
   | 3 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 4 | `rideRules` | No | Static Enum (RideRules) | Value from static enum `RideRules`. | `no_ride_change`, `reassign_rides`, `skip_riders`<br>[enum reference](#static-enum-riderules-157) |
   | 5 | `spawnEvent` | No | String (id:56) | Single string token. | `example_text` |
   | 6 | `nameTag` | No | String (id:56) | Single string token. | `example_text` |

### /save

Control or check how the game saves data to disk.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

1. `/save <mode>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (SaveMode) | Value from static enum `SaveMode`. | `query`, `hold`, `resume`<br>[enum reference](#static-enum-savemode-243) |

### /say

Sends a message in the chat to other players.

**Permission:** 1 (Game Directors) | **Flags:** 192 | **Overloads:** 1

1. `/say <message>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `message` | Yes | Message (id:68) | Greedy text message. | `hello world` |

### /schedule

Schedules an action to be executed once an area is loaded, or after a certain amount of time.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 11

1. `/schedule delay add <function> <time> [<DelayMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionDelay) | Literal keyword. | `delay`<br>[enum reference](#static-enum-scheduleactiondelay-158) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |
   | 4 | `time` | Yes | Integer (id:1) | Whole number. Time value. | `0`, `1`, `-1` |
   | 5 | `DelayMode` | No | Static Enum (DelayMode) | Value from static enum `DelayMode`. | `replace`, `append`<br>[enum reference](#static-enum-delaymode-163) |

2. `/schedule delay add <function> <time> [<DelayMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionDelay) | Literal keyword. | `delay`<br>[enum reference](#static-enum-scheduleactiondelay-158) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |
   | 4 | `time` | Yes | Suffix Number (t) | Numeric value with suffix `t` (ticks). | `10t` |
   | 5 | `DelayMode` | No | Static Enum (DelayMode) | Value from static enum `DelayMode`. | `replace`, `append`<br>[enum reference](#static-enum-delaymode-163) |

3. `/schedule delay add <function> <time> [<DelayMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionDelay) | Literal keyword. | `delay`<br>[enum reference](#static-enum-scheduleactiondelay-158) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |
   | 4 | `time` | Yes | Suffix Number (s) | Numeric value with suffix `s` (seconds). | `10s` |
   | 5 | `DelayMode` | No | Static Enum (DelayMode) | Value from static enum `DelayMode`. | `replace`, `append`<br>[enum reference](#static-enum-delaymode-163) |

4. `/schedule delay add <function> <time> [<DelayMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionDelay) | Literal keyword. | `delay`<br>[enum reference](#static-enum-scheduleactiondelay-158) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |
   | 4 | `time` | Yes | Suffix Number (d) | Numeric value with suffix `d` (days). | `10d` |
   | 5 | `DelayMode` | No | Static Enum (DelayMode) | Value from static enum `DelayMode`. | `replace`, `append`<br>[enum reference](#static-enum-delaymode-163) |

5. `/schedule delay clear <function>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionDelay) | Literal keyword. | `delay`<br>[enum reference](#static-enum-scheduleactiondelay-158) |
   | 2 | `condition` | Yes | Static Enum (RequestActionClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-requestactionclear-162) |
   | 3 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

6. `/schedule clear <function>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-scheduleactionclear-160) |
   | 2 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

7. `/schedule on_area_loaded add <from> <to> <function>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionOnAreaLoaded) | Literal keyword. | `on_area_loaded`<br>[enum reference](#static-enum-scheduleactiononarealoaded-159) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 5 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

8. `/schedule on_area_loaded add circle <center> <radius> <function>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionOnAreaLoaded) | Literal keyword. | `on_area_loaded`<br>[enum reference](#static-enum-scheduleactiononarealoaded-159) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `type` | Yes | Static Enum (CircleArea) | Literal keyword. | `circle`<br>[enum reference](#static-enum-circlearea-164) |
   | 4 | `center` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 5 | `radius` | Yes | Integer (id:1) | Whole number. Radius value. | `0`, `1`, `-1` |
   | 6 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

9. `/schedule on_area_loaded add tickingarea <name> <function>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScheduleActionOnAreaLoaded) | Literal keyword. | `on_area_loaded`<br>[enum reference](#static-enum-scheduleactiononarealoaded-159) |
   | 2 | `condition` | Yes | Static Enum (RequestActionAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-requestactionadd-161) |
   | 3 | `type` | Yes | Static Enum (TickingArea) | Literal keyword. | `tickingarea`<br>[enum reference](#static-enum-tickingarea-165) |
   | 4 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 5 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

10. `/schedule on_area_loaded clear tickingarea <name> [<function>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `mode` | Yes | Static Enum (ScheduleActionOnAreaLoaded) | Literal keyword. | `on_area_loaded`<br>[enum reference](#static-enum-scheduleactiononarealoaded-159) |
    | 2 | `condition` | Yes | Static Enum (RequestActionClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-requestactionclear-162) |
    | 3 | `cleartype` | Yes | Static Enum (TickingAreaName) | Literal keyword. | `tickingarea`<br>[enum reference](#static-enum-tickingareaname-167) |
    | 4 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
    | 5 | `function` | No | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

11. `/schedule on_area_loaded clear function <function>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `mode` | Yes | Static Enum (ScheduleActionOnAreaLoaded) | Literal keyword. | `on_area_loaded`<br>[enum reference](#static-enum-scheduleactiononarealoaded-159) |
    | 2 | `condition` | Yes | Static Enum (RequestActionClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-requestactionclear-162) |
    | 3 | `cleartype` | Yes | Static Enum (FunctionName) | Literal keyword. | `function`<br>[enum reference](#static-enum-functionname-166) |
    | 4 | `function` | Yes | Function Name (id:17) | Behavior-pack function identifier. | `namespace:path/function` |

### /scoreboard

Tracks and displays scores for various objectives.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 11

1. `/scoreboard objectives add <objective> dummy [<displayName>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardObjectivesCategory) | Literal keyword. | `objectives`<br>[enum reference](#static-enum-scoreboardobjectivescategory-168) |
   | 2 | `action` | Yes | Static Enum (ScoreboardAddAction) | Literal keyword. | `add`<br>[enum reference](#static-enum-scoreboardaddaction-170) |
   | 3 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
   | 4 | `criteria` | Yes | Static Enum (ScoreboardCriteria) | Literal keyword. | `dummy`<br>[enum reference](#static-enum-scoreboardcriteria-182) |
   | 5 | `displayName` | No | String (id:56) | Single string token. | `example_text` |

2. `/scoreboard objectives remove <objective>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardObjectivesCategory) | Literal keyword. | `objectives`<br>[enum reference](#static-enum-scoreboardobjectivescategory-168) |
   | 2 | `action` | Yes | Static Enum (ScoreboardRemoveAction) | Literal keyword. | `remove`<br>[enum reference](#static-enum-scoreboardremoveaction-171) |
   | 3 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |

3. `/scoreboard objectives list`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardObjectivesCategory) | Literal keyword. | `objectives`<br>[enum reference](#static-enum-scoreboardobjectivescategory-168) |
   | 2 | `action` | Yes | Static Enum (ScoreboardListAction) | Literal keyword. | `list`<br>[enum reference](#static-enum-scoreboardlistaction-174) |

4. `/scoreboard objectives setdisplay <displaySlot> [<objective>] [<sortOrder>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardObjectivesCategory) | Literal keyword. | `objectives`<br>[enum reference](#static-enum-scoreboardobjectivescategory-168) |
   | 2 | `action` | Yes | Static Enum (ScoreboardSetDisplayAction) | Literal keyword. | `setdisplay`<br>[enum reference](#static-enum-scoreboardsetdisplayaction-173) |
   | 3 | `displaySlot` | Yes | Static Enum (ScoreboardDisplaySlotSortable) | Value from static enum `ScoreboardDisplaySlotSortable`. | `list`, `sidebar`<br>[enum reference](#static-enum-scoreboarddisplayslotsortable-180) |
   | 4 | `objective` | No | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
   | 5 | `sortOrder` | No | Static Enum (ScoreboardSortOrder) | Value from static enum `ScoreboardSortOrder`. | `ascending`, `descending`<br>[enum reference](#static-enum-scoreboardsortorder-179) |

5. `/scoreboard objectives setdisplay belowname [<objective>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardObjectivesCategory) | Literal keyword. | `objectives`<br>[enum reference](#static-enum-scoreboardobjectivescategory-168) |
   | 2 | `action` | Yes | Static Enum (ScoreboardSetDisplayAction) | Literal keyword. | `setdisplay`<br>[enum reference](#static-enum-scoreboardsetdisplayaction-173) |
   | 3 | `displaySlot` | Yes | Static Enum (ScoreboardDisplaySlotNonSortable) | Literal keyword. | `belowname`<br>[enum reference](#static-enum-scoreboarddisplayslotnonsortable-181) |
   | 4 | `objective` | No | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |

6. `/scoreboard players list [<playername>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
   | 2 | `action` | Yes | Static Enum (ScoreboardListAction) | Literal keyword. | `list`<br>[enum reference](#static-enum-scoreboardlistaction-174) |
   | 3 | `playername` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

7. `/scoreboard players reset <player> [<objective>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
   | 2 | `action` | Yes | Static Enum (ScoreboardResetAction) | Literal keyword. | `reset`<br>[enum reference](#static-enum-scoreboardresetaction-175) |
   | 3 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `objective` | No | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |

8. `/scoreboard players test <player> <objective> <min> [<max>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
   | 2 | `action` | Yes | Static Enum (ScoreboardTestAction) | Literal keyword. | `test`<br>[enum reference](#static-enum-scoreboardtestaction-176) |
   | 3 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
   | 5 | `min` | Yes | Integer (id:5) | Whole number (often score bounds). | `0`, `100` |
   | 6 | `max` | No | Integer (id:5) | Whole number (often score bounds). | `0`, `100` |

9. `/scoreboard players random <player> <objective> <min> <max>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
   | 2 | `action` | Yes | Static Enum (ScoreboardRandomAction) | Literal keyword. | `random`<br>[enum reference](#static-enum-scoreboardrandomaction-172) |
   | 3 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
   | 5 | `min` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 6 | `max` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

10. `/scoreboard players <action> <player> <objective> <count>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
    | 2 | `action` | Yes | Static Enum (ScoreboardPlayersNumAction) | Value from static enum `ScoreboardPlayersNumAction`. | `set`, `add`, `remove`<br>[enum reference](#static-enum-scoreboardplayersnumaction-177) |
    | 3 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
    | 5 | `count` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

11. `/scoreboard players operation <targetName> <targetObjective> <operation> <selector> <objective>`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `category` | Yes | Static Enum (ScoreboardPlayersCategory) | Literal keyword. | `players`<br>[enum reference](#static-enum-scoreboardplayerscategory-169) |
    | 2 | `action` | Yes | Static Enum (ScoreboardOperationAction) | Literal keyword. | `operation`<br>[enum reference](#static-enum-scoreboardoperationaction-178) |
    | 3 | `targetName` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 4 | `targetObjective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |
    | 5 | `operation` | Yes | Comparison Operator (id:6) | Comparison operator. | `<`, `<=`, `=`, `>=`, `>` |
    | 6 | `selector` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 7 | `objective` | Yes | Dynamic Enum (ScoreboardObjectives) | Runtime or registry-backed value from dynamic enum `ScoreboardObjectives`. | [enum reference](#dynamic-enum-scoreboardobjectives-0) |

### /sendshowstoreoffer

Sends a request to show a store offer to the target player.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 2

1. `/sendshowstoreoffer <player> <redirectType> <offerId>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `redirectType` | Yes | Static Enum (RedirectLocation) | Value from static enum `RedirectLocation`. | `marketplace`, `character`<br>[enum reference](#static-enum-redirectlocation-248) |
   | 3 | `offerId` | Yes | String (id:56) | Single string token. | `example_text` |

2. `/sendshowstoreoffer <player> server`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `redirectType` | Yes | Static Enum (3PServerOfferList) | Literal keyword. | `server`<br>[enum reference](#static-enum-3pserverofferlist-249) |

### /setblock

Changes a block to another block.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/setblock <position> <tileName> <blockStates> [<oldBlockHandling>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 3 | `blockStates` | Yes | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |
   | 4 | `oldBlockHandling` | No | Static Enum (SetBlockMode) | Value from static enum `SetBlockMode`. | `replace`, `destroy`, `keep`<br>[enum reference](#static-enum-setblockmode-183) |

2. `/setblock <position> <tileName> [<oldBlockHandling>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 3 | `oldBlockHandling` | No | Static Enum (SetBlockMode) | Value from static enum `SetBlockMode`. | `replace`, `destroy`, `keep`<br>[enum reference](#static-enum-setblockmode-183) |

### /setmaxplayers

Sets the maximum number of players for this game session.

**Permission:** 3 (Host) | **Flags:** 0 | **Overloads:** 1

1. `/setmaxplayers <maxPlayers>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `maxPlayers` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /setworldspawn

Sets the world spawn.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/setworldspawn [<spawnPoint>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `spawnPoint` | No | Position (id:65) | Coordinates (supports relative/local). | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

### /spawnpoint

Sets the spawn point for a player.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/spawnpoint [<player>] [<spawnPos>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `spawnPos` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

### /spreadplayers

Teleports entities to random locations.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/spreadplayers <x> <z> <spreadDistance> <maxRange> <victim> [<maxHeight>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `x` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). | `0`, `45`, `-90` |
   | 2 | `z` | Yes | Angle/Float (id:4) | Angle or decimal number (command-specific). | `0`, `45`, `-90` |
   | 3 | `spreadDistance` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 4 | `maxRange` | Yes | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 5 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 6 | `maxHeight` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). | `0`, `45`, `-90` |

### /stop

Stops the server.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

1. `/stop`
   *No parameters.*

### /stopsound

Stops a sound.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/stopsound <player> [<sound>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `sound` | No | String (id:56) | Single string token. | `example_text` |

### /structure

Saves or loads a structure in the world.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 5

1. `/structure save <name> <from> <to> [<saveMode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (StructureSaveAction) | Literal keyword. | `save`<br>[enum reference](#static-enum-structuresaveaction-184) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 5 | `saveMode` | No | Static Enum (StructureSaveMode) | Value from static enum `StructureSaveMode`. | `disk`, `memory`<br>[enum reference](#static-enum-structuresavemode-187) |

2. `/structure save <name> <from> <to> [<includeEntities>] [<saveMode>] [<includeBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (StructureSaveAction) | Literal keyword. | `save`<br>[enum reference](#static-enum-structuresaveaction-184) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 5 | `includeEntities` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 6 | `saveMode` | No | Static Enum (StructureSaveMode) | Value from static enum `StructureSaveMode`. | `disk`, `memory`<br>[enum reference](#static-enum-structuresavemode-187) |
   | 7 | `includeBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

3. `/structure delete <name>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (StructureDeleteAction) | Literal keyword. | `delete`<br>[enum reference](#static-enum-structuredeleteaction-186) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |

4. `/structure load <name> <to> [<rotation>] [<mirror>] [<includeEntities>] [<includeBlocks>] [<waterlogged>] [<integrity>] [<seed>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (StructureLoadAction) | Literal keyword. | `load`<br>[enum reference](#static-enum-structureloadaction-185) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `rotation` | No | Static Enum (Rotation) | Value from static enum `Rotation`. | `0_degrees`, `90_degrees`, `180_degrees`, `270_degrees`<br>[enum reference](#static-enum-rotation-30) |
   | 5 | `mirror` | No | Static Enum (Mirror) | Value from static enum `Mirror`. | `x`, `z`, `none`, `xz`<br>[enum reference](#static-enum-mirror-31) |
   | 6 | `includeEntities` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 7 | `includeBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 8 | `waterlogged` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 9 | `integrity` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 10 | `seed` | No | String (id:56) | Single string token. | `example_text` |

5. `/structure load <name> <to> [<rotation>] [<mirror>] [<animationMode>] [<animationSeconds>] [<includeEntities>] [<includeBlocks>] [<waterlogged>] [<integrity>] [<seed>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `action` | Yes | Static Enum (StructureLoadAction) | Literal keyword. | `load`<br>[enum reference](#static-enum-structureloadaction-185) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `rotation` | No | Static Enum (Rotation) | Value from static enum `Rotation`. | `0_degrees`, `90_degrees`, `180_degrees`, `270_degrees`<br>[enum reference](#static-enum-rotation-30) |
   | 5 | `mirror` | No | Static Enum (Mirror) | Value from static enum `Mirror`. | `x`, `z`, `none`, `xz`<br>[enum reference](#static-enum-mirror-31) |
   | 6 | `animationMode` | No | Static Enum (StructureAnimationMode) | Value from static enum `StructureAnimationMode`. | `block_by_block`, `layer_by_layer`<br>[enum reference](#static-enum-structureanimationmode-188) |
   | 7 | `animationSeconds` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 8 | `includeEntities` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 9 | `includeBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 10 | `waterlogged` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |
   | 11 | `integrity` | No | Float (id:3) | Decimal number. | `0`, `1.5`, `-2.0` |
   | 12 | `seed` | No | String (id:56) | Single string token. | `example_text` |

### /summon

Summons an entity.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 4

1. `/summon <entityType> [<spawnPos>] [<yRot>] [<xRot>] [<spawnEvent>] [<nameTag>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 2 | `spawnPos` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `yRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 4 | `xRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 5 | `spawnEvent` | No | Dynamic Enum (EntityEvents) | Runtime or registry-backed value from dynamic enum `EntityEvents`. | `abort_sheltering`, `admire_item_started_event`, `admire_item_stopped_event`, `ageable_grow_up`, `attack_cooldown_complete_event`, `attacked`, `be_sheared`, `become_angry`, `become_angry_event`, `become_calm_event` ... (451 total)<br>[enum reference](#dynamic-enum-entityevents-7) |
   | 6 | `nameTag` | No | String (id:56) | Single string token. | `example_text` |

2. `/summon <entityType> <nameTag> [<spawnPos>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 2 | `nameTag` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `spawnPos` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |

3. `/summon <entityType> [<spawnPos>] facing <lookAtPosition> [<spawnEvent>] [<nameTag>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 2 | `spawnPos` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 4 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 5 | `spawnEvent` | No | Dynamic Enum (EntityEvents) | Runtime or registry-backed value from dynamic enum `EntityEvents`. | `abort_sheltering`, `admire_item_started_event`, `admire_item_stopped_event`, `ageable_grow_up`, `attack_cooldown_complete_event`, `attacked`, `be_sheared`, `become_angry`, `become_angry_event`, `become_calm_event` ... (451 total)<br>[enum reference](#dynamic-enum-entityevents-7) |
   | 6 | `nameTag` | No | String (id:56) | Single string token. | `example_text` |

4. `/summon <entityType> [<spawnPos>] facing <lookAtEntity> [<spawnEvent>] [<nameTag>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entityType` | Yes | Static Enum (EntityType) | Value from static enum `EntityType`. | `minecraft:slime`, `slime`, `minecraft:tnt`, `tnt`, `minecraft:camel`, `minecraft:turtle`, `minecraft:chicken`, `minecraft:bee`, `minecraft:axolotl`, `minecraft:pig` ... (220 total)<br>[enum reference](#static-enum-entitytype-27) |
   | 2 | `spawnPos` | No | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 4 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 5 | `spawnEvent` | No | Dynamic Enum (EntityEvents) | Runtime or registry-backed value from dynamic enum `EntityEvents`. | `abort_sheltering`, `admire_item_started_event`, `admire_item_stopped_event`, `ageable_grow_up`, `attack_cooldown_complete_event`, `attacked`, `be_sheared`, `become_angry`, `become_angry_event`, `become_calm_event` ... (451 total)<br>[enum reference](#dynamic-enum-entityevents-7) |
   | 6 | `nameTag` | No | String (id:56) | Single string token. | `example_text` |

### /tag

Manages tags stored in entities.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/tag <entity> <action> <name>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `action` | Yes | Static Enum (TagChangeAction) | Value from static enum `TagChangeAction`. | `add`, `remove`<br>[enum reference](#static-enum-tagchangeaction-190) |
   | 3 | `name` | Yes | Dynamic Enum (TagValues) | Runtime or registry-backed value from dynamic enum `TagValues`. | [enum reference](#dynamic-enum-tagvalues-1) |

2. `/tag <entity> list`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `entity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `action` | Yes | Static Enum (TagListAction) | Literal keyword. | `list`<br>[enum reference](#static-enum-taglistaction-191) |

### /teleport

Teleports entities (players, mobs, etc.).

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 10

**Aliases:** `/tp`

1. `/teleport <destination> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 2 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

2. `/teleport <destination> [<yRot>] [<xRot>] [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 2 | `yRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 3 | `xRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 4 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

3. `/teleport <destination> facing <lookAtPosition> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 2 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 3 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 4 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

4. `/teleport <destination> facing <lookAtEntity> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 2 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 3 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 4 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

5. `/teleport <victim> <destination> [<yRot>] [<xRot>] [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `yRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 4 | `xRot` | No | Angle/Float (id:4) | Angle or decimal number (command-specific). Rotation angle in degrees. | `0`, `45`, `-90` |
   | 5 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

6. `/teleport <victim> <destination> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

7. `/teleport <victim> <destination> facing <lookAtPosition> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 4 | `lookAtPosition` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 5 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

8. `/teleport <victim> <destination> facing <lookAtEntity> [<checkForBlocks>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `destination` | Yes | Position (id:65) | Coordinates (supports relative/local). Coordinate argument. | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
   | 3 | `facing` | Yes | Static Enum (TeleportFacing) | Literal keyword. | `facing`<br>[enum reference](#static-enum-teleportfacing-189) |
   | 4 | `lookAtEntity` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 5 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

9. `/teleport <destination>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `destination` | Yes | Target (id:8) | Entity/player selector or player name. Coordinate argument. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

10. `/teleport <victim> <destination> [<checkForBlocks>]`
    | # | Parameter | Required | Type | Description | Candidates |
    | --- | --- | --- | --- | --- | --- |
    | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 2 | `destination` | Yes | Target (id:8) | Entity/player selector or player name. Coordinate argument. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
    | 3 | `checkForBlocks` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /tell

Sends a private message to one or more players.

**Permission:** 0 (Any) | **Flags:** 192 | **Overloads:** 1

**Aliases:** `/w`, `/msg`

1. `/tell <target> <message>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `message` | Yes | Message (id:68) | Greedy text message. | `hello world` |

### /tellraw

Sends a JSON message to players.

**Permission:** 1 (Game Directors) | **Flags:** 192 | **Overloads:** 1

1. `/tellraw <target> <raw_json_message>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `target` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `raw json message` | Yes | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

### /testfor

Counts entities (players, mobs, items, etc.) matching specified conditions.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/testfor <victim>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `victim` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

### /testforblock

Tests whether a certain block is in a specific location.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/testforblock <position> <tileName> [<blockStates>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `tileName` | Yes | Static Enum (Block) | Value from static enum `Block`. | `minecraft:cyan_terracotta`, `cyan_terracotta`, `minecraft:blue_candle`, `blue_candle`, `minecraft:dark_oak_wood`, `dark_oak_wood`, `minecraft:birch_standing_sign`, `birch_standing_sign`, `minecraft:polished_basalt`, `polished_basalt` ... (2650 total)<br>[enum reference](#static-enum-block-24) |
   | 3 | `blockStates` | No | Block States (id:84) | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |

### /testforblocks

Tests whether the blocks in two regions match.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/testforblocks <begin> <end> <destination> [<mode>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `begin` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 2 | `end` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `destination` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `mode` | No | Static Enum (TestForBlocksMode) | Value from static enum `TestForBlocksMode`. | `masked`, `all`<br>[enum reference](#static-enum-testforblocksmode-194) |

### /tickingarea

Add, remove, or list ticking areas.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 8

1. `/tickingarea add <from> <to> [<name>] [<preload>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-tickingareamodeadd-195) |
   | 2 | `from` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `to` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `name` | No | String (id:56) | Single string token. | `example_text` |
   | 5 | `preload` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

2. `/tickingarea add circle <center> <radius> [<name>] [<preload>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-tickingareamodeadd-195) |
   | 2 | `circle` | Yes | Static Enum (AddTickingAreaType) | Literal keyword. | `circle`<br>[enum reference](#static-enum-addtickingareatype-200) |
   | 3 | `center` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 4 | `radius` | Yes | Integer (id:1) | Whole number. Radius value. | `0`, `1`, `-1` |
   | 5 | `name` | No | String (id:56) | Single string token. | `example_text` |
   | 6 | `preload` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

3. `/tickingarea remove <position>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeRemove) | Literal keyword. | `remove`<br>[enum reference](#static-enum-tickingareamoderemove-196) |
   | 2 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |

4. `/tickingarea remove <name>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeRemove) | Literal keyword. | `remove`<br>[enum reference](#static-enum-tickingareamoderemove-196) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |

5. `/tickingarea remove_all`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeRemoveAll) | Literal keyword. | `remove_all`<br>[enum reference](#static-enum-tickingareamoderemoveall-197) |

6. `/tickingarea list [all-dimensions]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModeList) | Literal keyword. | `list`<br>[enum reference](#static-enum-tickingareamodelist-198) |
   | 2 | `all-dimensions` | No | Static Enum (AllDimensions) | Literal keyword. | `all-dimensions`<br>[enum reference](#static-enum-alldimensions-201) |

7. `/tickingarea preload <position> [<preload>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModePreload) | Literal keyword. | `preload`<br>[enum reference](#static-enum-tickingareamodepreload-199) |
   | 2 | `position` | Yes | Block Position (id:64) | Block coordinates (integer x y z). Coordinate argument. | `~ ~ ~`, `100 64 -30` |
   | 3 | `preload` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

8. `/tickingarea preload <name> [<preload>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TickingAreaModePreload) | Literal keyword. | `preload`<br>[enum reference](#static-enum-tickingareamodepreload-199) |
   | 2 | `name` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `preload` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /time

Changes or queries the world's game time.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 4

1. `/time add <amount>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TimeModeAdd) | Literal keyword. | `add`<br>[enum reference](#static-enum-timemodeadd-203) |
   | 2 | `amount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

2. `/time set <amount>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TimeModeSet) | Literal keyword. | `set`<br>[enum reference](#static-enum-timemodeset-202) |
   | 2 | `amount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

3. `/time set <time>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TimeModeSet) | Literal keyword. | `set`<br>[enum reference](#static-enum-timemodeset-202) |
   | 2 | `time` | Yes | Static Enum (TimeSpec) | Value from static enum `TimeSpec`. Time value. | `day`, `sunrise`, `noon`, `sunset`, `night`, `midnight`<br>[enum reference](#static-enum-timespec-206) |

4. `/time query <time>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (TimeModeQuery) | Literal keyword. | `query`<br>[enum reference](#static-enum-timemodequery-204) |
   | 2 | `time` | Yes | Static Enum (TimeQuery) | Value from static enum `TimeQuery`. Time value. | `daytime`, `gametime`, `day`<br>[enum reference](#static-enum-timequery-205) |

### /title

Controls screen titles.

**Permission:** 1 (Game Directors) | **Flags:** 64 | **Overloads:** 4

1. `/title <player> clear`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `clear` | Yes | Static Enum (TitleClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-titleclear-207) |

2. `/title <player> reset`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `reset` | Yes | Static Enum (TitleReset) | Literal keyword. | `reset`<br>[enum reference](#static-enum-titlereset-208) |

3. `/title <player> <titleLocation> <titleText>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `titleLocation` | Yes | Static Enum (TitleSet) | Value from static enum `TitleSet`. | `title`, `subtitle`, `actionbar`<br>[enum reference](#static-enum-titleset-209) |
   | 3 | `titleText` | Yes | Message (id:68) | Greedy text message. | `hello world` |

4. `/title <player> times <fadeIn> <stay> <fadeOut>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `times` | Yes | Static Enum (TitleTimes) | Literal keyword. Time value. | `times`<br>[enum reference](#static-enum-titletimes-210) |
   | 3 | `fadeIn` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `stay` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `fadeOut` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /titleraw

Controls screen titles with JSON messages.

**Permission:** 1 (Game Directors) | **Flags:** 64 | **Overloads:** 4

1. `/titleraw <player> clear`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `clear` | Yes | Static Enum (TitleRawClear) | Literal keyword. | `clear`<br>[enum reference](#static-enum-titlerawclear-211) |

2. `/titleraw <player> reset`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `reset` | Yes | Static Enum (TitleRawReset) | Literal keyword. | `reset`<br>[enum reference](#static-enum-titlerawreset-212) |

3. `/titleraw <player> <titleLocation> <raw_json_titleText>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `titleLocation` | Yes | Static Enum (TitleRawSet) | Value from static enum `TitleRawSet`. | `title`, `subtitle`, `actionbar`<br>[enum reference](#static-enum-titlerawset-213) |
   | 3 | `raw json titleText` | Yes | JSON (id:74) | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |

4. `/titleraw <player> times <fadeIn> <stay> <fadeOut>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `times` | Yes | Static Enum (TitleRawTimes) | Literal keyword. Time value. | `times`<br>[enum reference](#static-enum-titlerawtimes-214) |
   | 3 | `fadeIn` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 4 | `stay` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 5 | `fadeOut` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /toggledownfall

Toggles the weather.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/toggledownfall`
   *No parameters.*

### /transfer

Transfers a player to another server.

**Permission:** 4 (Owner) | **Flags:** 0 | **Overloads:** 1

1. `/transfer <pfidOrMSA> <server> [<port>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `pfidOrMSA` | Yes | String (id:56) | Single string token. | `example_text` |
   | 2 | `server` | Yes | String (id:56) | Single string token. | `example_text` |
   | 3 | `port` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

### /weather

Sets the weather.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/weather <type> [<duration>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `type` | Yes | Static Enum (WeatherType) | Value from static enum `WeatherType`. | `clear`, `rain`, `thunder`<br>[enum reference](#static-enum-weathertype-215) |
   | 2 | `duration` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

2. `/weather query`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `query` | Yes | Static Enum (WeatherQuery) | Literal keyword. | `query`<br>[enum reference](#static-enum-weatherquery-216) |

### /xp

Adds or removes player experience.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/xp <amount> [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `amount` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

2. `/xp <amount> [<player>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `amount` | Yes | Suffix Number (l) | Numeric value with suffix `l` (levels). | `10l` |
   | 2 | `player` | No | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |

## WebSocket / Script Integration Commands

These commands are related to script events/debugging or websocket connectivity.

### /script

Script debugger commands.

**Permission:** 2 (Admin) | **Flags:** 32 | **Overloads:** 7

1. `/script debugger listen <port>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeDebugger) | Literal keyword. | `debugger`<br>[enum reference](#static-enum-scriptdebugmodedebugger-14) |
   | 2 | `action` | Yes | Static Enum (ScriptDebuggerListen) | Literal keyword. | `listen`<br>[enum reference](#static-enum-scriptdebuggerlisten-15) |
   | 3 | `port` | Yes | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

2. `/script debugger connect [<host>] [<port>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeDebugger) | Literal keyword. | `debugger`<br>[enum reference](#static-enum-scriptdebugmodedebugger-14) |
   | 2 | `action` | Yes | Static Enum (ScriptDebuggerConnect) | Literal keyword. | `connect`<br>[enum reference](#static-enum-scriptdebuggerconnect-16) |
   | 3 | `host` | No | String (id:56) | Single string token. | `example_text` |
   | 4 | `port` | No | Integer (id:1) | Whole number. | `0`, `1`, `-1` |

3. `/script debugger close`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeDebugger) | Literal keyword. | `debugger`<br>[enum reference](#static-enum-scriptdebugmodedebugger-14) |
   | 2 | `action` | Yes | Static Enum (ScriptDebuggerClose) | Literal keyword. | `close`<br>[enum reference](#static-enum-scriptdebuggerclose-17) |

4. `/script profiler start`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeProfiler) | Literal keyword. | `profiler`<br>[enum reference](#static-enum-scriptdebugmodeprofiler-18) |
   | 2 | `action` | Yes | Static Enum (ScriptProfilerStart) | Literal keyword. | `start`<br>[enum reference](#static-enum-scriptprofilerstart-19) |

5. `/script profiler stop`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeProfiler) | Literal keyword. | `profiler`<br>[enum reference](#static-enum-scriptdebugmodeprofiler-18) |
   | 2 | `action` | Yes | Static Enum (ScriptProfilerStop) | Literal keyword. | `stop`<br>[enum reference](#static-enum-scriptprofilerstop-20) |

6. `/script diagnostics startcapture`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeDiagnostics) | Literal keyword. | `diagnostics`<br>[enum reference](#static-enum-scriptdebugmodediagnostics-21) |
   | 2 | `action` | Yes | Static Enum (ScriptDiagnosticsStartCapture) | Literal keyword. | `startcapture`<br>[enum reference](#static-enum-scriptdiagnosticsstartcapture-22) |

7. `/script diagnostics stopcapture`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `mode` | Yes | Static Enum (ScriptDebugModeDiagnostics) | Literal keyword. | `diagnostics`<br>[enum reference](#static-enum-scriptdebugmodediagnostics-21) |
   | 2 | `action` | Yes | Static Enum (ScriptDiagnosticsStopCapture) | Literal keyword. | `stopcapture`<br>[enum reference](#static-enum-scriptdiagnosticsstopcapture-23) |

### /scriptevent

Triggers a script event with an ID and message.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/scriptevent <messageId> <message>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `messageId` | Yes | String (id:56) | Single string token. | `example_text` |
   | 2 | `message` | Yes | Message (id:68) | Greedy text message. | `hello world` |

### /wsserver

Attempts to connect to the websocket server on the provided URL.

**Permission:** 2 (Admin) | **Flags:** 32 | **Overloads:** 1

**Aliases:** `/connect`

1. `/wsserver <serverUri>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `serverUri` | Yes | URL (id:70) | URI value. | `ws://127.0.0.1:19131` |

## Education Edition-only Commands

The following commands are documented separately because they are Education Edition-limited commands.

### /ability

Sets a player's ability.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 2

1. `/ability <player> <ability> <value>`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `ability` | Yes | Static Enum (Ability) | Value from static enum `Ability`. | `mayfly`, `mute`, `worldbuilder`<br>[enum reference](#static-enum-ability-220) |
   | 3 | `value` | Yes | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

2. `/ability <player> [<ability>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `player` | Yes | Target (id:8) | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
   | 2 | `ability` | No | Static Enum (Ability) | Value from static enum `Ability`. | `mayfly`, `mute`, `worldbuilder`<br>[enum reference](#static-enum-ability-220) |

### /immutableworld

Sets the immutable state of the world.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

1. `/immutableworld [<value>]`
   | # | Parameter | Required | Type | Description | Candidates |
   | --- | --- | --- | --- | --- | --- |
   | 1 | `value` | No | Static Enum (Boolean) | Value from static enum `Boolean`. | `true`, `false`<br>[enum reference](#static-enum-boolean-5) |

### /worldbuilder

Toggle World Builder status of caller.

**Permission:** 1 (Game Directors) | **Flags:** 0 | **Overloads:** 1

**Aliases:** `/wb`

1. `/worldbuilder`
   *No parameters.*

## Primitive Parameter Type Legend

| Parser ID | Type | Description | Examples |
| --- | --- | --- | --- |
| 1 | Integer | Whole number. | `0`, `1`, `-1` |
| 3 | Float | Decimal number. | `0`, `1.5`, `-2.0` |
| 4 | Angle/Float | Angle or decimal number (command-specific). | `0`, `45`, `-90` |
| 5 | Integer | Whole number (often score bounds). | `0`, `100` |
| 6 | Comparison Operator | Comparison operator. | `<`, `<=`, `=`, `>=`, `>` |
| 7 | Score Operator | Score operation operator. | `+=`, `-=`, `*=`, `/=`, `%=`, `=`, `<`, `>`, `<>` |
| 8 | Target | Entity/player selector or player name. | `@s`, `@p`, `@a`, `@e[type=zombie]`, `PlayerName` |
| 17 | Function Name | Behavior-pack function identifier. | `namespace:path/function` |
| 23 | Range | Range expression. | `10`, `5..`, `..20`, `5..20` |
| 56 | String | Single string token. | `example_text` |
| 64 | Block Position | Block coordinates (integer x y z). | `~ ~ ~`, `100 64 -30` |
| 65 | Position | Coordinates (supports relative/local). | `~ ~ ~`, `^ ^ ^`, `100.5 64 -30.25` |
| 68 | Message | Greedy text message. | `hello world` |
| 70 | URL | URI value. | `ws://127.0.0.1:19131` |
| 74 | JSON | JSON object/string (components or raw text payload). | `{"text":"Hello"}` |
| 84 | Block States | Block state expression. | `["facing_direction"=2]`, `{"facing_direction":2}` |
| 87 | Command | Nested command string. | `/say hello` |

## Enum Candidate Appendix

### Static Enums Used by Commands

#### Static Enum: GameMode (#0)

Value count: 9

<details>
<summary>Show all values</summary>

```
default
creative
spectator
survival
adventure
d
c
s
a
```

</details>

#### Static Enum: Boolean (#5)

Value count: 2

<details>
<summary>Show all values</summary>

```
true
false
```

</details>

#### Static Enum: Item (#9)

Value count: 3399

<details>
<summary>Show all values</summary>

```
minecraft:cyan_terracotta
cyan_terracotta
minecraft:blue_candle
blue_candle
minecraft:dark_oak_wood
dark_oak_wood
minecraft:polished_basalt
polished_basalt
minecraft:nether_gold_ore
nether_gold_ore
minecraft:zombie_head
zombie_head
minecraft:waxed_weathered_copper_chain
waxed_weathered_copper_chain
minecraft:waxed_weathered_copper_chest
waxed_weathered_copper_chest
minecraft:leaf_litter
leaf_litter
minecraft:warped_door
warped_door
minecraft:light_blue_concrete_powder
light_blue_concrete_powder
minecraft:bamboo_block
bamboo_block
minecraft:waxed_oxidized_chiseled_copper
waxed_oxidized_chiseled_copper
minecraft:wet_sponge
wet_sponge
minecraft:end_stone_brick_wall
end_stone_brick_wall
minecraft:granite
granite
minecraft:blue_stained_glass_pane
blue_stained_glass_pane
minecraft:fence_gate
fence_gate
minecraft:birch_shelf
birch_shelf
minecraft:dark_oak_button
dark_oak_button
minecraft:deepslate_copper_ore
deepslate_copper_ore
minecraft:chiseled_stone_bricks
chiseled_stone_bricks
minecraft:nether_brick_stairs
nether_brick_stairs
minecraft:yellow_shulker_box
yellow_shulker_box
minecraft:lime_stained_glass
lime_stained_glass
minecraft:red_wool
red_wool
minecraft:jungle_button
jungle_button
minecraft:spruce_stairs
spruce_stairs
minecraft:acacia_shelf
acacia_shelf
minecraft:diorite
diorite
minecraft:pale_oak_fence_gate
pale_oak_fence_gate
minecraft:polished_tuff_slab
polished_tuff_slab
minecraft:cherry_pressure_plate
cherry_pressure_plate
minecraft:cherry_hanging_sign
cherry_hanging_sign
minecraft:yellow_wool
yellow_wool
minecraft:yellow_stained_glass_pane
yellow_stained_glass_pane
minecraft:azure_bluet
azure_bluet
minecraft:beacon
beacon
minecraft:red_nether_brick
red_nether_brick
minecraft:brick_wall
brick_wall
minecraft:cobbled_deepslate_stairs
cobbled_deepslate_stairs
minecraft:smooth_sandstone
smooth_sandstone
minecraft:snow_layer
snow_layer
minecraft:black_candle
black_candle
minecraft:blue_carpet
blue_carpet
minecraft:glow_frame
glow_frame
minecraft:hanging_roots
hanging_roots
minecraft:red_sandstone_wall
red_sandstone_wall
minecraft:prismarine_bricks_stairs
prismarine_bricks_stairs
minecraft:waxed_oxidized_cut_copper
waxed_oxidized_cut_copper
minecraft:waxed_exposed_copper_chain
waxed_exposed_copper_chain
minecraft:waxed_exposed_copper_chest
waxed_exposed_copper_chest
minecraft:calcite
calcite
minecraft:diorite_slab
diorite_slab
minecraft:stripped_dark_oak_log
stripped_dark_oak_log
minecraft:dead_bubble_coral_fan
dead_bubble_coral_fan
minecraft:jungle_log
jungle_log
minecraft:bubble_coral_fan
bubble_coral_fan
minecraft:sculk_shrieker
sculk_shrieker
minecraft:gray_wool
gray_wool
minecraft:orange_stained_glass_pane
orange_stained_glass_pane
minecraft:gray_carpet
gray_carpet
minecraft:lily_of_the_valley
lily_of_the_valley
minecraft:lime_glazed_terracotta
lime_glazed_terracotta
minecraft:trapdoor
trapdoor
minecraft:cactus_flower
cactus_flower
minecraft:dead_brain_coral_fan
dead_brain_coral_fan
minecraft:seagrass
seagrass
minecraft:tube_coral_fan
tube_coral_fan
minecraft:waxed_exposed_cut_copper_slab
waxed_exposed_cut_copper_slab
minecraft:redstone_lamp
redstone_lamp
minecraft:mossy_cobblestone
mossy_cobblestone
minecraft:deepslate
deepslate
minecraft:magenta_carpet
magenta_carpet
minecraft:brown_wool
brown_wool
minecraft:waxed_exposed_chiseled_copper
waxed_exposed_chiseled_copper
minecraft:tuff_slab
tuff_slab
minecraft:warped_pressure_plate
warped_pressure_plate
minecraft:stripped_acacia_wood
stripped_acacia_wood
minecraft:firefly_bush
firefly_bush
minecraft:diamond_block
diamond_block
minecraft:oak_stairs
oak_stairs
minecraft:oak_log
oak_log
minecraft:brown_stained_glass_pane
brown_stained_glass_pane
minecraft:end_bricks
end_bricks
minecraft:magenta_shulker_box
magenta_shulker_box
minecraft:packed_ice
packed_ice
minecraft:packed_mud
packed_mud
minecraft:moss_carpet
moss_carpet
minecraft:warped_fungus
warped_fungus
minecraft:oxidized_lightning_rod
oxidized_lightning_rod
minecraft:polished_deepslate_slab
polished_deepslate_slab
minecraft:bamboo_door
bamboo_door
minecraft:amethyst_block
amethyst_block
minecraft:gold_block
gold_block
minecraft:flower_pot
flower_pot
minecraft:chiseled_bookshelf
chiseled_bookshelf
minecraft:polished_deepslate_stairs
polished_deepslate_stairs
minecraft:lime_shulker_box
lime_shulker_box
minecraft:weathered_chiseled_copper
weathered_chiseled_copper
minecraft:small_amethyst_bud
small_amethyst_bud
minecraft:activator_rail
activator_rail
minecraft:iron_trapdoor
iron_trapdoor
minecraft:muddy_mangrove_roots
muddy_mangrove_roots
minecraft:pale_oak_pressure_plate
pale_oak_pressure_plate
minecraft:stripped_jungle_wood
stripped_jungle_wood
minecraft:noteblock
noteblock
minecraft:tuff
tuff
minecraft:mangrove_log
mangrove_log
minecraft:oxidized_cut_copper_stairs
oxidized_cut_copper_stairs
minecraft:pale_oak_fence
pale_oak_fence
minecraft:pale_oak_leaves
pale_oak_leaves
minecraft:sandstone_slab
sandstone_slab
minecraft:mossy_stone_brick_slab
mossy_stone_brick_slab
minecraft:raw_gold_block
raw_gold_block
minecraft:allium
allium
minecraft:white_shulker_box
white_shulker_box
minecraft:copper_grate
copper_grate
minecraft:black_wool
black_wool
minecraft:orange_candle
orange_candle
minecraft:jungle_fence
jungle_fence
minecraft:spruce_fence
spruce_fence
minecraft:dark_oak_sapling
dark_oak_sapling
minecraft:melon_block
melon_block
minecraft:black_concrete_powder
black_concrete_powder
minecraft:waxed_cut_copper_stairs
waxed_cut_copper_stairs
minecraft:open_eyeblossom
open_eyeblossom
minecraft:mob_spawner
mob_spawner
minecraft:pale_oak_sapling
pale_oak_sapling
minecraft:polished_granite
polished_granite
minecraft:magenta_candle
magenta_candle
minecraft:light_gray_stained_glass
light_gray_stained_glass
minecraft:obsidian
obsidian
minecraft:light_gray_stained_glass_pane
light_gray_stained_glass_pane
minecraft:dark_oak_slab
dark_oak_slab
minecraft:deepslate_brick_wall
deepslate_brick_wall
minecraft:waxed_exposed_copper_grate
waxed_exposed_copper_grate
minecraft:exposed_copper
exposed_copper
minecraft:waxed_copper_bars
waxed_copper_bars
minecraft:stone_button
stone_button
minecraft:waxed_copper_bulb
waxed_copper_bulb
minecraft:sponge
sponge
minecraft:bamboo_fence
bamboo_fence
minecraft:normal_stone_stairs
normal_stone_stairs
minecraft:end_stone_brick_slab
end_stone_brick_slab
minecraft:hardened_clay
hardened_clay
minecraft:birch_hanging_sign
birch_hanging_sign
minecraft:stripped_jungle_log
stripped_jungle_log
minecraft:oxidized_copper_golem_statue
oxidized_copper_golem_statue
minecraft:light_block_9
light_block_9
minecraft:light_block_8
light_block_8
minecraft:light_block_7
light_block_7
minecraft:light_block_6
light_block_6
minecraft:light_block_5
light_block_5
minecraft:light_block_4
light_block_4
minecraft:light_block_3
light_block_3
minecraft:light_block_2
light_block_2
minecraft:light_block_1
light_block_1
minecraft:light_block_0
light_block_0
minecraft:pale_oak_door
pale_oak_door
minecraft:oak_sapling
oak_sapling
minecraft:light_gray_terracotta
light_gray_terracotta
minecraft:smoker
smoker
minecraft:brown_stained_glass
brown_stained_glass
minecraft:andesite
andesite
minecraft:fire_coral
fire_coral
minecraft:stone
stone
minecraft:smooth_sandstone_slab
smooth_sandstone_slab
minecraft:birch_log
birch_log
minecraft:tuff_brick_wall
tuff_brick_wall
minecraft:purpur_slab
purpur_slab
minecraft:brain_coral
brain_coral
minecraft:stripped_spruce_wood
stripped_spruce_wood
minecraft:orange_wool
orange_wool
minecraft:respawn_anchor
respawn_anchor
minecraft:light_gray_concrete
light_gray_concrete
minecraft:green_candle
green_candle
minecraft:waxed_exposed_copper
waxed_exposed_copper
minecraft:birch_wood
birch_wood
minecraft:red_sand
red_sand
minecraft:hay_block
hay_block
minecraft:jungle_wood
jungle_wood
minecraft:waxed_weathered_copper
waxed_weathered_copper
minecraft:infested_cracked_stone_bricks
infested_cracked_stone_bricks
minecraft:waxed_oxidized_cut_copper_slab
waxed_oxidized_cut_copper_slab
minecraft:oak_leaves
oak_leaves
minecraft:resin_clump
resin_clump
minecraft:brain_coral_fan
brain_coral_fan
minecraft:polished_tuff_wall
polished_tuff_wall
minecraft:bamboo_stairs
bamboo_stairs
minecraft:infested_mossy_stone_bricks
infested_mossy_stone_bricks
minecraft:torch
torch
minecraft:mud_brick_wall
mud_brick_wall
minecraft:honey_block
honey_block
minecraft:underwater_tnt
underwater_tnt
minecraft:dripstone_block
dripstone_block
minecraft:vine
vine
minecraft:red_sandstone_slab
red_sandstone_slab
minecraft:cherry_trapdoor
cherry_trapdoor
minecraft:blackstone_slab
blackstone_slab
minecraft:gold_ore
gold_ore
minecraft:yellow_glazed_terracotta
yellow_glazed_terracotta
minecraft:dried_ghast
dried_ghast
minecraft:warped_planks
warped_planks
minecraft:piston
piston
minecraft:brown_carpet
brown_carpet
minecraft:stone_brick_stairs
stone_brick_stairs
minecraft:dead_bubble_coral_block
dead_bubble_coral_block
minecraft:gray_candle
gray_candle
minecraft:cherry_fence
cherry_fence
minecraft:mangrove_planks
mangrove_planks
minecraft:red_terracotta
red_terracotta
minecraft:diorite_wall
diorite_wall
minecraft:dead_fire_coral_block
dead_fire_coral_block
minecraft:oxidized_copper_bulb
oxidized_copper_bulb
minecraft:magenta_wool
magenta_wool
minecraft:oxidized_copper_bars
oxidized_copper_bars
minecraft:magenta_glazed_terracotta
magenta_glazed_terracotta
minecraft:polished_blackstone_brick_wall
polished_blackstone_brick_wall
minecraft:mangrove_slab
mangrove_slab
minecraft:orange_glazed_terracotta
orange_glazed_terracotta
minecraft:smooth_basalt
smooth_basalt
minecraft:waterlily
waterlily
minecraft:stripped_pale_oak_wood
stripped_pale_oak_wood
minecraft:emerald_block
emerald_block
minecraft:suspicious_sand
suspicious_sand
minecraft:mossy_cobblestone_wall
mossy_cobblestone_wall
minecraft:heavy_weighted_pressure_plate
heavy_weighted_pressure_plate
minecraft:purple_stained_glass
purple_stained_glass
minecraft:lightning_rod
lightning_rod
minecraft:acacia_leaves
acacia_leaves
minecraft:black_stained_glass_pane
black_stained_glass_pane
minecraft:cobblestone_wall
cobblestone_wall
minecraft:bamboo_mosaic_slab
bamboo_mosaic_slab
minecraft:dark_oak_log
dark_oak_log
minecraft:acacia_hanging_sign
acacia_hanging_sign
minecraft:ochre_froglight
ochre_froglight
minecraft:tuff_wall
tuff_wall
minecraft:observer
observer
minecraft:redstone_torch
redstone_torch
minecraft:silver_glazed_terracotta
silver_glazed_terracotta
minecraft:granite_stairs
granite_stairs
minecraft:pink_concrete
pink_concrete
minecraft:dark_oak_hanging_sign
dark_oak_hanging_sign
minecraft:brown_mushroom
brown_mushroom
minecraft:cyan_concrete_powder
cyan_concrete_powder
minecraft:brown_glazed_terracotta
brown_glazed_terracotta
minecraft:waxed_copper_trapdoor
waxed_copper_trapdoor
minecraft:spruce_shelf
spruce_shelf
minecraft:oxidized_copper
oxidized_copper
minecraft:copper_ore
copper_ore
minecraft:dark_oak_planks
dark_oak_planks
minecraft:birch_pressure_plate
birch_pressure_plate
minecraft:scaffolding
scaffolding
minecraft:sandstone_stairs
sandstone_stairs
minecraft:stripped_bamboo_block
stripped_bamboo_block
minecraft:red_mushroom_block
red_mushroom_block
minecraft:cracked_stone_bricks
cracked_stone_bricks
minecraft:sculk_catalyst
sculk_catalyst
minecraft:cobblestone
cobblestone
minecraft:waxed_lightning_rod
waxed_lightning_rod
minecraft:horn_coral
horn_coral
minecraft:yellow_concrete
yellow_concrete
minecraft:mangrove_shelf
mangrove_shelf
minecraft:cyan_carpet
cyan_carpet
minecraft:warped_shelf
warped_shelf
minecraft:smooth_sandstone_stairs
smooth_sandstone_stairs
minecraft:jungle_pressure_plate
jungle_pressure_plate
minecraft:blue_terracotta
blue_terracotta
minecraft:sandstone
sandstone
minecraft:light_weighted_pressure_plate
light_weighted_pressure_plate
minecraft:undyed_shulker_box
undyed_shulker_box
minecraft:polished_blackstone
polished_blackstone
minecraft:mycelium
mycelium
minecraft:exposed_lightning_rod
exposed_lightning_rod
minecraft:bamboo
bamboo
minecraft:quartz_block
quartz_block
minecraft:pale_oak_planks
pale_oak_planks
minecraft:stone_stairs
stone_stairs
minecraft:waxed_weathered_chiseled_copper
waxed_weathered_chiseled_copper
minecraft:gray_stained_glass
gray_stained_glass
minecraft:green_terracotta
green_terracotta
minecraft:deepslate_brick_slab
deepslate_brick_slab
minecraft:warped_stairs
warped_stairs
minecraft:smithing_table
smithing_table
minecraft:player_head
player_head
minecraft:weathered_copper_grate
weathered_copper_grate
minecraft:poppy
poppy
minecraft:tuff_brick_slab
tuff_brick_slab
minecraft:copper_chain
copper_chain
minecraft:copper_chest
copper_chest
minecraft:mossy_stone_bricks
mossy_stone_bricks
minecraft:green_wool
green_wool
minecraft:green_carpet
green_carpet
minecraft:prismarine_brick_slab
prismarine_brick_slab
minecraft:wooden_door
wooden_door
minecraft:pitcher_plant
pitcher_plant
minecraft:compound_creator
compound_creator
minecraft:spruce_pressure_plate
spruce_pressure_plate
minecraft:netherite_block
netherite_block
minecraft:pink_wool
pink_wool
minecraft:redstone_block
redstone_block
minecraft:birch_fence_gate
birch_fence_gate
minecraft:quartz_pillar
quartz_pillar
minecraft:waxed_exposed_cut_copper
waxed_exposed_cut_copper
minecraft:jungle_hanging_sign
jungle_hanging_sign
minecraft:birch_slab
birch_slab
minecraft:loom
loom
minecraft:waxed_weathered_copper_lantern
waxed_weathered_copper_lantern
minecraft:dead_tube_coral_block
dead_tube_coral_block
minecraft:end_stone
end_stone
minecraft:crimson_door
crimson_door
minecraft:mangrove_pressure_plate
mangrove_pressure_plate
minecraft:jungle_shelf
jungle_shelf
minecraft:jungle_slab
jungle_slab
minecraft:light_blue_stained_glass_pane
light_blue_stained_glass_pane
minecraft:glowstone
glowstone
minecraft:stone_pressure_plate
stone_pressure_plate
minecraft:waxed_exposed_cut_copper_stairs
waxed_exposed_cut_copper_stairs
minecraft:mud_brick_slab
mud_brick_slab
minecraft:waxed_exposed_lightning_rod
waxed_exposed_lightning_rod
minecraft:exposed_copper_lantern
exposed_copper_lantern
minecraft:farmland
farmland
minecraft:cut_red_sandstone
cut_red_sandstone
minecraft:rail
rail
minecraft:blackstone_wall
blackstone_wall
minecraft:stone_bricks
stone_bricks
minecraft:mossy_cobblestone_stairs
mossy_cobblestone_stairs
minecraft:detector_rail
detector_rail
minecraft:blue_orchid
blue_orchid
minecraft:green_stained_glass_pane
green_stained_glass_pane
minecraft:polished_granite_stairs
polished_granite_stairs
minecraft:birch_leaves
birch_leaves
minecraft:pink_terracotta
pink_terracotta
minecraft:infested_cobblestone
infested_cobblestone
minecraft:cracked_deepslate_tiles
cracked_deepslate_tiles
minecraft:mangrove_wood
mangrove_wood
minecraft:waxed_exposed_copper_golem_statue
waxed_exposed_copper_golem_statue
minecraft:red_glazed_terracotta
red_glazed_terracotta
minecraft:waxed_oxidized_copper_chest
waxed_oxidized_copper_chest
minecraft:waxed_oxidized_copper_chain
waxed_oxidized_copper_chain
minecraft:dark_oak_fence_gate
dark_oak_fence_gate
minecraft:mossy_cobblestone_slab
mossy_cobblestone_slab
minecraft:cobblestone_slab
cobblestone_slab
minecraft:crimson_nylium
crimson_nylium
minecraft:structure_void
structure_void
minecraft:waxed_exposed_copper_bars
waxed_exposed_copper_bars
minecraft:purple_concrete
purple_concrete
minecraft:waxed_exposed_copper_bulb
waxed_exposed_copper_bulb
minecraft:polished_blackstone_brick_slab
polished_blackstone_brick_slab
minecraft:normal_stone_slab
normal_stone_slab
minecraft:spruce_sapling
spruce_sapling
minecraft:yellow_terracotta
yellow_terracotta
minecraft:snow
snow
minecraft:sand
sand
minecraft:daylight_detector
daylight_detector
minecraft:stripped_mangrove_wood
stripped_mangrove_wood
minecraft:conduit
conduit
minecraft:slime
slime
minecraft:copper_torch
copper_torch
minecraft:bone_block
bone_block
minecraft:frame
frame
minecraft:spruce_log
spruce_log
minecraft:lapis_block
lapis_block
minecraft:coal_ore
coal_ore
minecraft:bamboo_shelf
bamboo_shelf
minecraft:redstone_ore
redstone_ore
minecraft:waxed_copper_chest
waxed_copper_chest
minecraft:green_stained_glass
green_stained_glass
minecraft:waxed_copper_chain
waxed_copper_chain
minecraft:bubble_coral_block
bubble_coral_block
minecraft:infested_chiseled_stone_bricks
infested_chiseled_stone_bricks
minecraft:nether_brick_fence
nether_brick_fence
minecraft:pink_tulip
pink_tulip
minecraft:oak_slab
oak_slab
minecraft:stripped_pale_oak_log
stripped_pale_oak_log
minecraft:deepslate_tile_slab
deepslate_tile_slab
minecraft:pink_concrete_powder
pink_concrete_powder
minecraft:pale_oak_slab
pale_oak_slab
minecraft:dead_tube_coral
dead_tube_coral
minecraft:nether_wart_block
nether_wart_block
minecraft:prismarine_slab
prismarine_slab
minecraft:cherry_door
cherry_door
minecraft:crimson_hyphae
crimson_hyphae
minecraft:polished_blackstone_stairs
polished_blackstone_stairs
minecraft:weathered_cut_copper_stairs
weathered_cut_copper_stairs
minecraft:small_dripleaf_block
small_dripleaf_block
minecraft:pink_stained_glass
pink_stained_glass
minecraft:waxed_weathered_copper_grate
waxed_weathered_copper_grate
minecraft:spruce_button
spruce_button
minecraft:acacia_log
acacia_log
minecraft:crimson_trapdoor
crimson_trapdoor
minecraft:basalt
basalt
minecraft:light_blue_terracotta
light_blue_terracotta
minecraft:copper_golem_statue
copper_golem_statue
minecraft:diamond_ore
diamond_ore
minecraft:warped_roots
warped_roots
minecraft:magenta_concrete
magenta_concrete
minecraft:dark_prismarine
dark_prismarine
minecraft:sticky_piston
sticky_piston
minecraft:ender_chest
ender_chest
minecraft:medium_amethyst_bud
medium_amethyst_bud
minecraft:pink_shulker_box
pink_shulker_box
minecraft:sculk_sensor
sculk_sensor
minecraft:copper_bulb
copper_bulb
minecraft:copper_bars
copper_bars
minecraft:oak_shelf
oak_shelf
minecraft:diorite_stairs
diorite_stairs
minecraft:spruce_leaves
spruce_leaves
minecraft:frog_spawn
frog_spawn
minecraft:acacia_door
acacia_door
minecraft:red_shulker_box
red_shulker_box
minecraft:stripped_cherry_log
stripped_cherry_log
minecraft:crimson_button
crimson_button
minecraft:acacia_planks
acacia_planks
minecraft:fire_coral_block
fire_coral_block
minecraft:magenta_concrete_powder
magenta_concrete_powder
minecraft:iron_door
iron_door
minecraft:honeycomb_block
honeycomb_block
minecraft:polished_blackstone_brick_stairs
polished_blackstone_brick_stairs
minecraft:mangrove_trapdoor
mangrove_trapdoor
minecraft:quartz_ore
quartz_ore
minecraft:barrel
barrel
minecraft:smooth_quartz
smooth_quartz
minecraft:coarse_dirt
coarse_dirt
minecraft:chorus_flower
chorus_flower
minecraft:orange_stained_glass
orange_stained_glass
minecraft:white_stained_glass_pane
white_stained_glass_pane
minecraft:stripped_birch_wood
stripped_birch_wood
minecraft:cracked_nether_bricks
cracked_nether_bricks
minecraft:light_blue_candle
light_blue_candle
minecraft:pumpkin
pumpkin
minecraft:element_constructor
element_constructor
minecraft:deepslate_tiles
deepslate_tiles
minecraft:smooth_stone
smooth_stone
minecraft:gray_terracotta
gray_terracotta
minecraft:oxidized_copper_trapdoor
oxidized_copper_trapdoor
minecraft:granite_slab
granite_slab
minecraft:white_tulip
white_tulip
minecraft:lime_concrete
lime_concrete
minecraft:red_mushroom
red_mushroom
minecraft:gilded_blackstone
gilded_blackstone
minecraft:magenta_terracotta
magenta_terracotta
minecraft:exposed_cut_copper_stairs
exposed_cut_copper_stairs
minecraft:mangrove_stairs
mangrove_stairs
minecraft:polished_diorite_slab
polished_diorite_slab
minecraft:cut_copper_stairs
cut_copper_stairs
minecraft:lab_table
lab_table
minecraft:waxed_oxidized_copper_lantern
waxed_oxidized_copper_lantern
minecraft:cherry_button
cherry_button
minecraft:mangrove_fence_gate
mangrove_fence_gate
minecraft:sunflower
sunflower
minecraft:pink_petals
pink_petals
minecraft:bamboo_hanging_sign
bamboo_hanging_sign
minecraft:infested_deepslate
infested_deepslate
minecraft:soul_torch
soul_torch
minecraft:podzol
podzol
minecraft:copper_block
copper_block
minecraft:deepslate_tile_stairs
deepslate_tile_stairs
minecraft:crimson_fence_gate
crimson_fence_gate
minecraft:deadbush
deadbush
minecraft:polished_blackstone_bricks
polished_blackstone_bricks
minecraft:red_candle
red_candle
minecraft:cut_copper
cut_copper
minecraft:waxed_weathered_copper_golem_statue
waxed_weathered_copper_golem_statue
minecraft:iron_ore
iron_ore
minecraft:spruce_door
spruce_door
minecraft:frosted_ice
frosted_ice
minecraft:chipped_anvil
chipped_anvil
minecraft:large_amethyst_bud
large_amethyst_bud
minecraft:exposed_copper_door
exposed_copper_door
minecraft:suspicious_gravel
suspicious_gravel
minecraft:warped_trapdoor
warped_trapdoor
minecraft:brick_block
brick_block
minecraft:waxed_weathered_copper_trapdoor
waxed_weathered_copper_trapdoor
minecraft:quartz_stairs
quartz_stairs
minecraft:magenta_stained_glass_pane
magenta_stained_glass_pane
minecraft:iron_bars
iron_bars
minecraft:white_terracotta
white_terracotta
minecraft:stripped_oak_wood
stripped_oak_wood
minecraft:light_blue_carpet
light_blue_carpet
minecraft:oak_hanging_sign
oak_hanging_sign
minecraft:white_concrete_powder
white_concrete_powder
minecraft:crimson_planks
crimson_planks
minecraft:stripped_dark_oak_wood
stripped_dark_oak_wood
minecraft:waxed_weathered_cut_copper
waxed_weathered_cut_copper
minecraft:white_stained_glass
white_stained_glass
minecraft:oak_wood
oak_wood
minecraft:purple_stained_glass_pane
purple_stained_glass_pane
minecraft:waxed_oxidized_copper_trapdoor
waxed_oxidized_copper_trapdoor
minecraft:jukebox
jukebox
minecraft:stripped_cherry_wood
stripped_cherry_wood
minecraft:jigsaw
jigsaw
minecraft:waxed_oxidized_copper_golem_statue
waxed_oxidized_copper_golem_statue
minecraft:prismarine_wall
prismarine_wall
minecraft:border_block
border_block
minecraft:shroomlight
shroomlight
minecraft:bamboo_fence_gate
bamboo_fence_gate
minecraft:cornflower
cornflower
minecraft:chiseled_polished_blackstone
chiseled_polished_blackstone
minecraft:dark_oak_stairs
dark_oak_stairs
minecraft:deepslate_tile_wall
deepslate_tile_wall
minecraft:glass_pane
glass_pane
minecraft:chiseled_deepslate
chiseled_deepslate
minecraft:cut_copper_slab
cut_copper_slab
minecraft:red_stained_glass
red_stained_glass
minecraft:pale_oak_wood
pale_oak_wood
minecraft:infested_stone_bricks
infested_stone_bricks
minecraft:acacia_pressure_plate
acacia_pressure_plate
minecraft:weathered_lightning_rod
weathered_lightning_rod
minecraft:bamboo_trapdoor
bamboo_trapdoor
minecraft:oxidized_chiseled_copper
oxidized_chiseled_copper
minecraft:raw_copper_block
raw_copper_block
minecraft:tall_dry_grass
tall_dry_grass
minecraft:oxidized_cut_copper_slab
oxidized_cut_copper_slab
minecraft:horn_coral_block
horn_coral_block
minecraft:dark_oak_shelf
dark_oak_shelf
minecraft:beetroot
beetroot
minecraft:white_candle
white_candle
minecraft:andesite_stairs
andesite_stairs
minecraft:birch_planks
birch_planks
minecraft:golden_rail
golden_rail
minecraft:cyan_wool
cyan_wool
minecraft:jungle_leaves
jungle_leaves
minecraft:gray_shulker_box
gray_shulker_box
minecraft:red_sandstone_stairs
red_sandstone_stairs
minecraft:cyan_glazed_terracotta
cyan_glazed_terracotta
minecraft:cracked_deepslate_bricks
cracked_deepslate_bricks
minecraft:jungle_fence_gate
jungle_fence_gate
minecraft:exposed_copper_grate
exposed_copper_grate
minecraft:waxed_copper_grate
waxed_copper_grate
minecraft:jungle_trapdoor
jungle_trapdoor
minecraft:dirt_with_roots
dirt_with_roots
minecraft:coal_block
coal_block
minecraft:white_wool
white_wool
minecraft:warped_fence_gate
warped_fence_gate
minecraft:cut_sandstone_slab
cut_sandstone_slab
minecraft:skeleton_skull
skeleton_skull
minecraft:exposed_copper_chest
exposed_copper_chest
minecraft:exposed_copper_chain
exposed_copper_chain
minecraft:composter
composter
minecraft:kelp
kelp
minecraft:waxed_exposed_copper_door
waxed_exposed_copper_door
minecraft:deepslate_bricks
deepslate_bricks
minecraft:blue_glazed_terracotta
blue_glazed_terracotta
minecraft:light_blue_glazed_terracotta
light_blue_glazed_terracotta
minecraft:rose_bush
rose_bush
minecraft:flowering_azalea
flowering_azalea
minecraft:oxidized_cut_copper
oxidized_cut_copper
minecraft:blue_wool
blue_wool
minecraft:pale_oak_hanging_sign
pale_oak_hanging_sign
minecraft:weeping_vines
weeping_vines
minecraft:chorus_plant
chorus_plant
minecraft:mud_brick_stairs
mud_brick_stairs
minecraft:stone_brick_wall
stone_brick_wall
minecraft:smooth_red_sandstone_stairs
smooth_red_sandstone_stairs
minecraft:element_100
element_100
minecraft:element_101
element_101
minecraft:element_102
element_102
minecraft:element_103
element_103
minecraft:element_104
element_104
minecraft:element_105
element_105
minecraft:element_106
element_106
minecraft:element_107
element_107
minecraft:element_108
element_108
minecraft:element_109
element_109
minecraft:element_113
element_113
minecraft:element_112
element_112
minecraft:element_111
element_111
minecraft:element_110
element_110
minecraft:element_117
element_117
minecraft:element_116
element_116
minecraft:element_115
element_115
minecraft:element_114
element_114
minecraft:element_118
element_118
minecraft:andesite_wall
andesite_wall
minecraft:white_glazed_terracotta
white_glazed_terracotta
minecraft:stripped_warped_hyphae
stripped_warped_hyphae
minecraft:trapped_chest
trapped_chest
minecraft:acacia_trapdoor
acacia_trapdoor
minecraft:weathered_copper_chest
weathered_copper_chest
minecraft:brain_coral_block
brain_coral_block
minecraft:weathered_copper_chain
weathered_copper_chain
minecraft:bamboo_planks
bamboo_planks
minecraft:glow_lichen
glow_lichen
minecraft:purpur_pillar
purpur_pillar
minecraft:twisting_vines
twisting_vines
minecraft:chiseled_copper
chiseled_copper
minecraft:dark_oak_door
dark_oak_door
minecraft:oak_fence
oak_fence
minecraft:pale_moss_block
pale_moss_block
minecraft:soul_lantern
soul_lantern
minecraft:dirt
dirt
minecraft:blue_stained_glass
blue_stained_glass
minecraft:deny
deny
minecraft:bee_nest
bee_nest
minecraft:campfire
campfire
minecraft:light_blue_stained_glass
light_blue_stained_glass
minecraft:soul_soil
soul_soil
minecraft:soul_sand
soul_sand
minecraft:granite_wall
granite_wall
minecraft:spruce_hanging_sign
spruce_hanging_sign
minecraft:polished_diorite
polished_diorite
minecraft:reinforced_deepslate
reinforced_deepslate
minecraft:fletching_table
fletching_table
minecraft:cherry_leaves
cherry_leaves
minecraft:creeper_head
creeper_head
minecraft:black_glazed_terracotta
black_glazed_terracotta
minecraft:waxed_oxidized_cut_copper_stairs
waxed_oxidized_cut_copper_stairs
minecraft:waxed_weathered_copper_bulb
waxed_weathered_copper_bulb
minecraft:dragon_head
dragon_head
minecraft:waxed_weathered_copper_bars
waxed_weathered_copper_bars
minecraft:calibrated_sculk_sensor
calibrated_sculk_sensor
minecraft:dark_prismarine_slab
dark_prismarine_slab
minecraft:copper_trapdoor
copper_trapdoor
minecraft:stripped_acacia_log
stripped_acacia_log
minecraft:warped_fence
warped_fence
minecraft:crafting_table
crafting_table
minecraft:sea_pickle
sea_pickle
minecraft:pale_oak_shelf
pale_oak_shelf
minecraft:brown_concrete_powder
brown_concrete_powder
minecraft:mangrove_hanging_sign
mangrove_hanging_sign
minecraft:waxed_exposed_copper_trapdoor
waxed_exposed_copper_trapdoor
minecraft:brown_candle
brown_candle
minecraft:mossy_stone_brick_stairs
mossy_stone_brick_stairs
minecraft:end_rod
end_rod
minecraft:crimson_stem
crimson_stem
minecraft:green_concrete
green_concrete
minecraft:crimson_slab
crimson_slab
minecraft:warped_hyphae
warped_hyphae
minecraft:warped_wart_block
warped_wart_block
minecraft:light_gray_shulker_box
light_gray_shulker_box
minecraft:resin_bricks
resin_bricks
minecraft:tuff_stairs
tuff_stairs
minecraft:yellow_carpet
yellow_carpet
minecraft:cyan_stained_glass
cyan_stained_glass
minecraft:black_stained_glass
black_stained_glass
minecraft:waxed_oxidized_copper_door
waxed_oxidized_copper_door
minecraft:dead_horn_coral
dead_horn_coral
minecraft:grass_block
grass_block
minecraft:tripwire_hook
tripwire_hook
minecraft:dark_oak_pressure_plate
dark_oak_pressure_plate
minecraft:copper_door
copper_door
minecraft:stripped_birch_log
stripped_birch_log
minecraft:tinted_glass
tinted_glass
minecraft:big_dripleaf
big_dripleaf
minecraft:cut_sandstone
cut_sandstone
minecraft:warped_hanging_sign
warped_hanging_sign
minecraft:lime_wool
lime_wool
minecraft:polished_blackstone_slab
polished_blackstone_slab
reeds
minecraft:black_shulker_box
black_shulker_box
minecraft:weathered_copper_golem_statue
weathered_copper_golem_statue
minecraft:jungle_sapling
jungle_sapling
minecraft:chiseled_sandstone
chiseled_sandstone
minecraft:barrier
barrier
minecraft:black_carpet
black_carpet
minecraft:pale_oak_log
pale_oak_log
minecraft:weathered_cut_copper_slab
weathered_cut_copper_slab
minecraft:oxidized_copper_lantern
oxidized_copper_lantern
minecraft:dark_oak_leaves
dark_oak_leaves
minecraft:nether_brick_slab
nether_brick_slab
minecraft:fern
fern
minecraft:torchflower
torchflower
minecraft:short_dry_grass
short_dry_grass
minecraft:infested_stone
infested_stone
minecraft:pale_hanging_moss
pale_hanging_moss
minecraft:pale_moss_carpet
pale_moss_carpet
minecraft:end_portal_frame
end_portal_frame
minecraft:bamboo_pressure_plate
bamboo_pressure_plate
minecraft:prismarine
prismarine
minecraft:exposed_copper_trapdoor
exposed_copper_trapdoor
minecraft:mushroom_stem
mushroom_stem
minecraft:black_terracotta
black_terracotta
minecraft:resin_brick_stairs
resin_brick_stairs
minecraft:deepslate_gold_ore
deepslate_gold_ore
minecraft:ancient_debris
ancient_debris
minecraft:vault
vault
minecraft:beehive
beehive
minecraft:jungle_door
jungle_door
minecraft:glass
glass
minecraft:wither_rose
wither_rose
minecraft:exposed_cut_copper
exposed_cut_copper
minecraft:waxed_weathered_cut_copper_stairs
waxed_weathered_cut_copper_stairs
minecraft:mangrove_roots
mangrove_roots
minecraft:yellow_candle
yellow_candle
minecraft:acacia_stairs
acacia_stairs
minecraft:bamboo_mosaic_stairs
bamboo_mosaic_stairs
minecraft:brown_concrete
brown_concrete
minecraft:cherry_slab
cherry_slab
minecraft:chiseled_resin_bricks
chiseled_resin_bricks
minecraft:bubble_coral
bubble_coral
minecraft:orange_shulker_box
orange_shulker_box
minecraft:light_gray_candle
light_gray_candle
minecraft:polished_blackstone_pressure_plate
polished_blackstone_pressure_plate
minecraft:polished_granite_slab
polished_granite_slab
minecraft:tuff_brick_stairs
tuff_brick_stairs
minecraft:blue_shulker_box
blue_shulker_box
minecraft:exposed_copper_bulb
exposed_copper_bulb
minecraft:exposed_copper_bars
exposed_copper_bars
minecraft:dead_fire_coral
dead_fire_coral
minecraft:stone_brick_slab
stone_brick_slab
minecraft:crimson_stairs
crimson_stairs
minecraft:waxed_oxidized_copper_bars
waxed_oxidized_copper_bars
minecraft:stripped_spruce_log
stripped_spruce_log
minecraft:waxed_oxidized_copper_bulb
waxed_oxidized_copper_bulb
minecraft:azalea_leaves_flowered
azalea_leaves_flowered
minecraft:warped_nylium
warped_nylium
minecraft:deepslate_emerald_ore
deepslate_emerald_ore
minecraft:acacia_sapling
acacia_sapling
minecraft:quartz_bricks
quartz_bricks
minecraft:andesite_slab
andesite_slab
minecraft:lime_candle
lime_candle
minecraft:structure_block
structure_block
minecraft:end_brick_stairs
end_brick_stairs
minecraft:purple_terracotta
purple_terracotta
minecraft:target
target
minecraft:wooden_button
wooden_button
minecraft:mangrove_door
mangrove_door
minecraft:weathered_copper_door
weathered_copper_door
minecraft:pearlescent_froglight
pearlescent_froglight
minecraft:bamboo_button
bamboo_button
minecraft:tall_grass
tall_grass
minecraft:weathered_copper_lantern
weathered_copper_lantern
minecraft:light_block_12
light_block_12
minecraft:light_block_13
light_block_13
minecraft:light_block_10
light_block_10
minecraft:light_block_11
light_block_11
minecraft:light_block_14
light_block_14
minecraft:light_block_15
light_block_15
minecraft:nether_sprouts
nether_sprouts
minecraft:cyan_stained_glass_pane
cyan_stained_glass_pane
minecraft:dead_horn_coral_block
dead_horn_coral_block
minecraft:verdant_froglight
verdant_froglight
minecraft:resin_block
resin_block
minecraft:warped_slab
warped_slab
minecraft:warped_stem
warped_stem
minecraft:horn_coral_fan
horn_coral_fan
minecraft:green_shulker_box
green_shulker_box
minecraft:large_fern
large_fern
minecraft:stripped_crimson_hyphae
stripped_crimson_hyphae
minecraft:lever
lever
minecraft:bamboo_slab
bamboo_slab
minecraft:brick_stairs
brick_stairs
minecraft:weathered_copper_trapdoor
weathered_copper_trapdoor
minecraft:smooth_red_sandstone_slab
smooth_red_sandstone_slab
minecraft:moss_block
moss_block
minecraft:purple_concrete_powder
purple_concrete_powder
minecraft:pink_glazed_terracotta
pink_glazed_terracotta
minecraft:short_grass
short_grass
minecraft:waxed_weathered_cut_copper_slab
waxed_weathered_cut_copper_slab
minecraft:fire_coral_fan
fire_coral_fan
minecraft:spruce_trapdoor
spruce_trapdoor
minecraft:chain_command_block
chain_command_block
minecraft:red_sandstone
red_sandstone
minecraft:red_nether_brick_slab
red_nether_brick_slab
minecraft:exposed_chiseled_copper
exposed_chiseled_copper
minecraft:spruce_fence_gate
spruce_fence_gate
minecraft:exposed_cut_copper_slab
exposed_cut_copper_slab
minecraft:red_nether_brick_stairs
red_nether_brick_stairs
minecraft:green_glazed_terracotta
green_glazed_terracotta
minecraft:jungle_planks
jungle_planks
minecraft:deepslate_redstone_ore
deepslate_redstone_ore
minecraft:dead_brain_coral_block
dead_brain_coral_block
minecraft:mangrove_fence
mangrove_fence
minecraft:oxidized_copper_grate
oxidized_copper_grate
minecraft:anvil
anvil
minecraft:birch_trapdoor
birch_trapdoor
minecraft:tuff_bricks
tuff_bricks
minecraft:mangrove_leaves
mangrove_leaves
minecraft:cobbled_deepslate
cobbled_deepslate
minecraft:quartz_slab
quartz_slab
minecraft:bookshelf
bookshelf
minecraft:mud
mud
minecraft:lit_pumpkin
lit_pumpkin
minecraft:ice
ice
minecraft:air
air
minecraft:bed
bed
minecraft:black_concrete
black_concrete
minecraft:tnt
tnt
minecraft:web
web
minecraft:dead_tube_coral_fan
dead_tube_coral_fan
minecraft:oxidized_copper_chest
oxidized_copper_chest
minecraft:oxidized_copper_chain
oxidized_copper_chain
minecraft:polished_diorite_stairs
polished_diorite_stairs
minecraft:blue_concrete_powder
blue_concrete_powder
minecraft:orange_concrete
orange_concrete
minecraft:crying_obsidian
crying_obsidian
minecraft:lime_carpet
lime_carpet
minecraft:closed_eyeblossom
closed_eyeblossom
minecraft:dead_fire_coral_fan
dead_fire_coral_fan
minecraft:decorated_pot
decorated_pot
minecraft:enchanting_table
enchanting_table
minecraft:polished_blackstone_wall
polished_blackstone_wall
minecraft:orange_tulip
orange_tulip
minecraft:brown_shulker_box
brown_shulker_box
minecraft:azalea
azalea
minecraft:mud_bricks
mud_bricks
minecraft:acacia_wood
acacia_wood
minecraft:gray_stained_glass_pane
gray_stained_glass_pane
minecraft:hopper
hopper
minecraft:bell
bell
minecraft:lectern
lectern
minecraft:bush
bush
minecraft:stripped_crimson_stem
stripped_crimson_stem
minecraft:light_blue_shulker_box
light_blue_shulker_box
minecraft:jungle_stairs
jungle_stairs
minecraft:mangrove_propagule
mangrove_propagule
minecraft:cactus
cactus
minecraft:budding_amethyst
budding_amethyst
minecraft:sniffer_egg
sniffer_egg
minecraft:birch_stairs
birch_stairs
minecraft:nether_brick_wall
nether_brick_wall
minecraft:purple_glazed_terracotta
purple_glazed_terracotta
minecraft:green_concrete_powder
green_concrete_powder
minecraft:bedrock
bedrock
minecraft:spruce_slab
spruce_slab
minecraft:blackstone_stairs
blackstone_stairs
minecraft:blue_ice
blue_ice
minecraft:cyan_shulker_box
cyan_shulker_box
minecraft:polished_andesite_stairs
polished_andesite_stairs
minecraft:piglin_head
piglin_head
minecraft:sculk
sculk
minecraft:netherrack
netherrack
minecraft:purple_candle
purple_candle
minecraft:mangrove_button
mangrove_button
minecraft:orange_carpet
orange_carpet
minecraft:dead_horn_coral_fan
dead_horn_coral_fan
minecraft:lantern
lantern
minecraft:crimson_shelf
crimson_shelf
minecraft:waxed_weathered_copper_door
waxed_weathered_copper_door
minecraft:red_stained_glass_pane
red_stained_glass_pane
minecraft:waxed_oxidized_lightning_rod
waxed_oxidized_lightning_rod
minecraft:pink_stained_glass_pane
pink_stained_glass_pane
minecraft:light_blue_wool
light_blue_wool
minecraft:allow
allow
minecraft:dark_oak_fence
dark_oak_fence
minecraft:birch_door
birch_door
minecraft:cherry_shelf
cherry_shelf
minecraft:chest
chest
minecraft:cherry_wood
cherry_wood
minecraft:clay
clay
minecraft:cherry_stairs
cherry_stairs
minecraft:cake
cake
minecraft:crimson_hanging_sign
crimson_hanging_sign
minecraft:sculk_vein
sculk_vein
minecraft:dead_brain_coral
dead_brain_coral
minecraft:deepslate_coal_ore
deepslate_coal_ore
minecraft:weathered_cut_copper
weathered_cut_copper
minecraft:cracked_polished_blackstone_bricks
cracked_polished_blackstone_bricks
minecraft:wither_skeleton_skull
wither_skeleton_skull
minecraft:polished_tuff
polished_tuff
minecraft:magenta_stained_glass
magenta_stained_glass
minecraft:acacia_button
acacia_button
minecraft:chiseled_nether_bricks
chiseled_nether_bricks
minecraft:warped_button
warped_button
minecraft:red_concrete_powder
red_concrete_powder
minecraft:light_gray_concrete_powder
light_gray_concrete_powder
minecraft:deepslate_lapis_ore
deepslate_lapis_ore
minecraft:dead_bubble_coral
dead_bubble_coral
minecraft:cherry_sapling
cherry_sapling
minecraft:cherry_log
cherry_log
minecraft:prismarine_stairs
prismarine_stairs
minecraft:white_carpet
white_carpet
minecraft:cyan_concrete
cyan_concrete
minecraft:polished_tuff_stairs
polished_tuff_stairs
minecraft:dragon_egg
dragon_egg
minecraft:blue_concrete
blue_concrete
minecraft:nether_brick
nether_brick
minecraft:deepslate_iron_ore
deepslate_iron_ore
minecraft:element_1
element_1
minecraft:element_0
element_0
minecraft:element_3
element_3
minecraft:element_2
element_2
minecraft:element_5
element_5
minecraft:element_4
element_4
minecraft:element_7
element_7
minecraft:element_6
element_6
minecraft:element_9
element_9
minecraft:element_8
element_8
minecraft:oxeye_daisy
oxeye_daisy
minecraft:wheat
wheat
minecraft:waxed_cut_copper
waxed_cut_copper
minecraft:iron_chain
iron_chain
minecraft:resin_brick_slab
resin_brick_slab
minecraft:heavy_core
heavy_core
minecraft:cobbled_deepslate_slab
cobbled_deepslate_slab
minecraft:lilac
lilac
minecraft:pale_oak_trapdoor
pale_oak_trapdoor
minecraft:chiseled_quartz_block
chiseled_quartz_block
minecraft:spore_blossom
spore_blossom
minecraft:waxed_exposed_copper_lantern
waxed_exposed_copper_lantern
minecraft:pale_oak_stairs
pale_oak_stairs
minecraft:emerald_ore
emerald_ore
minecraft:brown_mushroom_block
brown_mushroom_block
minecraft:gray_concrete_powder
gray_concrete_powder
minecraft:petrified_oak_slab
petrified_oak_slab
minecraft:gray_concrete
gray_concrete
minecraft:pink_candle
pink_candle
minecraft:red_nether_brick_wall
red_nether_brick_wall
minecraft:purple_shulker_box
purple_shulker_box
minecraft:carved_pumpkin
carved_pumpkin
minecraft:dropper
dropper
minecraft:stripped_warped_stem
stripped_warped_stem
minecraft:candle
candle
minecraft:polished_andesite_slab
polished_andesite_slab
minecraft:pointed_dripstone
pointed_dripstone
minecraft:red_carpet
red_carpet
minecraft:cut_red_sandstone_slab
cut_red_sandstone_slab
minecraft:deepslate_brick_stairs
deepslate_brick_stairs
minecraft:dark_prismarine_stairs
dark_prismarine_stairs
minecraft:creaking_heart
creaking_heart
minecraft:pale_oak_button
pale_oak_button
minecraft:chiseled_tuff_bricks
chiseled_tuff_bricks
minecraft:light_blue_concrete
light_blue_concrete
minecraft:exposed_copper_golem_statue
exposed_copper_golem_statue
minecraft:red_tulip
red_tulip
minecraft:cauldron
cauldron
minecraft:tube_coral_block
tube_coral_block
minecraft:chiseled_red_sandstone
chiseled_red_sandstone
minecraft:birch_sapling
birch_sapling
minecraft:dark_oak_trapdoor
dark_oak_trapdoor
minecraft:orange_terracotta
orange_terracotta
minecraft:brick_slab
brick_slab
minecraft:waxed_oxidized_copper
waxed_oxidized_copper
minecraft:oak_planks
oak_planks
minecraft:stripped_oak_log
stripped_oak_log
minecraft:smooth_stone_slab
smooth_stone_slab
minecraft:polished_andesite
polished_andesite
minecraft:sea_lantern
sea_lantern
minecraft:brewing_stand
brewing_stand
minecraft:weathered_copper_bulb
weathered_copper_bulb
minecraft:weathered_copper_bars
weathered_copper_bars
minecraft:blast_furnace
blast_furnace
minecraft:crimson_roots
crimson_roots
minecraft:acacia_slab
acacia_slab
minecraft:stonecutter_block
stonecutter_block
minecraft:smooth_quartz_slab
smooth_quartz_slab
minecraft:yellow_concrete_powder
yellow_concrete_powder
minecraft:lime_stained_glass_pane
lime_stained_glass_pane
minecraft:yellow_stained_glass
yellow_stained_glass
minecraft:spruce_wood
spruce_wood
minecraft:blackstone
blackstone
minecraft:acacia_fence_gate
acacia_fence_gate
minecraft:wildflowers
wildflowers
minecraft:element_10
element_10
minecraft:element_11
element_11
minecraft:element_12
element_12
minecraft:element_13
element_13
minecraft:element_14
element_14
minecraft:element_15
element_15
minecraft:element_16
element_16
minecraft:element_17
element_17
minecraft:element_18
element_18
minecraft:element_19
element_19
minecraft:element_36
element_36
minecraft:element_37
element_37
minecraft:element_34
element_34
minecraft:element_35
element_35
minecraft:element_32
element_32
minecraft:element_33
element_33
minecraft:element_30
element_30
minecraft:element_31
element_31
minecraft:element_38
element_38
minecraft:element_39
element_39
minecraft:element_29
element_29
minecraft:element_28
element_28
minecraft:element_21
element_21
minecraft:element_20
element_20
minecraft:element_23
element_23
minecraft:element_22
element_22
minecraft:element_25
element_25
minecraft:element_24
element_24
minecraft:element_27
element_27
minecraft:element_26
element_26
minecraft:element_58
element_58
minecraft:element_59
element_59
minecraft:element_54
element_54
minecraft:element_55
element_55
minecraft:element_56
element_56
minecraft:element_57
element_57
minecraft:element_50
element_50
minecraft:element_51
element_51
minecraft:element_52
element_52
minecraft:element_53
element_53
minecraft:element_49
element_49
minecraft:element_48
element_48
minecraft:element_47
element_47
minecraft:element_46
element_46
minecraft:element_45
element_45
minecraft:element_44
element_44
minecraft:element_43
element_43
minecraft:element_42
element_42
minecraft:element_41
element_41
minecraft:element_40
element_40
minecraft:element_72
element_72
minecraft:element_73
element_73
minecraft:element_70
element_70
minecraft:element_71
element_71
minecraft:element_76
element_76
minecraft:element_77
element_77
minecraft:element_74
element_74
minecraft:element_75
element_75
minecraft:element_78
element_78
minecraft:element_79
element_79
minecraft:element_65
element_65
minecraft:element_64
element_64
minecraft:element_67
element_67
minecraft:element_66
element_66
minecraft:element_61
element_61
minecraft:element_60
element_60
minecraft:element_63
element_63
minecraft:element_62
element_62
minecraft:element_69
element_69
minecraft:element_68
element_68
minecraft:element_98
element_98
minecraft:element_99
element_99
minecraft:element_90
element_90
minecraft:element_91
element_91
minecraft:element_92
element_92
minecraft:element_93
element_93
minecraft:element_94
element_94
minecraft:element_95
element_95
minecraft:element_96
element_96
minecraft:element_97
element_97
minecraft:element_89
element_89
minecraft:element_88
element_88
minecraft:element_83
element_83
minecraft:element_82
element_82
minecraft:element_81
element_81
minecraft:element_80
element_80
minecraft:element_87
element_87
minecraft:element_86
element_86
minecraft:element_85
element_85
minecraft:element_84
element_84
minecraft:lapis_ore
lapis_ore
minecraft:red_concrete
red_concrete
minecraft:pink_carpet
pink_carpet
minecraft:smooth_quartz_stairs
smooth_quartz_stairs
minecraft:waxed_copper_lantern
waxed_copper_lantern
minecraft:azalea_leaves
azalea_leaves
minecraft:purpur_block
purpur_block
minecraft:cyan_candle
cyan_candle
minecraft:waxed_copper
waxed_copper
minecraft:repeating_command_block
repeating_command_block
minecraft:nether_wart
nether_wart
minecraft:purple_carpet
purple_carpet
minecraft:crimson_fungus
crimson_fungus
minecraft:cherry_planks
cherry_planks
minecraft:polished_deepslate
polished_deepslate
minecraft:smooth_red_sandstone
smooth_red_sandstone
minecraft:purpur_stairs
purpur_stairs
minecraft:tube_coral
tube_coral
minecraft:waxed_copper_door
waxed_copper_door
minecraft:birch_button
birch_button
minecraft:peony
peony
minecraft:command_block
command_block
minecraft:polished_blackstone_button
polished_blackstone_button
minecraft:crafter
crafter
minecraft:spruce_planks
spruce_planks
minecraft:furnace
furnace
minecraft:amethyst_cluster
amethyst_cluster
minecraft:waxed_chiseled_copper
waxed_chiseled_copper
minecraft:waxed_cut_copper_slab
waxed_cut_copper_slab
minecraft:polished_deepslate_wall
polished_deepslate_wall
minecraft:dried_kelp_block
dried_kelp_block
minecraft:crimson_fence
crimson_fence
minecraft:chiseled_tuff
chiseled_tuff
minecraft:lime_concrete_powder
lime_concrete_powder
minecraft:turtle_egg
turtle_egg
minecraft:magma
magma
minecraft:dispenser
dispenser
minecraft:brown_terracotta
brown_terracotta
minecraft:deepslate_diamond_ore
deepslate_diamond_ore
minecraft:grindstone
grindstone
minecraft:waxed_copper_golem_statue
waxed_copper_golem_statue
minecraft:light_gray_wool
light_gray_wool
minecraft:soul_campfire
soul_campfire
minecraft:prismarine_bricks
prismarine_bricks
minecraft:wooden_pressure_plate
wooden_pressure_plate
minecraft:sandstone_wall
sandstone_wall
minecraft:birch_fence
birch_fence
minecraft:waxed_oxidized_copper_grate
waxed_oxidized_copper_grate
minecraft:damaged_anvil
damaged_anvil
minecraft:white_concrete
white_concrete
minecraft:material_reducer
material_reducer
minecraft:trial_spawner
trial_spawner
minecraft:acacia_fence
acacia_fence
minecraft:grass_path
grass_path
minecraft:resin_brick_wall
resin_brick_wall
minecraft:cobbled_deepslate_wall
cobbled_deepslate_wall
minecraft:waxed_weathered_lightning_rod
waxed_weathered_lightning_rod
minecraft:orange_concrete_powder
orange_concrete_powder
minecraft:weathered_copper
weathered_copper
minecraft:mossy_stone_brick_wall
mossy_stone_brick_wall
minecraft:lime_terracotta
lime_terracotta
minecraft:cherry_fence_gate
cherry_fence_gate
minecraft:gray_glazed_terracotta
gray_glazed_terracotta
minecraft:lodestone
lodestone
minecraft:bamboo_mosaic
bamboo_mosaic
minecraft:raw_iron_block
raw_iron_block
minecraft:light_gray_carpet
light_gray_carpet
minecraft:purple_wool
purple_wool
minecraft:iron_block
iron_block
minecraft:ladder
ladder
minecraft:crimson_pressure_plate
crimson_pressure_plate
minecraft:stripped_mangrove_log
stripped_mangrove_log
minecraft:copper_lantern
copper_lantern
minecraft:gravel
gravel
minecraft:cartography_table
cartography_table
minecraft:oxidized_copper_door
oxidized_copper_door
minecraft:dandelion
dandelion
grass
concretepowder
pistonarmcollision
stone_slab4
stone_slab
sealantern
stone_slab2
stickypistonarmcollision
stone_slab3
double_stone_slab
double_stone_slab2
double_stone_slab3
double_stone_slab4
yellow_flower
chain
wool
minecraft:wool
log
minecraft:log
log2
minecraft:log2
coral
minecraft:coral
fence
minecraft:fence
carpet
minecraft:carpet
shulker_box
minecraft:shulker_box
concrete
minecraft:concrete
stained_hardened_clay
minecraft:stained_hardened_clay
concrete_powder
minecraft:concrete_powder
stained_glass
minecraft:stained_glass
stained_glass_pane
minecraft:stained_glass_pane
planks
minecraft:planks
wooden_slab
minecraft:wooden_slab
leaves
minecraft:leaves
leaves2
minecraft:leaves2
wood
minecraft:wood
sapling
minecraft:sapling
coral_fan
minecraft:coral_fan
coral_fan_dead
minecraft:coral_fan_dead
red_flower
minecraft:red_flower
tallgrass
minecraft:tallgrass
coral_block
minecraft:coral_block
double_plant
minecraft:double_plant
stone_block_slab
minecraft:stone_block_slab
stone_block_slab2
minecraft:stone_block_slab2
stone_block_slab3
minecraft:stone_block_slab3
stone_block_slab4
minecraft:stone_block_slab4
monster_egg
minecraft:monster_egg
stonebrick
minecraft:stonebrick
light_block
minecraft:light_block
chemistry_table
minecraft:chemistry_table
skull
minecraft:skull
minecraft:chicken
minecraft:rabbit
minecraft:cod
minecraft:pufferfish
minecraft:salmon
minecraft:minecart
minecraft:hopper_minecart
minecraft:tnt_minecart
minecraft:chest_minecart
minecraft:command_block_minecart
minecraft:arrow
minecraft:snowball
minecraft:egg
minecraft:painting
minecraft:splash_potion
minecraft:ender_pearl
minecraft:boat
minecraft:chest_boat
minecraft:lingering_potion
minecraft:armor_stand
minecraft:ice_bomb
minecraft:balloon
chicken
rabbit
cod
pufferfish
salmon
minecart
hopper_minecart
tnt_minecart
chest_minecart
command_block_minecart
arrow
snowball
egg
painting
fireball
splash_potion
ender_pearl
boat
chest_boat
lingering_potion
armor_stand
ice_bomb
balloon
minecraft:wheat_seeds
wheat_seeds
minecraft:pumpkin_seeds
pumpkin_seeds
minecraft:melon_seeds
melon_seeds
minecraft:beetroot_seeds
beetroot_seeds
minecraft:torchflower_seeds
torchflower_seeds
minecraft:pitcher_pod
pitcher_pod
minecraft:potato
potato
minecraft:poisonous_potato
poisonous_potato
minecraft:carrot
carrot
minecraft:golden_carrot
golden_carrot
minecraft:apple
apple
minecraft:golden_apple
golden_apple
minecraft:enchanted_golden_apple
enchanted_golden_apple
minecraft:melon_slice
melon_slice
minecraft:glistering_melon_slice
glistering_melon_slice
minecraft:sweet_berries
sweet_berries
minecraft:glow_berries
glow_berries
minecraft:honeycomb
honeycomb
minecraft:white_dye
white_dye
minecraft:light_gray_dye
light_gray_dye
minecraft:gray_dye
gray_dye
minecraft:black_dye
black_dye
minecraft:brown_dye
brown_dye
minecraft:red_dye
red_dye
minecraft:orange_dye
orange_dye
minecraft:yellow_dye
yellow_dye
minecraft:lime_dye
lime_dye
minecraft:green_dye
green_dye
minecraft:cyan_dye
cyan_dye
minecraft:light_blue_dye
light_blue_dye
minecraft:blue_dye
blue_dye
minecraft:purple_dye
purple_dye
minecraft:magenta_dye
magenta_dye
minecraft:pink_dye
pink_dye
minecraft:ink_sac
ink_sac
minecraft:glow_ink_sac
glow_ink_sac
minecraft:cocoa_beans
cocoa_beans
minecraft:lapis_lazuli
lapis_lazuli
minecraft:bone_meal
bone_meal
minecraft:porkchop
porkchop
minecraft:beef
beef
minecraft:mutton
mutton
minecraft:tropical_fish
tropical_fish
minecraft:brown_egg
brown_egg
minecraft:blue_egg
blue_egg
minecraft:sugar_cane
sugar_cane
minecraft:sugar
sugar
minecraft:rotten_flesh
rotten_flesh
minecraft:bone
bone
minecraft:spider_eye
spider_eye
minecraft:chicken_spawn_egg
chicken_spawn_egg
minecraft:cow_spawn_egg
cow_spawn_egg
minecraft:pig_spawn_egg
pig_spawn_egg
minecraft:sheep_spawn_egg
sheep_spawn_egg
minecraft:camel_spawn_egg
camel_spawn_egg
minecraft:donkey_spawn_egg
donkey_spawn_egg
minecraft:horse_spawn_egg
horse_spawn_egg
minecraft:mule_spawn_egg
mule_spawn_egg
minecraft:cat_spawn_egg
cat_spawn_egg
minecraft:parrot_spawn_egg
parrot_spawn_egg
minecraft:wolf_spawn_egg
wolf_spawn_egg
minecraft:armadillo_spawn_egg
armadillo_spawn_egg
minecraft:bat_spawn_egg
bat_spawn_egg
minecraft:bee_spawn_egg
bee_spawn_egg
minecraft:fox_spawn_egg
fox_spawn_egg
minecraft:goat_spawn_egg
goat_spawn_egg
minecraft:llama_spawn_egg
llama_spawn_egg
minecraft:ocelot_spawn_egg
ocelot_spawn_egg
minecraft:panda_spawn_egg
panda_spawn_egg
minecraft:polar_bear_spawn_egg
polar_bear_spawn_egg
minecraft:rabbit_spawn_egg
rabbit_spawn_egg
minecraft:axolotl_spawn_egg
axolotl_spawn_egg
minecraft:cod_spawn_egg
cod_spawn_egg
minecraft:dolphin_spawn_egg
dolphin_spawn_egg
minecraft:frog_spawn_egg
frog_spawn_egg
minecraft:glow_squid_spawn_egg
glow_squid_spawn_egg
minecraft:nautilus_spawn_egg
nautilus_spawn_egg
minecraft:pufferfish_spawn_egg
pufferfish_spawn_egg
minecraft:salmon_spawn_egg
salmon_spawn_egg
minecraft:squid_spawn_egg
squid_spawn_egg
minecraft:tadpole_spawn_egg
tadpole_spawn_egg
minecraft:tropical_fish_spawn_egg
tropical_fish_spawn_egg
minecraft:turtle_spawn_egg
turtle_spawn_egg
minecraft:allay_spawn_egg
allay_spawn_egg
minecraft:mooshroom_spawn_egg
mooshroom_spawn_egg
minecraft:sniffer_spawn_egg
sniffer_spawn_egg
minecraft:copper_golem_spawn_egg
copper_golem_spawn_egg
minecraft:iron_golem_spawn_egg
iron_golem_spawn_egg
minecraft:snow_golem_spawn_egg
snow_golem_spawn_egg
minecraft:trader_llama_spawn_egg
trader_llama_spawn_egg
minecraft:villager_spawn_egg
villager_spawn_egg
minecraft:wandering_trader_spawn_egg
wandering_trader_spawn_egg
minecraft:bogged_spawn_egg
bogged_spawn_egg
minecraft:camel_husk_spawn_egg
camel_husk_spawn_egg
minecraft:drowned_spawn_egg
drowned_spawn_egg
minecraft:husk_spawn_egg
husk_spawn_egg
minecraft:parched_spawn_egg
parched_spawn_egg
minecraft:skeleton_spawn_egg
skeleton_spawn_egg
minecraft:skeleton_horse_spawn_egg
skeleton_horse_spawn_egg
minecraft:stray_spawn_egg
stray_spawn_egg
minecraft:zombie_spawn_egg
zombie_spawn_egg
minecraft:zombie_horse_spawn_egg
zombie_horse_spawn_egg
minecraft:zombie_nautilus_spawn_egg
zombie_nautilus_spawn_egg
minecraft:zombie_villager_spawn_egg
zombie_villager_spawn_egg
minecraft:cave_spider_spawn_egg
cave_spider_spawn_egg
minecraft:spider_spawn_egg
spider_spawn_egg
minecraft:breeze_spawn_egg
breeze_spawn_egg
minecraft:creaking_spawn_egg
creaking_spawn_egg
minecraft:creeper_spawn_egg
creeper_spawn_egg
minecraft:elder_guardian_spawn_egg
elder_guardian_spawn_egg
minecraft:guardian_spawn_egg
guardian_spawn_egg
minecraft:phantom_spawn_egg
phantom_spawn_egg
minecraft:silverfish_spawn_egg
silverfish_spawn_egg
minecraft:slime_spawn_egg
slime_spawn_egg
minecraft:warden_spawn_egg
warden_spawn_egg
minecraft:witch_spawn_egg
witch_spawn_egg
minecraft:evoker_spawn_egg
evoker_spawn_egg
minecraft:pillager_spawn_egg
pillager_spawn_egg
minecraft:ravager_spawn_egg
ravager_spawn_egg
minecraft:vex_spawn_egg
vex_spawn_egg
minecraft:vindicator_spawn_egg
vindicator_spawn_egg
minecraft:blaze_spawn_egg
blaze_spawn_egg
minecraft:ghast_spawn_egg
ghast_spawn_egg
minecraft:happy_ghast_spawn_egg
happy_ghast_spawn_egg
minecraft:hoglin_spawn_egg
hoglin_spawn_egg
minecraft:magma_cube_spawn_egg
magma_cube_spawn_egg
minecraft:piglin_spawn_egg
piglin_spawn_egg
minecraft:piglin_brute_spawn_egg
piglin_brute_spawn_egg
minecraft:strider_spawn_egg
strider_spawn_egg
minecraft:wither_skeleton_spawn_egg
wither_skeleton_spawn_egg
minecraft:zoglin_spawn_egg
zoglin_spawn_egg
minecraft:zombie_pigman_spawn_egg
zombie_pigman_spawn_egg
minecraft:enderman_spawn_egg
enderman_spawn_egg
minecraft:endermite_spawn_egg
endermite_spawn_egg
minecraft:shulker_spawn_egg
shulker_spawn_egg
minecraft:chorus_fruit
chorus_fruit
minecraft:popped_chorus_fruit
popped_chorus_fruit
minecraft:leather_helmet
leather_helmet
minecraft:copper_helmet
copper_helmet
minecraft:chainmail_helmet
chainmail_helmet
minecraft:iron_helmet
iron_helmet
minecraft:golden_helmet
golden_helmet
minecraft:diamond_helmet
diamond_helmet
minecraft:netherite_helmet
netherite_helmet
minecraft:leather_chestplate
leather_chestplate
minecraft:copper_chestplate
copper_chestplate
minecraft:chainmail_chestplate
chainmail_chestplate
minecraft:iron_chestplate
iron_chestplate
minecraft:golden_chestplate
golden_chestplate
minecraft:diamond_chestplate
diamond_chestplate
minecraft:netherite_chestplate
netherite_chestplate
minecraft:leather_leggings
leather_leggings
minecraft:copper_leggings
copper_leggings
minecraft:chainmail_leggings
chainmail_leggings
minecraft:iron_leggings
iron_leggings
minecraft:golden_leggings
golden_leggings
minecraft:diamond_leggings
diamond_leggings
minecraft:netherite_leggings
netherite_leggings
minecraft:leather_boots
leather_boots
minecraft:copper_boots
copper_boots
minecraft:chainmail_boots
chainmail_boots
minecraft:iron_boots
iron_boots
minecraft:golden_boots
golden_boots
minecraft:diamond_boots
diamond_boots
minecraft:netherite_boots
netherite_boots
minecraft:wooden_sword
wooden_sword
minecraft:stone_sword
stone_sword
minecraft:copper_sword
copper_sword
minecraft:iron_sword
iron_sword
minecraft:golden_sword
golden_sword
minecraft:diamond_sword
diamond_sword
minecraft:netherite_sword
netherite_sword
minecraft:wooden_spear
wooden_spear
minecraft:stone_spear
stone_spear
minecraft:copper_spear
copper_spear
minecraft:iron_spear
iron_spear
minecraft:golden_spear
golden_spear
minecraft:diamond_spear
diamond_spear
minecraft:netherite_spear
netherite_spear
minecraft:wooden_axe
wooden_axe
minecraft:stone_axe
stone_axe
minecraft:copper_axe
copper_axe
minecraft:iron_axe
iron_axe
minecraft:golden_axe
golden_axe
minecraft:diamond_axe
diamond_axe
minecraft:netherite_axe
netherite_axe
minecraft:wooden_pickaxe
wooden_pickaxe
minecraft:stone_pickaxe
stone_pickaxe
minecraft:copper_pickaxe
copper_pickaxe
minecraft:iron_pickaxe
iron_pickaxe
minecraft:golden_pickaxe
golden_pickaxe
minecraft:diamond_pickaxe
diamond_pickaxe
minecraft:netherite_pickaxe
netherite_pickaxe
minecraft:wooden_shovel
wooden_shovel
minecraft:stone_shovel
stone_shovel
minecraft:copper_shovel
copper_shovel
minecraft:iron_shovel
iron_shovel
minecraft:golden_shovel
golden_shovel
minecraft:diamond_shovel
diamond_shovel
minecraft:netherite_shovel
netherite_shovel
minecraft:wooden_hoe
wooden_hoe
minecraft:stone_hoe
stone_hoe
minecraft:copper_hoe
copper_hoe
minecraft:iron_hoe
iron_hoe
minecraft:golden_hoe
golden_hoe
minecraft:diamond_hoe
diamond_hoe
minecraft:netherite_hoe
netherite_hoe
minecraft:bow
bow
minecraft:crossbow
crossbow
minecraft:mace
mace
minecraft:trident
trident
minecraft:shield
shield
minecraft:cooked_chicken
cooked_chicken
minecraft:cooked_porkchop
cooked_porkchop
minecraft:cooked_beef
cooked_beef
minecraft:cooked_mutton
cooked_mutton
minecraft:cooked_rabbit
cooked_rabbit
minecraft:cooked_cod
cooked_cod
minecraft:cooked_salmon
cooked_salmon
minecraft:bread
bread
minecraft:mushroom_stew
mushroom_stew
minecraft:beetroot_soup
beetroot_soup
minecraft:rabbit_stew
rabbit_stew
minecraft:suspicious_stew
suspicious_stew
minecraft:baked_potato
baked_potato
minecraft:cookie
cookie
minecraft:pumpkin_pie
pumpkin_pie
minecraft:dried_kelp
dried_kelp
minecraft:fishing_rod
fishing_rod
minecraft:carrot_on_a_stick
carrot_on_a_stick
minecraft:warped_fungus_on_a_stick
warped_fungus_on_a_stick
minecraft:wind_charge
wind_charge
minecraft:shears
shears
minecraft:flint_and_steel
flint_and_steel
minecraft:lead
lead
minecraft:clock
clock
minecraft:compass
compass
minecraft:recovery_compass
recovery_compass
minecraft:goat_horn
goat_horn
minecraft:empty_map
empty_map
minecraft:saddle
saddle
minecraft:white_harness
white_harness
minecraft:light_gray_harness
light_gray_harness
minecraft:gray_harness
gray_harness
minecraft:black_harness
black_harness
minecraft:brown_harness
brown_harness
minecraft:red_harness
red_harness
minecraft:orange_harness
orange_harness
minecraft:yellow_harness
yellow_harness
minecraft:lime_harness
lime_harness
minecraft:green_harness
green_harness
minecraft:cyan_harness
cyan_harness
minecraft:light_blue_harness
light_blue_harness
minecraft:blue_harness
blue_harness
minecraft:purple_harness
purple_harness
minecraft:magenta_harness
magenta_harness
minecraft:pink_harness
pink_harness
minecraft:bundle
bundle
minecraft:white_bundle
white_bundle
minecraft:light_gray_bundle
light_gray_bundle
minecraft:gray_bundle
gray_bundle
minecraft:black_bundle
black_bundle
minecraft:brown_bundle
brown_bundle
minecraft:red_bundle
red_bundle
minecraft:orange_bundle
orange_bundle
minecraft:yellow_bundle
yellow_bundle
minecraft:lime_bundle
lime_bundle
minecraft:green_bundle
green_bundle
minecraft:cyan_bundle
cyan_bundle
minecraft:light_blue_bundle
light_blue_bundle
minecraft:blue_bundle
blue_bundle
minecraft:purple_bundle
purple_bundle
minecraft:magenta_bundle
magenta_bundle
minecraft:pink_bundle
pink_bundle
minecraft:leather_horse_armor
leather_horse_armor
minecraft:copper_horse_armor
copper_horse_armor
minecraft:iron_horse_armor
iron_horse_armor
minecraft:golden_horse_armor
golden_horse_armor
minecraft:diamond_horse_armor
diamond_horse_armor
minecraft:netherite_horse_armor
netherite_horse_armor
minecraft:wolf_armor
wolf_armor
minecraft:copper_nautilus_armor
copper_nautilus_armor
minecraft:iron_nautilus_armor
iron_nautilus_armor
minecraft:golden_nautilus_armor
golden_nautilus_armor
minecraft:diamond_nautilus_armor
diamond_nautilus_armor
minecraft:netherite_nautilus_armor
netherite_nautilus_armor
minecraft:turtle_helmet
turtle_helmet
minecraft:elytra
elytra
minecraft:totem_of_undying
totem_of_undying
minecraft:glass_bottle
glass_bottle
minecraft:experience_bottle
experience_bottle
minecraft:potion
potion
minecraft:ominous_bottle
ominous_bottle
minecraft:spyglass
spyglass
minecraft:brush
brush
minecraft:stick
stick
minecraft:music_disc_13
music_disc_13
minecraft:music_disc_cat
music_disc_cat
minecraft:music_disc_blocks
music_disc_blocks
minecraft:music_disc_chirp
music_disc_chirp
minecraft:music_disc_far
music_disc_far
minecraft:music_disc_mall
music_disc_mall
minecraft:music_disc_mellohi
music_disc_mellohi
minecraft:music_disc_stal
music_disc_stal
minecraft:music_disc_strad
music_disc_strad
minecraft:music_disc_ward
music_disc_ward
minecraft:music_disc_11
music_disc_11
minecraft:music_disc_wait
music_disc_wait
minecraft:music_disc_otherside
music_disc_otherside
minecraft:music_disc_5
music_disc_5
minecraft:music_disc_pigstep
music_disc_pigstep
minecraft:music_disc_relic
music_disc_relic
minecraft:music_disc_creator
music_disc_creator
minecraft:music_disc_creator_music_box
music_disc_creator_music_box
minecraft:music_disc_precipice
music_disc_precipice
minecraft:music_disc_tears
music_disc_tears
minecraft:music_disc_lava_chicken
music_disc_lava_chicken
minecraft:disc_fragment_5
disc_fragment_5
minecraft:glowstone_dust
glowstone_dust
minecraft:oak_sign
oak_sign
minecraft:spruce_sign
spruce_sign
minecraft:birch_sign
birch_sign
minecraft:jungle_sign
jungle_sign
minecraft:acacia_sign
acacia_sign
minecraft:dark_oak_sign
dark_oak_sign
minecraft:mangrove_sign
mangrove_sign
minecraft:cherry_sign
cherry_sign
minecraft:pale_oak_sign
pale_oak_sign
minecraft:bamboo_sign
bamboo_sign
minecraft:crimson_sign
crimson_sign
minecraft:warped_sign
warped_sign
minecraft:honey_bottle
honey_bottle
minecraft:bowl
bowl
minecraft:bucket
bucket
minecraft:milk_bucket
milk_bucket
minecraft:water_bucket
water_bucket
minecraft:lava_bucket
lava_bucket
minecraft:cod_bucket
cod_bucket
minecraft:salmon_bucket
salmon_bucket
minecraft:tropical_fish_bucket
tropical_fish_bucket
minecraft:pufferfish_bucket
pufferfish_bucket
minecraft:powder_snow_bucket
powder_snow_bucket
minecraft:axolotl_bucket
axolotl_bucket
minecraft:tadpole_bucket
tadpole_bucket
minecraft:coal
coal
minecraft:charcoal
charcoal
minecraft:diamond
diamond
minecraft:iron_nugget
iron_nugget
minecraft:raw_iron
raw_iron
minecraft:raw_gold
raw_gold
minecraft:copper_nugget
copper_nugget
minecraft:raw_copper
raw_copper
minecraft:copper_ingot
copper_ingot
minecraft:iron_ingot
iron_ingot
minecraft:netherite_scrap
netherite_scrap
minecraft:netherite_ingot
netherite_ingot
minecraft:gold_nugget
gold_nugget
minecraft:gold_ingot
gold_ingot
minecraft:emerald
emerald
minecraft:quartz
quartz
minecraft:clay_ball
clay_ball
minecraft:brick
brick
minecraft:netherbrick
netherbrick
minecraft:resin_brick
resin_brick
minecraft:prismarine_shard
prismarine_shard
minecraft:amethyst_shard
amethyst_shard
minecraft:prismarine_crystals
prismarine_crystals
minecraft:nautilus_shell
nautilus_shell
minecraft:heart_of_the_sea
heart_of_the_sea
minecraft:turtle_scute
turtle_scute
minecraft:armadillo_scute
armadillo_scute
minecraft:phantom_membrane
phantom_membrane
minecraft:string
string
minecraft:feather
feather
minecraft:flint
flint
minecraft:gunpowder
gunpowder
minecraft:leather
leather
minecraft:rabbit_hide
rabbit_hide
minecraft:rabbit_foot
rabbit_foot
minecraft:fire_charge
fire_charge
minecraft:blaze_rod
blaze_rod
minecraft:breeze_rod
breeze_rod
minecraft:blaze_powder
blaze_powder
minecraft:magma_cream
magma_cream
minecraft:fermented_spider_eye
fermented_spider_eye
minecraft:echo_shard
echo_shard
minecraft:dragon_breath
dragon_breath
minecraft:shulker_shell
shulker_shell
minecraft:ghast_tear
ghast_tear
minecraft:slime_ball
slime_ball
minecraft:ender_eye
ender_eye
minecraft:nether_star
nether_star
minecraft:end_crystal
end_crystal
minecraft:paper
paper
minecraft:book
book
minecraft:writable_book
writable_book
minecraft:enchanted_book
enchanted_book
minecraft:oak_boat
oak_boat
minecraft:spruce_boat
spruce_boat
minecraft:birch_boat
birch_boat
minecraft:jungle_boat
jungle_boat
minecraft:acacia_boat
acacia_boat
minecraft:dark_oak_boat
dark_oak_boat
minecraft:mangrove_boat
mangrove_boat
minecraft:cherry_boat
cherry_boat
minecraft:pale_oak_boat
pale_oak_boat
minecraft:bamboo_raft
bamboo_raft
minecraft:oak_chest_boat
oak_chest_boat
minecraft:spruce_chest_boat
spruce_chest_boat
minecraft:birch_chest_boat
birch_chest_boat
minecraft:jungle_chest_boat
jungle_chest_boat
minecraft:acacia_chest_boat
acacia_chest_boat
minecraft:dark_oak_chest_boat
dark_oak_chest_boat
minecraft:mangrove_chest_boat
mangrove_chest_boat
minecraft:cherry_chest_boat
cherry_chest_boat
minecraft:pale_oak_chest_boat
pale_oak_chest_boat
minecraft:bamboo_chest_raft
bamboo_chest_raft
minecraft:redstone
redstone
minecraft:repeater
repeater
minecraft:comparator
comparator
minecraft:name_tag
name_tag
minecraft:banner
banner
minecraft:creeper_banner_pattern
creeper_banner_pattern
minecraft:skull_banner_pattern
skull_banner_pattern
minecraft:flower_banner_pattern
flower_banner_pattern
minecraft:mojang_banner_pattern
mojang_banner_pattern
minecraft:field_masoned_banner_pattern
field_masoned_banner_pattern
minecraft:bordure_indented_banner_pattern
bordure_indented_banner_pattern
minecraft:piglin_banner_pattern
piglin_banner_pattern
minecraft:globe_banner_pattern
globe_banner_pattern
minecraft:flow_banner_pattern
flow_banner_pattern
minecraft:guster_banner_pattern
guster_banner_pattern
minecraft:angler_pottery_sherd
angler_pottery_sherd
minecraft:archer_pottery_sherd
archer_pottery_sherd
minecraft:arms_up_pottery_sherd
arms_up_pottery_sherd
minecraft:blade_pottery_sherd
blade_pottery_sherd
minecraft:brewer_pottery_sherd
brewer_pottery_sherd
minecraft:burn_pottery_sherd
burn_pottery_sherd
minecraft:danger_pottery_sherd
danger_pottery_sherd
minecraft:explorer_pottery_sherd
explorer_pottery_sherd
minecraft:flow_pottery_sherd
flow_pottery_sherd
minecraft:friend_pottery_sherd
friend_pottery_sherd
minecraft:guster_pottery_sherd
guster_pottery_sherd
minecraft:heart_pottery_sherd
heart_pottery_sherd
minecraft:heartbreak_pottery_sherd
heartbreak_pottery_sherd
minecraft:howl_pottery_sherd
howl_pottery_sherd
minecraft:miner_pottery_sherd
miner_pottery_sherd
minecraft:mourner_pottery_sherd
mourner_pottery_sherd
minecraft:plenty_pottery_sherd
plenty_pottery_sherd
minecraft:prize_pottery_sherd
prize_pottery_sherd
minecraft:scrape_pottery_sherd
scrape_pottery_sherd
minecraft:sheaf_pottery_sherd
sheaf_pottery_sherd
minecraft:shelter_pottery_sherd
shelter_pottery_sherd
minecraft:skull_pottery_sherd
skull_pottery_sherd
minecraft:snort_pottery_sherd
snort_pottery_sherd
minecraft:netherite_upgrade_smithing_template
netherite_upgrade_smithing_template
minecraft:sentry_armor_trim_smithing_template
sentry_armor_trim_smithing_template
minecraft:vex_armor_trim_smithing_template
vex_armor_trim_smithing_template
minecraft:wild_armor_trim_smithing_template
wild_armor_trim_smithing_template
minecraft:coast_armor_trim_smithing_template
coast_armor_trim_smithing_template
minecraft:dune_armor_trim_smithing_template
dune_armor_trim_smithing_template
minecraft:wayfinder_armor_trim_smithing_template
wayfinder_armor_trim_smithing_template
minecraft:shaper_armor_trim_smithing_template
shaper_armor_trim_smithing_template
minecraft:raiser_armor_trim_smithing_template
raiser_armor_trim_smithing_template
minecraft:host_armor_trim_smithing_template
host_armor_trim_smithing_template
minecraft:ward_armor_trim_smithing_template
ward_armor_trim_smithing_template
minecraft:silence_armor_trim_smithing_template
silence_armor_trim_smithing_template
minecraft:tide_armor_trim_smithing_template
tide_armor_trim_smithing_template
minecraft:snout_armor_trim_smithing_template
snout_armor_trim_smithing_template
minecraft:rib_armor_trim_smithing_template
rib_armor_trim_smithing_template
minecraft:eye_armor_trim_smithing_template
eye_armor_trim_smithing_template
minecraft:spire_armor_trim_smithing_template
spire_armor_trim_smithing_template
minecraft:flow_armor_trim_smithing_template
flow_armor_trim_smithing_template
minecraft:bolt_armor_trim_smithing_template
bolt_armor_trim_smithing_template
minecraft:firework_rocket
firework_rocket
minecraft:firework_star
firework_star
minecraft:trial_key
trial_key
minecraft:ominous_trial_key
ominous_trial_key
minecraft:compound
compound
minecraft:rapid_fertilizer
rapid_fertilizer
minecraft:bleach
bleach
minecraft:medicine
medicine
minecraft:glow_stick
glow_stick
minecraft:sparkler
sparkler
speckled_melon
nametag
glazedterracotta.white
record_chirp
glazedterracotta.orange
glazedterracotta.purple
carrotonastick
glazedterracotta.cyan
glazedterracotta.magenta
glazedterracotta.lime
glazedterracotta.light_blue
record_lava_chicken
glazedterracotta.yellow
cooked_fish
glazedterracotta.pink
record_far
glazedterracotta.gray
glazedterracotta.silver
record_blocks
prismarineshard
glazedterracotta.blue
glazedterracotta.brown
glazedterracotta.green
glazedterracotta.black
glazedterracotta.red
record_tears
record_cat
record_creator
record_13
fish
clownfish
muttoncooked
record_creator_music_box
record_precipice
appleenchanted
fireworkscharge
fireworks
record_11
record_pigstep
record_mall
record_mellohi
record_relic
record_stal
record_strad
record_wait
record_ward
record_otherside
record_5
muttonraw
netherstar
chorus_fruit_popped
melon
horsearmorleather
horsearmoriron
horsearmorgold
horsearmordiamond
turtle_shell_piece
scute
totem
lodestonecompass
map
emptymap
sign
darkoak_sign
dye
banner_pattern
spawn_egg
minecraft:filled_map
filled_map
minecraft:colored_torch_rg
colored_torch_rg
minecraft:ender_dragon_spawn_egg
ender_dragon_spawn_egg
minecraft:wither_spawn_egg
wither_spawn_egg
minecraft:colored_torch_bp
colored_torch_bp
minecraft:lodestone_compass
lodestone_compass
minecraft:dye
minecraft:banner_pattern
minecraft:spawn_egg
```

</details>

#### Static Enum: EntityEquipmentSlot (#10)

Value count: 14

<details>
<summary>Show all values</summary>

```
slot.weapon.mainhand
slot.weapon.offhand
slot.armor.head
slot.armor.chest
slot.armor.legs
slot.armor.feet
slot.armor.body
slot.hotbar
slot.inventory
slot.enderchest
slot.saddle
slot.armor
slot.chest
slot.equippable
```

</details>

#### Static Enum: Dimension (#12)

Value count: 3

<details>
<summary>Show all values</summary>

```
overworld
nether
the_end
```

</details>

#### Static Enum: ScriptDebugModeDebugger (#14)

Value count: 1

<details>
<summary>Show all values</summary>

```
debugger
```

</details>

#### Static Enum: ScriptDebuggerListen (#15)

Value count: 1

<details>
<summary>Show all values</summary>

```
listen
```

</details>

#### Static Enum: ScriptDebuggerConnect (#16)

Value count: 1

<details>
<summary>Show all values</summary>

```
connect
```

</details>

#### Static Enum: ScriptDebuggerClose (#17)

Value count: 1

<details>
<summary>Show all values</summary>

```
close
```

</details>

#### Static Enum: ScriptDebugModeProfiler (#18)

Value count: 1

<details>
<summary>Show all values</summary>

```
profiler
```

</details>

#### Static Enum: ScriptProfilerStart (#19)

Value count: 1

<details>
<summary>Show all values</summary>

```
start
```

</details>

#### Static Enum: ScriptProfilerStop (#20)

Value count: 1

<details>
<summary>Show all values</summary>

```
stop
```

</details>

#### Static Enum: ScriptDebugModeDiagnostics (#21)

Value count: 1

<details>
<summary>Show all values</summary>

```
diagnostics
```

</details>

#### Static Enum: ScriptDiagnosticsStartCapture (#22)

Value count: 1

<details>
<summary>Show all values</summary>

```
startcapture
```

</details>

#### Static Enum: ScriptDiagnosticsStopCapture (#23)

Value count: 1

<details>
<summary>Show all values</summary>

```
stopcapture
```

</details>

#### Static Enum: Block (#24)

Value count: 2650

<details>
<summary>Show all values</summary>

```
minecraft:cyan_terracotta
cyan_terracotta
minecraft:blue_candle
blue_candle
minecraft:dark_oak_wood
dark_oak_wood
minecraft:birch_standing_sign
birch_standing_sign
minecraft:polished_basalt
polished_basalt
minecraft:nether_gold_ore
nether_gold_ore
minecraft:zombie_head
zombie_head
minecraft:waxed_weathered_copper_chain
waxed_weathered_copper_chain
minecraft:waxed_weathered_copper_chest
waxed_weathered_copper_chest
minecraft:leaf_litter
leaf_litter
minecraft:warped_door
warped_door
minecraft:light_blue_concrete_powder
light_blue_concrete_powder
minecraft:bamboo_block
bamboo_block
minecraft:piston_arm_collision
piston_arm_collision
minecraft:waxed_oxidized_chiseled_copper
waxed_oxidized_chiseled_copper
minecraft:wet_sponge
wet_sponge
minecraft:end_stone_brick_wall
end_stone_brick_wall
minecraft:granite
granite
minecraft:blue_stained_glass_pane
blue_stained_glass_pane
minecraft:fence_gate
fence_gate
minecraft:birch_shelf
birch_shelf
minecraft:powder_snow
powder_snow
minecraft:dark_oak_button
dark_oak_button
minecraft:deepslate_copper_ore
deepslate_copper_ore
minecraft:chiseled_stone_bricks
chiseled_stone_bricks
minecraft:nether_brick_stairs
nether_brick_stairs
minecraft:yellow_shulker_box
yellow_shulker_box
minecraft:blackstone_double_slab
blackstone_double_slab
minecraft:lime_stained_glass
lime_stained_glass
minecraft:red_wool
red_wool
minecraft:jungle_button
jungle_button
minecraft:spruce_stairs
spruce_stairs
minecraft:acacia_shelf
acacia_shelf
minecraft:diorite
diorite
minecraft:pale_oak_fence_gate
pale_oak_fence_gate
minecraft:gray_candle_cake
gray_candle_cake
minecraft:polished_tuff_slab
polished_tuff_slab
minecraft:cherry_pressure_plate
cherry_pressure_plate
minecraft:cherry_hanging_sign
cherry_hanging_sign
minecraft:yellow_wool
yellow_wool
minecraft:crimson_wall_sign
crimson_wall_sign
minecraft:yellow_stained_glass_pane
yellow_stained_glass_pane
minecraft:azure_bluet
azure_bluet
minecraft:beacon
beacon
minecraft:red_nether_brick
red_nether_brick
minecraft:brick_wall
brick_wall
minecraft:cobbled_deepslate_stairs
cobbled_deepslate_stairs
minecraft:smooth_sandstone
smooth_sandstone
minecraft:snow_layer
snow_layer
minecraft:brick_double_slab
brick_double_slab
minecraft:black_candle
black_candle
minecraft:blue_carpet
blue_carpet
minecraft:glow_frame
glow_frame
minecraft:mud_brick_double_slab
mud_brick_double_slab
minecraft:hanging_roots
hanging_roots
minecraft:red_sandstone_wall
red_sandstone_wall
minecraft:prismarine_bricks_stairs
prismarine_bricks_stairs
minecraft:waxed_oxidized_cut_copper
waxed_oxidized_cut_copper
minecraft:waxed_exposed_copper_chain
waxed_exposed_copper_chain
minecraft:waxed_exposed_copper_chest
waxed_exposed_copper_chest
minecraft:calcite
calcite
minecraft:diorite_slab
diorite_slab
minecraft:stripped_dark_oak_log
stripped_dark_oak_log
minecraft:dead_bubble_coral_fan
dead_bubble_coral_fan
minecraft:jungle_log
jungle_log
minecraft:bubble_coral_fan
bubble_coral_fan
minecraft:sculk_shrieker
sculk_shrieker
minecraft:gray_wool
gray_wool
minecraft:orange_stained_glass_pane
orange_stained_glass_pane
minecraft:gray_carpet
gray_carpet
minecraft:lily_of_the_valley
lily_of_the_valley
minecraft:lime_glazed_terracotta
lime_glazed_terracotta
minecraft:trapdoor
trapdoor
minecraft:cactus_flower
cactus_flower
minecraft:dead_brain_coral_fan
dead_brain_coral_fan
minecraft:seagrass
seagrass
minecraft:tube_coral_fan
tube_coral_fan
minecraft:waxed_exposed_cut_copper_slab
waxed_exposed_cut_copper_slab
minecraft:redstone_lamp
redstone_lamp
minecraft:mossy_cobblestone
mossy_cobblestone
minecraft:deepslate
deepslate
minecraft:magenta_carpet
magenta_carpet
minecraft:pitcher_crop
pitcher_crop
minecraft:brown_wool
brown_wool
minecraft:waxed_exposed_chiseled_copper
waxed_exposed_chiseled_copper
minecraft:tuff_slab
tuff_slab
minecraft:warped_pressure_plate
warped_pressure_plate
minecraft:stripped_acacia_wood
stripped_acacia_wood
minecraft:firefly_bush
firefly_bush
minecraft:diamond_block
diamond_block
minecraft:dark_prismarine_double_slab
dark_prismarine_double_slab
minecraft:oak_stairs
oak_stairs
minecraft:oak_log
oak_log
minecraft:brown_stained_glass_pane
brown_stained_glass_pane
minecraft:end_bricks
end_bricks
minecraft:magenta_shulker_box
magenta_shulker_box
minecraft:packed_ice
packed_ice
minecraft:packed_mud
packed_mud
minecraft:light_blue_candle_cake
light_blue_candle_cake
minecraft:moss_carpet
moss_carpet
minecraft:warped_fungus
warped_fungus
minecraft:oxidized_lightning_rod
oxidized_lightning_rod
minecraft:polished_deepslate_slab
polished_deepslate_slab
minecraft:bamboo_door
bamboo_door
minecraft:amethyst_block
amethyst_block
minecraft:dead_bubble_coral_wall_fan
dead_bubble_coral_wall_fan
minecraft:gold_block
gold_block
minecraft:flower_pot
flower_pot
minecraft:chiseled_bookshelf
chiseled_bookshelf
minecraft:polished_deepslate_stairs
polished_deepslate_stairs
minecraft:lime_shulker_box
lime_shulker_box
minecraft:weathered_chiseled_copper
weathered_chiseled_copper
minecraft:small_amethyst_bud
small_amethyst_bud
minecraft:activator_rail
activator_rail
minecraft:iron_trapdoor
iron_trapdoor
minecraft:potatoes
potatoes
minecraft:muddy_mangrove_roots
muddy_mangrove_roots
minecraft:pale_oak_pressure_plate
pale_oak_pressure_plate
minecraft:stripped_jungle_wood
stripped_jungle_wood
minecraft:noteblock
noteblock
minecraft:tuff
tuff
minecraft:mangrove_log
mangrove_log
minecraft:oxidized_cut_copper_stairs
oxidized_cut_copper_stairs
minecraft:pale_oak_fence
pale_oak_fence
minecraft:pale_oak_leaves
pale_oak_leaves
minecraft:deepslate_tile_double_slab
deepslate_tile_double_slab
minecraft:sandstone_slab
sandstone_slab
minecraft:mossy_stone_brick_slab
mossy_stone_brick_slab
minecraft:raw_gold_block
raw_gold_block
minecraft:allium
allium
minecraft:white_shulker_box
white_shulker_box
minecraft:copper_grate
copper_grate
minecraft:black_wool
black_wool
minecraft:orange_candle
orange_candle
minecraft:powered_comparator
powered_comparator
minecraft:jungle_fence
jungle_fence
minecraft:cut_sandstone_double_slab
cut_sandstone_double_slab
minecraft:warped_wall_sign
warped_wall_sign
minecraft:spruce_fence
spruce_fence
minecraft:dark_oak_sapling
dark_oak_sapling
minecraft:melon_block
melon_block
minecraft:black_concrete_powder
black_concrete_powder
minecraft:sandstone_double_slab
sandstone_double_slab
minecraft:waxed_cut_copper_stairs
waxed_cut_copper_stairs
minecraft:open_eyeblossom
open_eyeblossom
minecraft:mob_spawner
mob_spawner
minecraft:pale_oak_sapling
pale_oak_sapling
minecraft:polished_granite
polished_granite
minecraft:pale_oak_wall_sign
pale_oak_wall_sign
minecraft:soul_fire
soul_fire
minecraft:magenta_candle
magenta_candle
minecraft:mangrove_double_slab
mangrove_double_slab
minecraft:smooth_quartz_double_slab
smooth_quartz_double_slab
minecraft:light_gray_stained_glass
light_gray_stained_glass
minecraft:obsidian
obsidian
minecraft:light_gray_stained_glass_pane
light_gray_stained_glass_pane
minecraft:dark_oak_slab
dark_oak_slab
minecraft:deepslate_brick_wall
deepslate_brick_wall
minecraft:waxed_exposed_copper_grate
waxed_exposed_copper_grate
minecraft:oxidized_double_cut_copper_slab
oxidized_double_cut_copper_slab
minecraft:exposed_copper
exposed_copper
minecraft:polished_deepslate_double_slab
polished_deepslate_double_slab
minecraft:waxed_copper_bars
waxed_copper_bars
minecraft:stone_button
stone_button
minecraft:red_nether_brick_double_slab
red_nether_brick_double_slab
minecraft:waxed_copper_bulb
waxed_copper_bulb
minecraft:sponge
sponge
minecraft:exposed_double_cut_copper_slab
exposed_double_cut_copper_slab
minecraft:bamboo_fence
bamboo_fence
minecraft:normal_stone_stairs
normal_stone_stairs
minecraft:diorite_double_slab
diorite_double_slab
minecraft:end_stone_brick_slab
end_stone_brick_slab
minecraft:hardened_clay
hardened_clay
minecraft:birch_hanging_sign
birch_hanging_sign
minecraft:stripped_jungle_log
stripped_jungle_log
minecraft:oxidized_copper_golem_statue
oxidized_copper_golem_statue
minecraft:light_block_9
light_block_9
minecraft:light_block_8
light_block_8
minecraft:light_block_7
light_block_7
minecraft:light_block_6
light_block_6
minecraft:light_block_5
light_block_5
minecraft:light_block_4
light_block_4
minecraft:light_block_3
light_block_3
minecraft:light_block_2
light_block_2
minecraft:light_block_1
light_block_1
minecraft:light_block_0
light_block_0
minecraft:pale_oak_door
pale_oak_door
minecraft:oak_sapling
oak_sapling
minecraft:polished_blackstone_double_slab
polished_blackstone_double_slab
minecraft:light_gray_terracotta
light_gray_terracotta
minecraft:smoker
smoker
minecraft:brown_stained_glass
brown_stained_glass
minecraft:andesite
andesite
minecraft:fire_coral
fire_coral
minecraft:stone
stone
minecraft:smooth_sandstone_slab
smooth_sandstone_slab
minecraft:birch_log
birch_log
minecraft:tuff_brick_wall
tuff_brick_wall
minecraft:purpur_slab
purpur_slab
minecraft:brain_coral
brain_coral
minecraft:stripped_spruce_wood
stripped_spruce_wood
minecraft:orange_wool
orange_wool
minecraft:polished_blackstone_brick_double_slab
polished_blackstone_brick_double_slab
minecraft:crimson_double_slab
crimson_double_slab
minecraft:respawn_anchor
respawn_anchor
minecraft:light_gray_concrete
light_gray_concrete
minecraft:green_candle
green_candle
minecraft:waxed_exposed_copper
waxed_exposed_copper
minecraft:red_sandstone_double_slab
red_sandstone_double_slab
minecraft:birch_wood
birch_wood
minecraft:red_sand
red_sand
minecraft:hay_block
hay_block
minecraft:jungle_wood
jungle_wood
minecraft:waxed_weathered_copper
waxed_weathered_copper
minecraft:infested_cracked_stone_bricks
infested_cracked_stone_bricks
minecraft:waxed_oxidized_cut_copper_slab
waxed_oxidized_cut_copper_slab
minecraft:oak_leaves
oak_leaves
minecraft:resin_clump
resin_clump
minecraft:brain_coral_fan
brain_coral_fan
minecraft:cyan_candle_cake
cyan_candle_cake
minecraft:polished_tuff_wall
polished_tuff_wall
minecraft:bamboo_stairs
bamboo_stairs
minecraft:infested_mossy_stone_bricks
infested_mossy_stone_bricks
minecraft:torch
torch
minecraft:mud_brick_wall
mud_brick_wall
minecraft:honey_block
honey_block
minecraft:underwater_tnt
underwater_tnt
minecraft:dripstone_block
dripstone_block
minecraft:vine
vine
minecraft:red_sandstone_slab
red_sandstone_slab
minecraft:cherry_trapdoor
cherry_trapdoor
minecraft:blackstone_slab
blackstone_slab
minecraft:gold_ore
gold_ore
minecraft:yellow_glazed_terracotta
yellow_glazed_terracotta
minecraft:dried_ghast
dried_ghast
minecraft:warped_planks
warped_planks
minecraft:piston
piston
minecraft:brown_carpet
brown_carpet
minecraft:stone_brick_stairs
stone_brick_stairs
minecraft:dead_bubble_coral_block
dead_bubble_coral_block
minecraft:gray_candle
gray_candle
minecraft:cherry_fence
cherry_fence
minecraft:mangrove_planks
mangrove_planks
minecraft:red_terracotta
red_terracotta
minecraft:diorite_wall
diorite_wall
minecraft:dead_fire_coral_block
dead_fire_coral_block
minecraft:oxidized_copper_bulb
oxidized_copper_bulb
minecraft:magenta_wool
magenta_wool
minecraft:oxidized_copper_bars
oxidized_copper_bars
minecraft:magenta_glazed_terracotta
magenta_glazed_terracotta
minecraft:quartz_double_slab
quartz_double_slab
minecraft:polished_blackstone_brick_wall
polished_blackstone_brick_wall
minecraft:mangrove_slab
mangrove_slab
minecraft:orange_glazed_terracotta
orange_glazed_terracotta
minecraft:smooth_basalt
smooth_basalt
minecraft:waterlily
waterlily
minecraft:stripped_pale_oak_wood
stripped_pale_oak_wood
minecraft:emerald_block
emerald_block
minecraft:suspicious_sand
suspicious_sand
minecraft:mossy_cobblestone_wall
mossy_cobblestone_wall
minecraft:heavy_weighted_pressure_plate
heavy_weighted_pressure_plate
minecraft:purple_stained_glass
purple_stained_glass
minecraft:lightning_rod
lightning_rod
minecraft:acacia_leaves
acacia_leaves
minecraft:black_stained_glass_pane
black_stained_glass_pane
minecraft:cobblestone_wall
cobblestone_wall
minecraft:deepslate_brick_double_slab
deepslate_brick_double_slab
minecraft:spruce_double_slab
spruce_double_slab
minecraft:bamboo_mosaic_slab
bamboo_mosaic_slab
minecraft:dark_oak_log
dark_oak_log
minecraft:acacia_hanging_sign
acacia_hanging_sign
minecraft:ochre_froglight
ochre_froglight
minecraft:tuff_wall
tuff_wall
minecraft:observer
observer
minecraft:redstone_torch
redstone_torch
minecraft:silver_glazed_terracotta
silver_glazed_terracotta
minecraft:granite_stairs
granite_stairs
minecraft:pink_concrete
pink_concrete
minecraft:dark_oak_hanging_sign
dark_oak_hanging_sign
minecraft:brown_mushroom
brown_mushroom
minecraft:cyan_concrete_powder
cyan_concrete_powder
minecraft:dead_fire_coral_wall_fan
dead_fire_coral_wall_fan
minecraft:brown_glazed_terracotta
brown_glazed_terracotta
minecraft:waxed_copper_trapdoor
waxed_copper_trapdoor
minecraft:spruce_shelf
spruce_shelf
minecraft:resin_brick_double_slab
resin_brick_double_slab
minecraft:oxidized_copper
oxidized_copper
minecraft:copper_ore
copper_ore
minecraft:dark_oak_planks
dark_oak_planks
minecraft:birch_pressure_plate
birch_pressure_plate
minecraft:scaffolding
scaffolding
minecraft:sandstone_stairs
sandstone_stairs
minecraft:green_candle_cake
green_candle_cake
minecraft:stripped_bamboo_block
stripped_bamboo_block
minecraft:red_mushroom_block
red_mushroom_block
minecraft:cracked_stone_bricks
cracked_stone_bricks
minecraft:sculk_catalyst
sculk_catalyst
minecraft:cobblestone
cobblestone
minecraft:waxed_lightning_rod
waxed_lightning_rod
minecraft:horn_coral
horn_coral
minecraft:yellow_concrete
yellow_concrete
minecraft:mangrove_shelf
mangrove_shelf
minecraft:cyan_carpet
cyan_carpet
minecraft:warped_shelf
warped_shelf
minecraft:oak_double_slab
oak_double_slab
minecraft:smooth_sandstone_stairs
smooth_sandstone_stairs
minecraft:jungle_pressure_plate
jungle_pressure_plate
minecraft:double_cut_copper_slab
double_cut_copper_slab
minecraft:blue_terracotta
blue_terracotta
minecraft:sandstone
sandstone
minecraft:brown_candle_cake
brown_candle_cake
minecraft:acacia_wall_sign
acacia_wall_sign
minecraft:light_weighted_pressure_plate
light_weighted_pressure_plate
minecraft:undyed_shulker_box
undyed_shulker_box
minecraft:polished_blackstone
polished_blackstone
minecraft:mycelium
mycelium
minecraft:exposed_lightning_rod
exposed_lightning_rod
minecraft:bamboo
bamboo
minecraft:quartz_block
quartz_block
minecraft:pale_oak_planks
pale_oak_planks
minecraft:stone_stairs
stone_stairs
minecraft:waxed_weathered_chiseled_copper
waxed_weathered_chiseled_copper
minecraft:gray_stained_glass
gray_stained_glass
minecraft:green_terracotta
green_terracotta
minecraft:deepslate_brick_slab
deepslate_brick_slab
minecraft:warped_stairs
warped_stairs
minecraft:smithing_table
smithing_table
minecraft:player_head
player_head
minecraft:weathered_copper_grate
weathered_copper_grate
minecraft:poppy
poppy
minecraft:tuff_brick_slab
tuff_brick_slab
minecraft:copper_chain
copper_chain
minecraft:copper_chest
copper_chest
minecraft:mossy_stone_bricks
mossy_stone_bricks
minecraft:green_wool
green_wool
minecraft:green_carpet
green_carpet
minecraft:prismarine_brick_slab
prismarine_brick_slab
minecraft:wooden_door
wooden_door
minecraft:pitcher_plant
pitcher_plant
minecraft:compound_creator
compound_creator
minecraft:spruce_pressure_plate
spruce_pressure_plate
minecraft:netherite_block
netherite_block
minecraft:pink_wool
pink_wool
minecraft:redstone_block
redstone_block
minecraft:birch_fence_gate
birch_fence_gate
minecraft:redstone_wire
redstone_wire
minecraft:quartz_pillar
quartz_pillar
minecraft:waxed_exposed_cut_copper
waxed_exposed_cut_copper
minecraft:lava
lava
minecraft:jungle_hanging_sign
jungle_hanging_sign
minecraft:birch_slab
birch_slab
minecraft:loom
loom
minecraft:waxed_weathered_copper_lantern
waxed_weathered_copper_lantern
minecraft:dead_tube_coral_block
dead_tube_coral_block
minecraft:end_stone
end_stone
minecraft:polished_tuff_double_slab
polished_tuff_double_slab
minecraft:crimson_door
crimson_door
minecraft:mangrove_pressure_plate
mangrove_pressure_plate
minecraft:jungle_shelf
jungle_shelf
minecraft:jungle_slab
jungle_slab
minecraft:light_blue_stained_glass_pane
light_blue_stained_glass_pane
minecraft:glowstone
glowstone
minecraft:stone_pressure_plate
stone_pressure_plate
minecraft:waxed_exposed_cut_copper_stairs
waxed_exposed_cut_copper_stairs
minecraft:mud_brick_slab
mud_brick_slab
minecraft:waxed_exposed_lightning_rod
waxed_exposed_lightning_rod
minecraft:exposed_copper_lantern
exposed_copper_lantern
minecraft:farmland
farmland
minecraft:dead_brain_coral_wall_fan
dead_brain_coral_wall_fan
minecraft:cut_red_sandstone
cut_red_sandstone
minecraft:rail
rail
minecraft:blackstone_wall
blackstone_wall
minecraft:stone_bricks
stone_bricks
minecraft:mossy_cobblestone_stairs
mossy_cobblestone_stairs
minecraft:detector_rail
detector_rail
minecraft:blue_orchid
blue_orchid
minecraft:green_stained_glass_pane
green_stained_glass_pane
minecraft:polished_granite_stairs
polished_granite_stairs
minecraft:birch_leaves
birch_leaves
minecraft:pink_terracotta
pink_terracotta
minecraft:dark_oak_double_slab
dark_oak_double_slab
minecraft:infested_cobblestone
infested_cobblestone
minecraft:pink_candle_cake
pink_candle_cake
minecraft:cracked_deepslate_tiles
cracked_deepslate_tiles
minecraft:brain_coral_wall_fan
brain_coral_wall_fan
minecraft:mangrove_wood
mangrove_wood
minecraft:waxed_exposed_copper_golem_statue
waxed_exposed_copper_golem_statue
minecraft:red_glazed_terracotta
red_glazed_terracotta
minecraft:waxed_oxidized_copper_chest
waxed_oxidized_copper_chest
minecraft:waxed_oxidized_copper_chain
waxed_oxidized_copper_chain
minecraft:dark_oak_fence_gate
dark_oak_fence_gate
minecraft:mossy_cobblestone_slab
mossy_cobblestone_slab
minecraft:bamboo_mosaic_double_slab
bamboo_mosaic_double_slab
minecraft:cobblestone_slab
cobblestone_slab
minecraft:crimson_nylium
crimson_nylium
minecraft:structure_void
structure_void
minecraft:waxed_exposed_copper_bars
waxed_exposed_copper_bars
minecraft:purple_concrete
purple_concrete
minecraft:waxed_exposed_copper_bulb
waxed_exposed_copper_bulb
minecraft:polished_blackstone_brick_slab
polished_blackstone_brick_slab
minecraft:normal_stone_slab
normal_stone_slab
minecraft:spruce_sapling
spruce_sapling
minecraft:yellow_terracotta
yellow_terracotta
minecraft:snow
snow
minecraft:sand
sand
minecraft:daylight_detector
daylight_detector
minecraft:mangrove_standing_sign
mangrove_standing_sign
minecraft:stripped_mangrove_wood
stripped_mangrove_wood
minecraft:conduit
conduit
minecraft:slime
slime
minecraft:copper_torch
copper_torch
minecraft:bone_block
bone_block
minecraft:frame
frame
minecraft:spruce_log
spruce_log
minecraft:lapis_block
lapis_block
minecraft:coal_ore
coal_ore
minecraft:mossy_stone_brick_double_slab
mossy_stone_brick_double_slab
minecraft:cut_red_sandstone_double_slab
cut_red_sandstone_double_slab
minecraft:bamboo_shelf
bamboo_shelf
minecraft:redstone_ore
redstone_ore
minecraft:bamboo_double_slab
bamboo_double_slab
minecraft:waxed_copper_chest
waxed_copper_chest
minecraft:green_stained_glass
green_stained_glass
minecraft:waxed_copper_chain
waxed_copper_chain
minecraft:bubble_coral_block
bubble_coral_block
minecraft:infested_chiseled_stone_bricks
infested_chiseled_stone_bricks
minecraft:nether_brick_fence
nether_brick_fence
minecraft:pink_tulip
pink_tulip
minecraft:oak_slab
oak_slab
minecraft:stripped_pale_oak_log
stripped_pale_oak_log
minecraft:deepslate_tile_slab
deepslate_tile_slab
minecraft:pink_concrete_powder
pink_concrete_powder
minecraft:pale_oak_slab
pale_oak_slab
minecraft:dead_tube_coral
dead_tube_coral
minecraft:nether_wart_block
nether_wart_block
minecraft:prismarine_slab
prismarine_slab
minecraft:prismarine_double_slab
prismarine_double_slab
minecraft:cherry_door
cherry_door
minecraft:crimson_hyphae
crimson_hyphae
minecraft:polished_blackstone_stairs
polished_blackstone_stairs
minecraft:weathered_cut_copper_stairs
weathered_cut_copper_stairs
minecraft:small_dripleaf_block
small_dripleaf_block
minecraft:pink_stained_glass
pink_stained_glass
minecraft:waxed_weathered_copper_grate
waxed_weathered_copper_grate
minecraft:spruce_button
spruce_button
minecraft:acacia_log
acacia_log
minecraft:crimson_trapdoor
crimson_trapdoor
minecraft:basalt
basalt
minecraft:normal_stone_double_slab
normal_stone_double_slab
minecraft:stone_brick_double_slab
stone_brick_double_slab
minecraft:light_blue_terracotta
light_blue_terracotta
minecraft:lit_redstone_lamp
lit_redstone_lamp
minecraft:copper_golem_statue
copper_golem_statue
minecraft:diamond_ore
diamond_ore
minecraft:warped_roots
warped_roots
minecraft:magenta_concrete
magenta_concrete
minecraft:dark_prismarine
dark_prismarine
minecraft:sticky_piston
sticky_piston
minecraft:ender_chest
ender_chest
minecraft:medium_amethyst_bud
medium_amethyst_bud
minecraft:pink_shulker_box
pink_shulker_box
minecraft:warped_double_slab
warped_double_slab
minecraft:jungle_wall_sign
jungle_wall_sign
minecraft:sculk_sensor
sculk_sensor
minecraft:copper_bulb
copper_bulb
minecraft:copper_bars
copper_bars
minecraft:oak_shelf
oak_shelf
minecraft:diorite_stairs
diorite_stairs
minecraft:spruce_leaves
spruce_leaves
minecraft:frog_spawn
frog_spawn
minecraft:acacia_door
acacia_door
minecraft:smooth_sandstone_double_slab
smooth_sandstone_double_slab
minecraft:red_shulker_box
red_shulker_box
minecraft:stripped_cherry_log
stripped_cherry_log
minecraft:crimson_button
crimson_button
minecraft:acacia_planks
acacia_planks
minecraft:fire_coral_block
fire_coral_block
minecraft:magenta_concrete_powder
magenta_concrete_powder
minecraft:iron_door
iron_door
minecraft:honeycomb_block
honeycomb_block
minecraft:polished_blackstone_brick_stairs
polished_blackstone_brick_stairs
minecraft:mangrove_trapdoor
mangrove_trapdoor
minecraft:quartz_ore
quartz_ore
minecraft:daylight_detector_inverted
daylight_detector_inverted
minecraft:barrel
barrel
minecraft:smooth_quartz
smooth_quartz
minecraft:coarse_dirt
coarse_dirt
minecraft:chorus_flower
chorus_flower
minecraft:orange_stained_glass
orange_stained_glass
minecraft:white_stained_glass_pane
white_stained_glass_pane
minecraft:stripped_birch_wood
stripped_birch_wood
minecraft:cracked_nether_bricks
cracked_nether_bricks
minecraft:powered_repeater
powered_repeater
minecraft:light_blue_candle
light_blue_candle
minecraft:pumpkin
pumpkin
minecraft:element_constructor
element_constructor
minecraft:deepslate_tiles
deepslate_tiles
minecraft:smooth_stone
smooth_stone
minecraft:gray_terracotta
gray_terracotta
minecraft:oxidized_copper_trapdoor
oxidized_copper_trapdoor
minecraft:granite_slab
granite_slab
minecraft:white_tulip
white_tulip
minecraft:lime_concrete
lime_concrete
minecraft:black_candle_cake
black_candle_cake
minecraft:red_mushroom
red_mushroom
minecraft:gilded_blackstone
gilded_blackstone
minecraft:magenta_terracotta
magenta_terracotta
minecraft:exposed_cut_copper_stairs
exposed_cut_copper_stairs
minecraft:mangrove_stairs
mangrove_stairs
minecraft:polished_diorite_slab
polished_diorite_slab
minecraft:cut_copper_stairs
cut_copper_stairs
minecraft:lab_table
lab_table
minecraft:waxed_oxidized_copper_lantern
waxed_oxidized_copper_lantern
minecraft:cherry_button
cherry_button
minecraft:yellow_candle_cake
yellow_candle_cake
minecraft:mangrove_fence_gate
mangrove_fence_gate
minecraft:sunflower
sunflower
minecraft:pink_petals
pink_petals
minecraft:bamboo_hanging_sign
bamboo_hanging_sign
minecraft:infested_deepslate
infested_deepslate
minecraft:soul_torch
soul_torch
minecraft:podzol
podzol
minecraft:copper_block
copper_block
minecraft:lit_redstone_ore
lit_redstone_ore
minecraft:deepslate_tile_stairs
deepslate_tile_stairs
minecraft:crimson_fence_gate
crimson_fence_gate
minecraft:deadbush
deadbush
minecraft:waxed_weathered_double_cut_copper_slab
waxed_weathered_double_cut_copper_slab
minecraft:polished_blackstone_bricks
polished_blackstone_bricks
minecraft:red_candle
red_candle
minecraft:cut_copper
cut_copper
minecraft:waxed_weathered_copper_golem_statue
waxed_weathered_copper_golem_statue
minecraft:iron_ore
iron_ore
minecraft:spruce_door
spruce_door
minecraft:frosted_ice
frosted_ice
minecraft:chipped_anvil
chipped_anvil
minecraft:large_amethyst_bud
large_amethyst_bud
minecraft:exposed_copper_door
exposed_copper_door
minecraft:suspicious_gravel
suspicious_gravel
minecraft:warped_trapdoor
warped_trapdoor
minecraft:flowing_water
flowing_water
minecraft:brick_block
brick_block
minecraft:waxed_weathered_copper_trapdoor
waxed_weathered_copper_trapdoor
minecraft:quartz_stairs
quartz_stairs
minecraft:cave_vines
cave_vines
minecraft:magenta_stained_glass_pane
magenta_stained_glass_pane
minecraft:iron_bars
iron_bars
minecraft:white_terracotta
white_terracotta
minecraft:stripped_oak_wood
stripped_oak_wood
minecraft:light_blue_carpet
light_blue_carpet
minecraft:oak_hanging_sign
oak_hanging_sign
minecraft:white_concrete_powder
white_concrete_powder
minecraft:melon_stem
melon_stem
minecraft:crimson_planks
crimson_planks
minecraft:stripped_dark_oak_wood
stripped_dark_oak_wood
minecraft:waxed_weathered_cut_copper
waxed_weathered_cut_copper
minecraft:white_stained_glass
white_stained_glass
minecraft:horn_coral_wall_fan
horn_coral_wall_fan
minecraft:oak_wood
oak_wood
minecraft:purple_stained_glass_pane
purple_stained_glass_pane
minecraft:waxed_oxidized_copper_trapdoor
waxed_oxidized_copper_trapdoor
minecraft:wall_sign
wall_sign
minecraft:jukebox
jukebox
minecraft:stripped_cherry_wood
stripped_cherry_wood
minecraft:jigsaw
jigsaw
minecraft:waxed_oxidized_copper_golem_statue
waxed_oxidized_copper_golem_statue
minecraft:prismarine_wall
prismarine_wall
minecraft:border_block
border_block
minecraft:shroomlight
shroomlight
minecraft:bamboo_fence_gate
bamboo_fence_gate
minecraft:cornflower
cornflower
minecraft:chiseled_polished_blackstone
chiseled_polished_blackstone
minecraft:dark_oak_stairs
dark_oak_stairs
minecraft:deepslate_tile_wall
deepslate_tile_wall
minecraft:glass_pane
glass_pane
minecraft:chiseled_deepslate
chiseled_deepslate
minecraft:cut_copper_slab
cut_copper_slab
minecraft:red_stained_glass
red_stained_glass
minecraft:pale_oak_wood
pale_oak_wood
minecraft:infested_stone_bricks
infested_stone_bricks
minecraft:acacia_pressure_plate
acacia_pressure_plate
minecraft:weathered_lightning_rod
weathered_lightning_rod
minecraft:bamboo_trapdoor
bamboo_trapdoor
minecraft:oxidized_chiseled_copper
oxidized_chiseled_copper
minecraft:mangrove_wall_sign
mangrove_wall_sign
minecraft:raw_copper_block
raw_copper_block
minecraft:tall_dry_grass
tall_dry_grass
minecraft:oxidized_cut_copper_slab
oxidized_cut_copper_slab
minecraft:horn_coral_block
horn_coral_block
minecraft:dark_oak_shelf
dark_oak_shelf
minecraft:beetroot
beetroot
minecraft:light_gray_candle_cake
light_gray_candle_cake
minecraft:white_candle
white_candle
minecraft:andesite_stairs
andesite_stairs
minecraft:birch_planks
birch_planks
minecraft:golden_rail
golden_rail
minecraft:cyan_wool
cyan_wool
minecraft:petrified_oak_double_slab
petrified_oak_double_slab
minecraft:darkoak_wall_sign
darkoak_wall_sign
minecraft:jungle_leaves
jungle_leaves
minecraft:gray_shulker_box
gray_shulker_box
minecraft:red_sandstone_stairs
red_sandstone_stairs
minecraft:cyan_glazed_terracotta
cyan_glazed_terracotta
minecraft:cracked_deepslate_bricks
cracked_deepslate_bricks
minecraft:fire_coral_wall_fan
fire_coral_wall_fan
minecraft:jungle_fence_gate
jungle_fence_gate
minecraft:exposed_copper_grate
exposed_copper_grate
minecraft:waxed_copper_grate
waxed_copper_grate
minecraft:jungle_trapdoor
jungle_trapdoor
minecraft:dirt_with_roots
dirt_with_roots
minecraft:coal_block
coal_block
minecraft:white_wool
white_wool
minecraft:warped_fence_gate
warped_fence_gate
minecraft:cut_sandstone_slab
cut_sandstone_slab
minecraft:skeleton_skull
skeleton_skull
minecraft:exposed_copper_chest
exposed_copper_chest
minecraft:exposed_copper_chain
exposed_copper_chain
minecraft:composter
composter
minecraft:waxed_double_cut_copper_slab
waxed_double_cut_copper_slab
minecraft:kelp
kelp
minecraft:waxed_exposed_copper_door
waxed_exposed_copper_door
minecraft:deepslate_bricks
deepslate_bricks
minecraft:blue_glazed_terracotta
blue_glazed_terracotta
minecraft:light_blue_glazed_terracotta
light_blue_glazed_terracotta
minecraft:rose_bush
rose_bush
minecraft:flowering_azalea
flowering_azalea
minecraft:oxidized_cut_copper
oxidized_cut_copper
minecraft:blue_wool
blue_wool
minecraft:pale_oak_hanging_sign
pale_oak_hanging_sign
minecraft:weeping_vines
weeping_vines
minecraft:chorus_plant
chorus_plant
minecraft:water
water
minecraft:mud_brick_stairs
mud_brick_stairs
minecraft:unpowered_repeater
unpowered_repeater
minecraft:stone_brick_wall
stone_brick_wall
minecraft:smooth_red_sandstone_stairs
smooth_red_sandstone_stairs
minecraft:element_100
element_100
minecraft:element_101
element_101
minecraft:element_102
element_102
minecraft:element_103
element_103
minecraft:element_104
element_104
minecraft:element_105
element_105
minecraft:element_106
element_106
minecraft:element_107
element_107
minecraft:element_108
element_108
minecraft:element_109
element_109
minecraft:element_113
element_113
minecraft:element_112
element_112
minecraft:element_111
element_111
minecraft:element_110
element_110
minecraft:element_117
element_117
minecraft:element_116
element_116
minecraft:element_115
element_115
minecraft:element_114
element_114
minecraft:element_118
element_118
minecraft:andesite_wall
andesite_wall
minecraft:white_glazed_terracotta
white_glazed_terracotta
minecraft:stripped_warped_hyphae
stripped_warped_hyphae
minecraft:trapped_chest
trapped_chest
minecraft:acacia_trapdoor
acacia_trapdoor
minecraft:weathered_copper_chest
weathered_copper_chest
minecraft:brain_coral_block
brain_coral_block
minecraft:weathered_copper_chain
weathered_copper_chain
minecraft:standing_sign
standing_sign
minecraft:bamboo_planks
bamboo_planks
minecraft:glow_lichen
glow_lichen
minecraft:purpur_pillar
purpur_pillar
minecraft:wall_banner
wall_banner
minecraft:twisting_vines
twisting_vines
minecraft:chiseled_copper
chiseled_copper
minecraft:acacia_double_slab
acacia_double_slab
minecraft:dark_oak_door
dark_oak_door
minecraft:oak_fence
oak_fence
minecraft:pale_moss_block
pale_moss_block
minecraft:soul_lantern
soul_lantern
minecraft:dirt
dirt
minecraft:blue_stained_glass
blue_stained_glass
minecraft:deny
deny
minecraft:bee_nest
bee_nest
minecraft:bubble_column
bubble_column
minecraft:campfire
campfire
minecraft:smooth_stone_double_slab
smooth_stone_double_slab
minecraft:light_blue_stained_glass
light_blue_stained_glass
minecraft:soul_soil
soul_soil
minecraft:soul_sand
soul_sand
minecraft:granite_wall
granite_wall
minecraft:spruce_hanging_sign
spruce_hanging_sign
minecraft:polished_diorite
polished_diorite
minecraft:reinforced_deepslate
reinforced_deepslate
minecraft:fletching_table
fletching_table
minecraft:cherry_leaves
cherry_leaves
minecraft:creeper_head
creeper_head
minecraft:black_glazed_terracotta
black_glazed_terracotta
minecraft:waxed_oxidized_cut_copper_stairs
waxed_oxidized_cut_copper_stairs
minecraft:waxed_weathered_copper_bulb
waxed_weathered_copper_bulb
minecraft:dragon_head
dragon_head
minecraft:waxed_weathered_copper_bars
waxed_weathered_copper_bars
minecraft:calibrated_sculk_sensor
calibrated_sculk_sensor
minecraft:dark_prismarine_slab
dark_prismarine_slab
minecraft:copper_trapdoor
copper_trapdoor
minecraft:stripped_acacia_log
stripped_acacia_log
minecraft:cobbled_deepslate_double_slab
cobbled_deepslate_double_slab
minecraft:warped_fence
warped_fence
minecraft:crafting_table
crafting_table
minecraft:sea_pickle
sea_pickle
minecraft:cherry_standing_sign
cherry_standing_sign
minecraft:pale_oak_shelf
pale_oak_shelf
minecraft:brown_concrete_powder
brown_concrete_powder
minecraft:mangrove_hanging_sign
mangrove_hanging_sign
minecraft:waxed_exposed_copper_trapdoor
waxed_exposed_copper_trapdoor
minecraft:brown_candle
brown_candle
minecraft:mossy_stone_brick_stairs
mossy_stone_brick_stairs
minecraft:end_rod
end_rod
minecraft:crimson_stem
crimson_stem
minecraft:green_concrete
green_concrete
minecraft:tuff_brick_double_slab
tuff_brick_double_slab
minecraft:crimson_slab
crimson_slab
minecraft:warped_hyphae
warped_hyphae
minecraft:warped_wart_block
warped_wart_block
minecraft:light_gray_shulker_box
light_gray_shulker_box
minecraft:resin_bricks
resin_bricks
minecraft:carrots
carrots
minecraft:tuff_stairs
tuff_stairs
minecraft:yellow_carpet
yellow_carpet
minecraft:cyan_stained_glass
cyan_stained_glass
minecraft:black_stained_glass
black_stained_glass
minecraft:waxed_oxidized_copper_door
waxed_oxidized_copper_door
minecraft:dead_horn_coral
dead_horn_coral
minecraft:andesite_double_slab
andesite_double_slab
minecraft:grass_block
grass_block
minecraft:tripwire_hook
tripwire_hook
minecraft:cave_vines_body_with_berries
cave_vines_body_with_berries
minecraft:dark_oak_pressure_plate
dark_oak_pressure_plate
minecraft:copper_door
copper_door
minecraft:stripped_birch_log
stripped_birch_log
minecraft:tinted_glass
tinted_glass
minecraft:big_dripleaf
big_dripleaf
minecraft:cut_sandstone
cut_sandstone
minecraft:warped_hanging_sign
warped_hanging_sign
minecraft:lime_wool
lime_wool
minecraft:blue_candle_cake
blue_candle_cake
minecraft:sweet_berry_bush
sweet_berry_bush
minecraft:polished_blackstone_slab
polished_blackstone_slab
minecraft:reeds
reeds
minecraft:black_shulker_box
black_shulker_box
minecraft:weathered_copper_golem_statue
weathered_copper_golem_statue
minecraft:jungle_sapling
jungle_sapling
minecraft:chiseled_sandstone
chiseled_sandstone
minecraft:barrier
barrier
minecraft:torchflower_crop
torchflower_crop
minecraft:black_carpet
black_carpet
minecraft:pale_oak_log
pale_oak_log
minecraft:jungle_standing_sign
jungle_standing_sign
minecraft:cherry_double_slab
cherry_double_slab
minecraft:weathered_cut_copper_slab
weathered_cut_copper_slab
minecraft:oxidized_copper_lantern
oxidized_copper_lantern
minecraft:dark_oak_leaves
dark_oak_leaves
minecraft:nether_brick_slab
nether_brick_slab
minecraft:fire
fire
minecraft:fern
fern
minecraft:purpur_double_slab
purpur_double_slab
minecraft:torchflower
torchflower
minecraft:short_dry_grass
short_dry_grass
minecraft:infested_stone
infested_stone
minecraft:pale_hanging_moss
pale_hanging_moss
minecraft:pale_moss_carpet
pale_moss_carpet
minecraft:end_portal_frame
end_portal_frame
minecraft:bamboo_pressure_plate
bamboo_pressure_plate
minecraft:prismarine
prismarine
minecraft:magenta_candle_cake
magenta_candle_cake
minecraft:exposed_copper_trapdoor
exposed_copper_trapdoor
minecraft:mushroom_stem
mushroom_stem
minecraft:black_terracotta
black_terracotta
minecraft:resin_brick_stairs
resin_brick_stairs
minecraft:deepslate_gold_ore
deepslate_gold_ore
minecraft:ancient_debris
ancient_debris
minecraft:vault
vault
minecraft:beehive
beehive
minecraft:jungle_door
jungle_door
minecraft:glass
glass
minecraft:wither_rose
wither_rose
minecraft:nether_brick_double_slab
nether_brick_double_slab
minecraft:exposed_cut_copper
exposed_cut_copper
minecraft:waxed_weathered_cut_copper_stairs
waxed_weathered_cut_copper_stairs
minecraft:mangrove_roots
mangrove_roots
minecraft:yellow_candle
yellow_candle
minecraft:acacia_stairs
acacia_stairs
minecraft:bamboo_mosaic_stairs
bamboo_mosaic_stairs
minecraft:brown_concrete
brown_concrete
minecraft:cherry_slab
cherry_slab
minecraft:chiseled_resin_bricks
chiseled_resin_bricks
minecraft:bubble_coral
bubble_coral
minecraft:orange_shulker_box
orange_shulker_box
minecraft:light_gray_candle
light_gray_candle
minecraft:polished_blackstone_pressure_plate
polished_blackstone_pressure_plate
minecraft:acacia_standing_sign
acacia_standing_sign
minecraft:polished_granite_slab
polished_granite_slab
minecraft:smooth_red_sandstone_double_slab
smooth_red_sandstone_double_slab
minecraft:tuff_brick_stairs
tuff_brick_stairs
minecraft:blue_shulker_box
blue_shulker_box
minecraft:exposed_copper_bulb
exposed_copper_bulb
minecraft:exposed_copper_bars
exposed_copper_bars
minecraft:dead_fire_coral
dead_fire_coral
minecraft:stone_brick_slab
stone_brick_slab
minecraft:crimson_stairs
crimson_stairs
minecraft:waxed_oxidized_copper_bars
waxed_oxidized_copper_bars
minecraft:stripped_spruce_log
stripped_spruce_log
minecraft:waxed_oxidized_copper_bulb
waxed_oxidized_copper_bulb
minecraft:pumpkin_stem
pumpkin_stem
minecraft:azalea_leaves_flowered
azalea_leaves_flowered
minecraft:sticky_piston_arm_collision
sticky_piston_arm_collision
minecraft:warped_nylium
warped_nylium
minecraft:deepslate_emerald_ore
deepslate_emerald_ore
minecraft:acacia_sapling
acacia_sapling
minecraft:quartz_bricks
quartz_bricks
minecraft:andesite_slab
andesite_slab
minecraft:unpowered_comparator
unpowered_comparator
minecraft:lime_candle
lime_candle
minecraft:structure_block
structure_block
minecraft:end_brick_stairs
end_brick_stairs
minecraft:purple_terracotta
purple_terracotta
minecraft:target
target
minecraft:wooden_button
wooden_button
minecraft:mangrove_door
mangrove_door
minecraft:end_stone_brick_double_slab
end_stone_brick_double_slab
minecraft:weathered_copper_door
weathered_copper_door
minecraft:pearlescent_froglight
pearlescent_froglight
minecraft:bamboo_button
bamboo_button
minecraft:tall_grass
tall_grass
minecraft:weathered_copper_lantern
weathered_copper_lantern
minecraft:light_block_12
light_block_12
minecraft:light_block_13
light_block_13
minecraft:light_block_10
light_block_10
minecraft:light_block_11
light_block_11
minecraft:light_block_14
light_block_14
minecraft:light_block_15
light_block_15
minecraft:nether_sprouts
nether_sprouts
minecraft:cyan_stained_glass_pane
cyan_stained_glass_pane
minecraft:dead_horn_coral_block
dead_horn_coral_block
minecraft:verdant_froglight
verdant_froglight
minecraft:resin_block
resin_block
minecraft:warped_slab
warped_slab
minecraft:warped_stem
warped_stem
minecraft:horn_coral_fan
horn_coral_fan
minecraft:green_shulker_box
green_shulker_box
minecraft:large_fern
large_fern
minecraft:stripped_crimson_hyphae
stripped_crimson_hyphae
minecraft:cocoa
cocoa
minecraft:lever
lever
minecraft:bamboo_slab
bamboo_slab
minecraft:brick_stairs
brick_stairs
minecraft:weathered_copper_trapdoor
weathered_copper_trapdoor
minecraft:smooth_red_sandstone_slab
smooth_red_sandstone_slab
minecraft:moss_block
moss_block
minecraft:purple_concrete_powder
purple_concrete_powder
minecraft:pink_glazed_terracotta
pink_glazed_terracotta
minecraft:short_grass
short_grass
minecraft:waxed_weathered_cut_copper_slab
waxed_weathered_cut_copper_slab
minecraft:fire_coral_fan
fire_coral_fan
minecraft:spruce_trapdoor
spruce_trapdoor
minecraft:chain_command_block
chain_command_block
minecraft:red_sandstone
red_sandstone
minecraft:red_nether_brick_slab
red_nether_brick_slab
minecraft:exposed_chiseled_copper
exposed_chiseled_copper
minecraft:spruce_fence_gate
spruce_fence_gate
minecraft:exposed_cut_copper_slab
exposed_cut_copper_slab
minecraft:red_nether_brick_stairs
red_nether_brick_stairs
minecraft:green_glazed_terracotta
green_glazed_terracotta
minecraft:jungle_planks
jungle_planks
minecraft:deepslate_redstone_ore
deepslate_redstone_ore
minecraft:dead_brain_coral_block
dead_brain_coral_block
minecraft:mangrove_fence
mangrove_fence
minecraft:oxidized_copper_grate
oxidized_copper_grate
minecraft:anvil
anvil
minecraft:birch_trapdoor
birch_trapdoor
minecraft:tuff_bricks
tuff_bricks
minecraft:mangrove_leaves
mangrove_leaves
minecraft:cobbled_deepslate
cobbled_deepslate
minecraft:quartz_slab
quartz_slab
minecraft:bookshelf
bookshelf
minecraft:mud
mud
minecraft:lit_pumpkin
lit_pumpkin
minecraft:ice
ice
minecraft:air
air
minecraft:bed
bed
minecraft:black_concrete
black_concrete
minecraft:tnt
tnt
minecraft:purple_candle_cake
purple_candle_cake
minecraft:web
web
minecraft:dead_tube_coral_fan
dead_tube_coral_fan
minecraft:oxidized_copper_chest
oxidized_copper_chest
minecraft:oxidized_copper_chain
oxidized_copper_chain
minecraft:pale_oak_standing_sign
pale_oak_standing_sign
minecraft:polished_diorite_stairs
polished_diorite_stairs
minecraft:blue_concrete_powder
blue_concrete_powder
minecraft:orange_concrete
orange_concrete
minecraft:crying_obsidian
crying_obsidian
minecraft:lime_carpet
lime_carpet
minecraft:closed_eyeblossom
closed_eyeblossom
minecraft:dead_fire_coral_fan
dead_fire_coral_fan
minecraft:decorated_pot
decorated_pot
minecraft:granite_double_slab
granite_double_slab
minecraft:enchanting_table
enchanting_table
minecraft:polished_blackstone_wall
polished_blackstone_wall
minecraft:waxed_exposed_double_cut_copper_slab
waxed_exposed_double_cut_copper_slab
minecraft:bubble_coral_wall_fan
bubble_coral_wall_fan
minecraft:orange_tulip
orange_tulip
minecraft:brown_shulker_box
brown_shulker_box
minecraft:azalea
azalea
minecraft:mud_bricks
mud_bricks
minecraft:birch_wall_sign
birch_wall_sign
minecraft:bamboo_wall_sign
bamboo_wall_sign
minecraft:acacia_wood
acacia_wood
minecraft:gray_stained_glass_pane
gray_stained_glass_pane
minecraft:hopper
hopper
minecraft:bell
bell
minecraft:lectern
lectern
minecraft:bush
bush
minecraft:stripped_crimson_stem
stripped_crimson_stem
minecraft:standing_banner
standing_banner
minecraft:light_blue_shulker_box
light_blue_shulker_box
minecraft:jungle_stairs
jungle_stairs
minecraft:mangrove_propagule
mangrove_propagule
minecraft:cactus
cactus
minecraft:budding_amethyst
budding_amethyst
minecraft:sniffer_egg
sniffer_egg
minecraft:polished_diorite_double_slab
polished_diorite_double_slab
minecraft:birch_stairs
birch_stairs
minecraft:nether_brick_wall
nether_brick_wall
minecraft:purple_glazed_terracotta
purple_glazed_terracotta
minecraft:green_concrete_powder
green_concrete_powder
minecraft:bedrock
bedrock
minecraft:spruce_slab
spruce_slab
minecraft:blackstone_stairs
blackstone_stairs
minecraft:blue_ice
blue_ice
minecraft:cyan_shulker_box
cyan_shulker_box
minecraft:polished_andesite_stairs
polished_andesite_stairs
minecraft:dead_horn_coral_wall_fan
dead_horn_coral_wall_fan
minecraft:piglin_head
piglin_head
minecraft:sculk
sculk
minecraft:netherrack
netherrack
minecraft:purple_candle
purple_candle
minecraft:spruce_standing_sign
spruce_standing_sign
minecraft:mangrove_button
mangrove_button
minecraft:orange_carpet
orange_carpet
minecraft:dead_horn_coral_fan
dead_horn_coral_fan
minecraft:lantern
lantern
minecraft:crimson_shelf
crimson_shelf
minecraft:waxed_weathered_copper_door
waxed_weathered_copper_door
minecraft:red_stained_glass_pane
red_stained_glass_pane
minecraft:lit_blast_furnace
lit_blast_furnace
minecraft:waxed_oxidized_lightning_rod
waxed_oxidized_lightning_rod
minecraft:pink_stained_glass_pane
pink_stained_glass_pane
minecraft:light_blue_wool
light_blue_wool
minecraft:allow
allow
minecraft:dark_oak_fence
dark_oak_fence
minecraft:birch_door
birch_door
minecraft:cherry_shelf
cherry_shelf
minecraft:chest
chest
minecraft:cherry_wood
cherry_wood
minecraft:clay
clay
minecraft:cherry_stairs
cherry_stairs
minecraft:cake
cake
minecraft:crimson_hanging_sign
crimson_hanging_sign
minecraft:sculk_vein
sculk_vein
minecraft:dead_brain_coral
dead_brain_coral
minecraft:deepslate_coal_ore
deepslate_coal_ore
minecraft:weathered_cut_copper
weathered_cut_copper
minecraft:warped_standing_sign
warped_standing_sign
minecraft:polished_andesite_double_slab
polished_andesite_double_slab
minecraft:cracked_polished_blackstone_bricks
cracked_polished_blackstone_bricks
minecraft:bamboo_standing_sign
bamboo_standing_sign
minecraft:flowing_lava
flowing_lava
minecraft:wither_skeleton_skull
wither_skeleton_skull
minecraft:polished_tuff
polished_tuff
minecraft:magenta_stained_glass
magenta_stained_glass
minecraft:acacia_button
acacia_button
minecraft:lit_furnace
lit_furnace
minecraft:chiseled_nether_bricks
chiseled_nether_bricks
minecraft:warped_button
warped_button
minecraft:red_concrete_powder
red_concrete_powder
minecraft:light_gray_concrete_powder
light_gray_concrete_powder
minecraft:deepslate_lapis_ore
deepslate_lapis_ore
minecraft:dead_bubble_coral
dead_bubble_coral
minecraft:cherry_sapling
cherry_sapling
minecraft:cherry_log
cherry_log
minecraft:prismarine_stairs
prismarine_stairs
minecraft:white_carpet
white_carpet
minecraft:cyan_concrete
cyan_concrete
minecraft:polished_tuff_stairs
polished_tuff_stairs
minecraft:dragon_egg
dragon_egg
minecraft:blue_concrete
blue_concrete
minecraft:nether_brick
nether_brick
minecraft:deepslate_iron_ore
deepslate_iron_ore
minecraft:element_1
element_1
minecraft:element_0
element_0
minecraft:element_3
element_3
minecraft:element_2
element_2
minecraft:element_5
element_5
minecraft:element_4
element_4
minecraft:element_7
element_7
minecraft:element_6
element_6
minecraft:element_9
element_9
minecraft:element_8
element_8
minecraft:oxeye_daisy
oxeye_daisy
minecraft:wheat
wheat
minecraft:waxed_cut_copper
waxed_cut_copper
minecraft:iron_chain
iron_chain
minecraft:resin_brick_slab
resin_brick_slab
minecraft:heavy_core
heavy_core
minecraft:cobbled_deepslate_slab
cobbled_deepslate_slab
minecraft:lilac
lilac
minecraft:pale_oak_trapdoor
pale_oak_trapdoor
minecraft:chiseled_quartz_block
chiseled_quartz_block
minecraft:spore_blossom
spore_blossom
minecraft:waxed_exposed_copper_lantern
waxed_exposed_copper_lantern
minecraft:crimson_standing_sign
crimson_standing_sign
minecraft:darkoak_standing_sign
darkoak_standing_sign
minecraft:weathered_double_cut_copper_slab
weathered_double_cut_copper_slab
minecraft:pale_oak_stairs
pale_oak_stairs
minecraft:emerald_ore
emerald_ore
minecraft:brown_mushroom_block
brown_mushroom_block
minecraft:gray_concrete_powder
gray_concrete_powder
minecraft:petrified_oak_slab
petrified_oak_slab
minecraft:gray_concrete
gray_concrete
minecraft:pink_candle
pink_candle
minecraft:red_nether_brick_wall
red_nether_brick_wall
minecraft:purple_shulker_box
purple_shulker_box
minecraft:carved_pumpkin
carved_pumpkin
minecraft:dropper
dropper
minecraft:spruce_wall_sign
spruce_wall_sign
minecraft:stripped_warped_stem
stripped_warped_stem
minecraft:candle
candle
minecraft:polished_andesite_slab
polished_andesite_slab
minecraft:pointed_dripstone
pointed_dripstone
minecraft:red_carpet
red_carpet
minecraft:cut_red_sandstone_slab
cut_red_sandstone_slab
minecraft:deepslate_brick_stairs
deepslate_brick_stairs
minecraft:dark_prismarine_stairs
dark_prismarine_stairs
minecraft:creaking_heart
creaking_heart
minecraft:pale_oak_button
pale_oak_button
minecraft:chiseled_tuff_bricks
chiseled_tuff_bricks
minecraft:light_blue_concrete
light_blue_concrete
minecraft:exposed_copper_golem_statue
exposed_copper_golem_statue
minecraft:red_tulip
red_tulip
minecraft:trip_wire
trip_wire
minecraft:cauldron
cauldron
minecraft:cave_vines_head_with_berries
cave_vines_head_with_berries
minecraft:tube_coral_block
tube_coral_block
minecraft:chiseled_red_sandstone
chiseled_red_sandstone
minecraft:dead_tube_coral_wall_fan
dead_tube_coral_wall_fan
minecraft:birch_sapling
birch_sapling
minecraft:dark_oak_trapdoor
dark_oak_trapdoor
minecraft:orange_terracotta
orange_terracotta
minecraft:brick_slab
brick_slab
minecraft:waxed_oxidized_copper
waxed_oxidized_copper
minecraft:oak_planks
oak_planks
minecraft:stripped_oak_log
stripped_oak_log
minecraft:smooth_stone_slab
smooth_stone_slab
minecraft:polished_andesite
polished_andesite
minecraft:sea_lantern
sea_lantern
minecraft:brewing_stand
brewing_stand
minecraft:bamboo_sapling
bamboo_sapling
minecraft:weathered_copper_bulb
weathered_copper_bulb
minecraft:weathered_copper_bars
weathered_copper_bars
minecraft:blast_furnace
blast_furnace
minecraft:crimson_roots
crimson_roots
minecraft:acacia_slab
acacia_slab
minecraft:stonecutter_block
stonecutter_block
minecraft:smooth_quartz_slab
smooth_quartz_slab
minecraft:yellow_concrete_powder
yellow_concrete_powder
minecraft:white_candle_cake
white_candle_cake
minecraft:candle_cake
candle_cake
minecraft:lime_stained_glass_pane
lime_stained_glass_pane
minecraft:end_portal
end_portal
minecraft:yellow_stained_glass
yellow_stained_glass
minecraft:jungle_double_slab
jungle_double_slab
minecraft:polished_granite_double_slab
polished_granite_double_slab
minecraft:spruce_wood
spruce_wood
minecraft:blackstone
blackstone
minecraft:acacia_fence_gate
acacia_fence_gate
minecraft:lit_deepslate_redstone_ore
lit_deepslate_redstone_ore
minecraft:wildflowers
wildflowers
minecraft:element_10
element_10
minecraft:element_11
element_11
minecraft:element_12
element_12
minecraft:element_13
element_13
minecraft:element_14
element_14
minecraft:element_15
element_15
minecraft:element_16
element_16
minecraft:element_17
element_17
minecraft:element_18
element_18
minecraft:element_19
element_19
minecraft:element_36
element_36
minecraft:element_37
element_37
minecraft:element_34
element_34
minecraft:element_35
element_35
minecraft:element_32
element_32
minecraft:element_33
element_33
minecraft:element_30
element_30
minecraft:element_31
element_31
minecraft:element_38
element_38
minecraft:element_39
element_39
minecraft:element_29
element_29
minecraft:element_28
element_28
minecraft:element_21
element_21
minecraft:element_20
element_20
minecraft:element_23
element_23
minecraft:element_22
element_22
minecraft:element_25
element_25
minecraft:element_24
element_24
minecraft:element_27
element_27
minecraft:element_26
element_26
minecraft:element_58
element_58
minecraft:element_59
element_59
minecraft:element_54
element_54
minecraft:element_55
element_55
minecraft:element_56
element_56
minecraft:element_57
element_57
minecraft:element_50
element_50
minecraft:element_51
element_51
minecraft:element_52
element_52
minecraft:element_53
element_53
minecraft:element_49
element_49
minecraft:element_48
element_48
minecraft:element_47
element_47
minecraft:element_46
element_46
minecraft:element_45
element_45
minecraft:element_44
element_44
minecraft:element_43
element_43
minecraft:element_42
element_42
minecraft:element_41
element_41
minecraft:element_40
element_40
minecraft:element_72
element_72
minecraft:element_73
element_73
minecraft:element_70
element_70
minecraft:element_71
element_71
minecraft:element_76
element_76
minecraft:element_77
element_77
minecraft:element_74
element_74
minecraft:element_75
element_75
minecraft:element_78
element_78
minecraft:element_79
element_79
minecraft:element_65
element_65
minecraft:element_64
element_64
minecraft:element_67
element_67
minecraft:element_66
element_66
minecraft:element_61
element_61
minecraft:element_60
element_60
minecraft:element_63
element_63
minecraft:element_62
element_62
minecraft:element_69
element_69
minecraft:element_68
element_68
minecraft:element_98
element_98
minecraft:element_99
element_99
minecraft:element_90
element_90
minecraft:element_91
element_91
minecraft:element_92
element_92
minecraft:element_93
element_93
minecraft:element_94
element_94
minecraft:element_95
element_95
minecraft:element_96
element_96
minecraft:element_97
element_97
minecraft:element_89
element_89
minecraft:element_88
element_88
minecraft:element_83
element_83
minecraft:element_82
element_82
minecraft:element_81
element_81
minecraft:element_80
element_80
minecraft:element_87
element_87
minecraft:element_86
element_86
minecraft:element_85
element_85
minecraft:element_84
element_84
minecraft:lit_smoker
lit_smoker
minecraft:lapis_ore
lapis_ore
minecraft:red_concrete
red_concrete
minecraft:pink_carpet
pink_carpet
minecraft:smooth_quartz_stairs
smooth_quartz_stairs
minecraft:red_candle_cake
red_candle_cake
minecraft:waxed_copper_lantern
waxed_copper_lantern
minecraft:azalea_leaves
azalea_leaves
minecraft:purpur_block
purpur_block
minecraft:cherry_wall_sign
cherry_wall_sign
minecraft:cyan_candle
cyan_candle
minecraft:waxed_copper
waxed_copper
minecraft:repeating_command_block
repeating_command_block
minecraft:nether_wart
nether_wart
minecraft:purple_carpet
purple_carpet
minecraft:waxed_oxidized_double_cut_copper_slab
waxed_oxidized_double_cut_copper_slab
minecraft:crimson_fungus
crimson_fungus
minecraft:cherry_planks
cherry_planks
minecraft:polished_deepslate
polished_deepslate
minecraft:tuff_double_slab
tuff_double_slab
minecraft:smooth_red_sandstone
smooth_red_sandstone
minecraft:purpur_stairs
purpur_stairs
minecraft:tube_coral
tube_coral
minecraft:waxed_copper_door
waxed_copper_door
minecraft:portal
portal
minecraft:birch_button
birch_button
minecraft:peony
peony
minecraft:command_block
command_block
minecraft:polished_blackstone_button
polished_blackstone_button
minecraft:crafter
crafter
minecraft:spruce_planks
spruce_planks
minecraft:mossy_cobblestone_double_slab
mossy_cobblestone_double_slab
minecraft:furnace
furnace
minecraft:amethyst_cluster
amethyst_cluster
minecraft:waxed_chiseled_copper
waxed_chiseled_copper
minecraft:waxed_cut_copper_slab
waxed_cut_copper_slab
minecraft:polished_deepslate_wall
polished_deepslate_wall
minecraft:prismarine_brick_double_slab
prismarine_brick_double_slab
minecraft:dried_kelp_block
dried_kelp_block
minecraft:crimson_fence
crimson_fence
minecraft:chiseled_tuff
chiseled_tuff
minecraft:lime_concrete_powder
lime_concrete_powder
minecraft:turtle_egg
turtle_egg
minecraft:magma
magma
minecraft:dispenser
dispenser
minecraft:brown_terracotta
brown_terracotta
minecraft:cobblestone_double_slab
cobblestone_double_slab
minecraft:deepslate_diamond_ore
deepslate_diamond_ore
minecraft:grindstone
grindstone
minecraft:waxed_copper_golem_statue
waxed_copper_golem_statue
minecraft:light_gray_wool
light_gray_wool
minecraft:soul_campfire
soul_campfire
minecraft:prismarine_bricks
prismarine_bricks
minecraft:wooden_pressure_plate
wooden_pressure_plate
minecraft:sandstone_wall
sandstone_wall
minecraft:birch_fence
birch_fence
minecraft:lime_candle_cake
lime_candle_cake
minecraft:waxed_oxidized_copper_grate
waxed_oxidized_copper_grate
minecraft:damaged_anvil
damaged_anvil
minecraft:birch_double_slab
birch_double_slab
minecraft:white_concrete
white_concrete
minecraft:material_reducer
material_reducer
minecraft:trial_spawner
trial_spawner
minecraft:acacia_fence
acacia_fence
minecraft:grass_path
grass_path
minecraft:resin_brick_wall
resin_brick_wall
minecraft:cobbled_deepslate_wall
cobbled_deepslate_wall
minecraft:waxed_weathered_lightning_rod
waxed_weathered_lightning_rod
minecraft:orange_concrete_powder
orange_concrete_powder
minecraft:orange_candle_cake
orange_candle_cake
minecraft:weathered_copper
weathered_copper
minecraft:mossy_stone_brick_wall
mossy_stone_brick_wall
minecraft:unlit_redstone_torch
unlit_redstone_torch
minecraft:pale_oak_double_slab
pale_oak_double_slab
minecraft:lime_terracotta
lime_terracotta
minecraft:cherry_fence_gate
cherry_fence_gate
minecraft:gray_glazed_terracotta
gray_glazed_terracotta
minecraft:lodestone
lodestone
minecraft:bamboo_mosaic
bamboo_mosaic
minecraft:raw_iron_block
raw_iron_block
minecraft:light_gray_carpet
light_gray_carpet
minecraft:purple_wool
purple_wool
minecraft:iron_block
iron_block
minecraft:ladder
ladder
minecraft:crimson_pressure_plate
crimson_pressure_plate
minecraft:stripped_mangrove_log
stripped_mangrove_log
minecraft:copper_lantern
copper_lantern
minecraft:gravel
gravel
minecraft:cartography_table
cartography_table
minecraft:oxidized_copper_door
oxidized_copper_door
minecraft:tube_coral_wall_fan
tube_coral_wall_fan
minecraft:dandelion
dandelion
movingblock
minecraft:movingblock
invisiblebedrock
minecraft:invisiblebedrock
grass
minecraft:grass
concretepowder
minecraft:concretepowder
pistonarmcollision
minecraft:pistonarmcollision
stone_slab4
minecraft:stone_slab4
stone_slab
minecraft:stone_slab
tripwire
minecraft:tripwire
sealantern
minecraft:sealantern
stone_slab2
minecraft:stone_slab2
stickypistonarmcollision
minecraft:stickypistonarmcollision
stone_slab3
minecraft:stone_slab3
double_stone_slab
minecraft:double_stone_slab
double_stone_slab2
minecraft:double_stone_slab2
double_stone_slab3
minecraft:double_stone_slab3
double_stone_slab4
minecraft:double_stone_slab4
yellow_flower
minecraft:yellow_flower
chain
minecraft:chain
wool
minecraft:wool
log
minecraft:log
log2
minecraft:log2
coral
minecraft:coral
fence
minecraft:fence
carpet
minecraft:carpet
shulker_box
minecraft:shulker_box
concrete
minecraft:concrete
stained_hardened_clay
minecraft:stained_hardened_clay
concrete_powder
minecraft:concrete_powder
stained_glass
minecraft:stained_glass
stained_glass_pane
minecraft:stained_glass_pane
planks
minecraft:planks
wooden_slab
minecraft:wooden_slab
double_wooden_slab
minecraft:double_wooden_slab
leaves
minecraft:leaves
leaves2
minecraft:leaves2
wood
minecraft:wood
sapling
minecraft:sapling
coral_fan
minecraft:coral_fan
coral_fan_dead
minecraft:coral_fan_dead
red_flower
minecraft:red_flower
tallgrass
minecraft:tallgrass
coral_block
minecraft:coral_block
double_plant
minecraft:double_plant
stone_block_slab
minecraft:stone_block_slab
stone_block_slab2
minecraft:stone_block_slab2
stone_block_slab3
minecraft:stone_block_slab3
stone_block_slab4
minecraft:stone_block_slab4
double_stone_block_slab
minecraft:double_stone_block_slab
double_stone_block_slab2
minecraft:double_stone_block_slab2
double_stone_block_slab3
minecraft:double_stone_block_slab3
double_stone_block_slab4
minecraft:double_stone_block_slab4
monster_egg
minecraft:monster_egg
stonebrick
minecraft:stonebrick
coral_fan_hang
minecraft:coral_fan_hang
coral_fan_hang2
minecraft:coral_fan_hang2
coral_fan_hang3
minecraft:coral_fan_hang3
light_block
minecraft:light_block
chemistry_table
minecraft:chemistry_table
skull
minecraft:skull
lava_cauldron
minecraft:lava_cauldron
```

</details>

#### Static Enum: features (#25)

Value count: 240

<details>
<summary>Show all values</summary>

```
minecraft:optional_log_mushrooms_feature
minecraft:copper_ore_feature
minecraft:fixup_mesa_gold_position_feature
minecraft:silverfish_feature
minecraft:grass_double_plant_upper_feature
minecraft:scatter_warm_ocean_seagrass_feature
minecraft:random_oak_tree_from_sapling_feature
minecraft:underground_extra_cave_carver_feature
minecraft:scatter_fern_feature
minecraft:dirt_feature
minecraft:scatter_swamp_seagrass_feature
minecraft:tuff_feature
minecraft:pale_oak_tree_feature
minecraft:select_taiga_plant_feature
minecraft:spore_blossom_feature
minecraft:deepslate_feature
minecraft:scatter_ocean_seagrass_feature
minecraft:nether_sprouts_scatter_feature
minecraft:birch_tree_with_optional_beehive_feature
minecraft:beehive_east_feature
minecraft:fern_double_plant_lower_feature
minecraft:roofed_tree_with_vines_feature
minecraft:fixup_fern_double_plant_upper_position_feature
minecraft:cave_vine_snap_to_ceiling_feature
minecraft:tall_grass_feature
minecraft:scatter_birch_forest_wildflowers_feature
minecraft:scatter_overworld_flower_feature
minecraft:scatter_tall_grass_around_forest_foliage_feature
minecraft:scatter_tall_grass_around_tree_feature
minecraft:random_mangrove_tree_feature
minecraft:scatter_deep_warm_ocean_seagrass_feature
minecraft:fancy_oak_tree_feature
minecraft:jungle_bush_feature
minecraft:pine_tree_feature
minecraft:mega_jungle_tree_feature
minecraft:diorite_feature
minecraft:scatter_cold_ocean_seagrass_feature
minecraft:select_birch_tree_feature
minecraft:crimson_fungus_scatter_feature
minecraft:moss_patch_bonemeal_feature
minecraft:birch_tree_with_beehive_feature
minecraft:select_super_birch_tree_feature
minecraft:select_spruce_tree_feature
minecraft:select_oak_tree_feature
minecraft:beehive_wes_order_feature
minecraft:fancy_oak_tree_with_optional_beehive_feature
minecraft:oak_tree_with_optional_beehive_feature
minecraft:fancy_oak_tree_with_beehive_feature
minecraft:super_birch_tree_with_beehive_feature
minecraft:select_birch_tree_with_leaf_litter_feature
minecraft:fancy_oak_tree_with_leaf_litter_and_optional_beehive
minecraft:select_oak_tree_with_leaf_litter_feature
minecraft:emerald_ore_feature
minecraft:select_jungle_tree_feature
minecraft:jungle_tree_feature
minecraft:mega_spruce_tree_feature
minecraft:warped_fungus_feature
minecraft:mega_pine_tree_feature
minecraft:optional_fallen_spruce_tree_feature
minecraft:oak_tree_with_beehive_feature
minecraft:beehive_esw_order_feature
minecraft:redstone_ore_feature
minecraft:creaking_heart_search_feature
minecraft:savanna_tree_feature
minecraft:swamp_tree_feature
minecraft:random_roofed_forest_feature
minecraft:diamond_ore_buried_feature
minecraft:scatter_meadow_wildflowers_feature
minecraft:short_dry_grass_feature
minecraft:scatter_sweet_berry_bush_feature
minecraft:jungle_tall_grass_feature
minecraft:random_oak_tree_with_beehive_from_sapling_feature
minecraft:scatter_red_mushroom_feature
minecraft:cherry_tree_feature
minecraft:big_dripleaf_west_feature
minecraft:select_cocoa_feature
minecraft:random_roofed_forest_feature_with_decoration_feature
minecraft:big_dripleaf_north_feature
minecraft:fallen_spruce_tree_feature
minecraft:cave_vine_feature
minecraft:big_dripleaf_south_feature
minecraft:big_dripleaf_east_feature
minecraft:azalea_tree_feature
minecraft:mangrove_tree_feature
minecraft:tall_mangrove_tree_feature
minecraft:mangrove_tree_with_beenest_feature
minecraft:scatter_meadow_flower_feature
minecraft:tall_mangrove_tree_with_beenest_feature
minecraft:pale_moss_patch_bonemeal_feature
minecraft:beehive_west_feature
minecraft:crimson_fungus_feature
minecraft:warped_roots_scatter_feature
minecraft:crimson_roots_scatter_feature
minecraft:optional_mountain_spruce_tree_feature
minecraft:scatter_dry_grass_feature
minecraft:scatter_meadow_tall_grass_feature
minecraft:scatter_bush_feature
minecraft:optional_spruce_tree_with_vines_feature
minecraft:bamboo_then_podzol_feature
minecraft:grass_double_plant_patch_feature
minecraft:scatter_tall_grass_feature
minecraft:optional_fallen_oak_tree_feature
minecraft:pale_moss_patch_feature
minecraft:random_cherry_tree_feature
minecraft:pink_petals_scatter_feature
minecraft:scatter_deep_cold_ocean_seagrass_feature
minecraft:scatter_deep_ocean_seagrass_feature
minecraft:deepslate_diamond_fossil_feature
minecraft:scatter_flower_forest_flower_feature
minecraft:sunflower_double_plant_patch_feature
minecraft:scatter_jungle_plant_feature
minecraft:scatter_brown_mushroom_feature
minecraft:scatter_taiga_plant_feature
minecraft:nether_cave_carver_feature
minecraft:scatter_plains_flower_feature
minecraft:scatter_river_seagrass_feature
minecraft:fern_feature
minecraft:optional_jungle_tree_cocoa_feature
minecraft:scatter_swamp_flower_feature
minecraft:fixup_waterlily_position_feature
minecraft:fern_double_plant_patch_feature
minecraft:scatter_eyeblossom_feature
minecraft:random_pale_oak_tree_feature
minecraft:diamond_ore_feature
minecraft:sculk_vein_feature
minecraft:mountain_pine_tree_feature
minecraft:mountain_spruce_tree_feature
minecraft:random_clay_with_dripleaves_feature
minecraft:azalea_root_system_snap_to_ceiling_feature
minecraft:random_clay_with_dripleaves_snap_to_floor_feature
minecraft:moss_ceiling_snap_to_ceiling_feature
minecraft:spore_blossom_snap_to_ceiling_feature
minecraft:gold_ore_feature
minecraft:moss_patch_snap_to_floor_feature
minecraft:clay_ore_feature
minecraft:clay_with_dripleaves_feature
minecraft:small_dripstone_feature
minecraft:dripstone_caves_copper_ore_feature
minecraft:fixup_vines_position_feature
minecraft:vines_single_face_scatter_feature
minecraft:gold_ore_extra_feature
minecraft:coal_ore_feature
minecraft:amethyst_geode_feature
minecraft:sunflower_double_plant_lower_feature
minecraft:diamond_ore_large_feature
minecraft:andesite_feature
minecraft:coal_ore_upper_feature
minecraft:gravel_ore_feature
minecraft:beehive_search_feature
minecraft:underground_glow_lichen_feature
minecraft:gold_ore_lower_feature
minecraft:optional_oak_tree_with_vines_feature
minecraft:granite_feature
minecraft:iron_ore_feature
minecraft:optional_undecorated_jungle_tree_with_vines_feature
minecraft:iron_ore_small_feature
minecraft:lapis_ore_buried_feature
minecraft:lapis_ore_feature
minecraft:underground_underwater_cave_carver_feature
minecraft:underwater_magma_underground_feature
minecraft:glow_lichen_feature
minecraft:fossil_feature
minecraft:taiga_tall_grass_feature
minecraft:nether_soul_sand_underground_feature
minecraft:underground_cave_carver_feature
minecraft:fixup_lapis_position_feature
minecraft:warped_fungus_scatter_feature
minecraft:optional_fallen_birch_tree_feature
minecraft:birch_tree_feature
minecraft:optional_fallen_super_birch_tree_feature
minecraft:super_birch_tree_with_optional_beehive_feature
minecraft:select_standing_spruce_tree_feature
minecraft:fallen_super_birch_tree_feature
minecraft:select_standing_oak_tree_feature
minecraft:optional_beehive_feature
minecraft:oak_tree_feature
minecraft:super_birch_tree_feature
minecraft:undecorated_jungle_tree_with_vines_feature
minecraft:select_log_mushroom_feature
minecraft:scatter_leaf_litter_feature
minecraft:optional_fallen_jungle_tree_feature
minecraft:jungle_tree_with_cocoa_feature
minecraft:noop_undecorated_jungle_tree_feature
minecraft:crimson_roots_feature
minecraft:random_dry_grass_block_feature
minecraft:bush_feature
minecraft:optional_podzol_feature
minecraft:grass_double_plant_feature
minecraft:cherry_tree_with_beehive_feature
minecraft:select_jungle_plant_feature
minecraft:sunflower_double_plant_feature
minecraft:fern_double_plant_feature
minecraft:pale_oak_tree_with_decorations_feature
minecraft:pale_oak_tree_with_decorations_and_creaking_heart_feature
minecraft:moss_ceiling_feature
minecraft:moss_patch_feature
minecraft:underwater_magma_feature
minecraft:small_dripstone_snap_to_surface_feature
minecraft:underwater_magma_snap_to_surface_feature
minecraft:optional_tall_grass_feature
minecraft:nether_sprouts_feature
minecraft:random_roofed_forest_feature_with_leaf_litter_feature
minecraft:warped_roots_feature
minecraft:fallen_birch_tree_feature
minecraft:select_beehive_feature
minecraft:spruce_tree_feature
minecraft:fallen_oak_tree_feature
minecraft:fallen_jungle_tree_feature
minecraft:select_undecorated_jungle_tree_feature
minecraft:tall_dry_grass_feature
minecraft:pale_hanging_moss_feature
minecraft:grass_double_plant_lower_feature
minecraft:fixup_grass_double_plant_upper_position_feature
minecraft:jungle_fern_feature
minecraft:fixup_sunflower_double_plant_upper_position_feature
minecraft:scatter_pale_hanging_moss_feature
minecraft:clay_pool_with_dripleaves_feature
minecraft:cave_vine_in_moss_feature
minecraft:beehive_swe_order_feature
minecraft:spruce_tree_with_vines_feature
minecraft:oak_tree_with_vines_feature
minecraft:scatter_jungle_tree_cocoa_feature
minecraft:undecorated_jungle_tree_feature
minecraft:sunflower_double_plant_upper_feature
minecraft:fern_double_plant_upper_feature
minecraft:pale_hanging_moss_snap_to_ceiling_feature
minecraft:creaking_heart_feature
minecraft:select_roofed_tree_feature
minecraft:beehive_south_feature
minecraft:scatter_jungle_tree_lower_cocoa_feature
minecraft:scatter_jungle_tree_upper_cocoa_feature
minecraft:optional_roofed_tree_with_vines_feature
minecraft:roofed_tree_feature
minecraft:optional_log_brown_mushroom_feature
minecraft:beehive_feature
minecraft:optional_lower_cocoa_feature
minecraft:optional_upper_cocoa_feature
minecraft:cocoa_age_0_feature
minecraft:cocoa_age_1_feature
minecraft:cocoa_age_2_feature
```

</details>

#### Static Enum: EntityType (#27)

Value count: 220

<details>
<summary>Show all values</summary>

```
minecraft:slime
slime
minecraft:tnt
tnt
minecraft:camel
minecraft:turtle
minecraft:chicken
minecraft:bee
minecraft:axolotl
minecraft:pig
minecraft:hoglin
minecraft:sniffer
minecraft:cat
minecraft:cow
minecraft:sheep
minecraft:armadillo
minecraft:wolf
minecraft:villager
minecraft:wandering_trader
minecraft:mooshroom
minecraft:squid
minecraft:glow_squid
minecraft:strider
minecraft:rabbit
minecraft:happy_ghast
minecraft:bat
minecraft:iron_golem
minecraft:nautilus
minecraft:snow_golem
minecraft:zombie_nautilus
minecraft:ocelot
minecraft:horse
minecraft:trader_llama
minecraft:llama
minecraft:polar_bear
minecraft:parrot
minecraft:dolphin
minecraft:panda
minecraft:fox
minecraft:goat
minecraft:frog
minecraft:tadpole
minecraft:allay
minecraft:tropicalfish
minecraft:cod
minecraft:zombie_villager
minecraft:pufferfish
minecraft:salmon
minecraft:donkey
minecraft:mule
minecraft:skeleton_horse
minecraft:zombie_horse
minecraft:zombie
minecraft:drowned
minecraft:creeper
minecraft:skeleton
minecraft:spider
minecraft:zombie_pigman
minecraft:enderman
minecraft:silverfish
minecraft:cave_spider
minecraft:ghast
minecraft:magma_cube
minecraft:blaze
minecraft:warden
minecraft:witch
minecraft:stray
minecraft:husk
minecraft:wither_skeleton
minecraft:guardian
minecraft:elder_guardian
minecraft:elder_guardian_ghost
minecraft:wither
minecraft:ender_dragon
minecraft:shulker
minecraft:endermite
minecraft:vindicator
minecraft:evocation_illager
minecraft:vex
minecraft:phantom
minecraft:pillager
minecraft:ravager
minecraft:piglin_brute
minecraft:piglin
minecraft:zoglin
minecraft:breeze
minecraft:bogged
minecraft:creaking
minecraft:copper_golem
minecraft:parched
minecraft:camel_husk
minecraft:minecart
minecraft:hopper_minecart
minecraft:tnt_minecart
minecraft:chest_minecart
minecraft:command_block_minecart
minecraft:xp_bottle
minecraft:xp_orb
minecraft:ender_crystal
minecraft:arrow
minecraft:snowball
minecraft:egg
minecraft:splash_potion
minecraft:leash_knot
minecraft:wind_charge_projectile
minecraft:boat
minecraft:chest_boat
minecraft:lightning_bolt
minecraft:evocation_fang
minecraft:armor_stand
minecraft:fireworks_rocket
minecraft:npc
camel
turtle
chicken
bee
axolotl
pig
hoglin
sniffer
cat
cow
sheep
armadillo
wolf
villager
wandering_trader
mooshroom
squid
glow_squid
strider
rabbit
happy_ghast
bat
iron_golem
nautilus
snow_golem
zombie_nautilus
ocelot
horse
trader_llama
llama
polar_bear
parrot
dolphin
panda
fox
goat
frog
tadpole
allay
tropicalfish
cod
zombie_villager
pufferfish
salmon
donkey
mule
skeleton_horse
zombie_horse
zombie
drowned
creeper
skeleton
spider
zombie_pigman
enderman
silverfish
cave_spider
ghast
magma_cube
blaze
warden
witch
stray
husk
wither_skeleton
guardian
elder_guardian
elder_guardian_ghost
wither
ender_dragon
shulker
endermite
vindicator
evocation_illager
vex
phantom
pillager
ravager
piglin_brute
piglin
zoglin
breeze
bogged
creaking
copper_golem
parched
camel_husk
minecart
hopper_minecart
tnt_minecart
chest_minecart
command_block_minecart
xp_bottle
xp_orb
ender_crystal
arrow
snowball
egg
splash_potion
leash_knot
wind_charge_projectile
boat
chest_boat
lightning_bolt
evocation_fang
armor_stand
fireworks_rocket
npc
```

</details>

#### Static Enum: Biome (#28)

Value count: 86

<details>
<summary>Show all values</summary>

```
minecraft:ocean
minecraft:plains
minecraft:desert
minecraft:extreme_hills
minecraft:forest
minecraft:taiga
minecraft:swampland
minecraft:river
minecraft:hell
minecraft:the_end
minecraft:legacy_frozen_ocean
minecraft:frozen_river
minecraft:ice_plains
minecraft:ice_mountains
minecraft:mushroom_island
minecraft:mushroom_island_shore
minecraft:beach
minecraft:desert_hills
minecraft:forest_hills
minecraft:taiga_hills
minecraft:extreme_hills_edge
minecraft:jungle
minecraft:jungle_hills
minecraft:jungle_edge
minecraft:deep_ocean
minecraft:stone_beach
minecraft:cold_beach
minecraft:birch_forest
minecraft:birch_forest_hills
minecraft:roofed_forest
minecraft:cold_taiga
minecraft:cold_taiga_hills
minecraft:mega_taiga
minecraft:mega_taiga_hills
minecraft:extreme_hills_plus_trees
minecraft:savanna
minecraft:savanna_plateau
minecraft:mesa
minecraft:mesa_plateau_stone
minecraft:mesa_plateau
minecraft:warm_ocean
minecraft:lukewarm_ocean
minecraft:deep_lukewarm_ocean
minecraft:cold_ocean
minecraft:deep_cold_ocean
minecraft:frozen_ocean
minecraft:deep_frozen_ocean
minecraft:bamboo_jungle
minecraft:bamboo_jungle_hills
minecraft:sunflower_plains
minecraft:desert_mutated
minecraft:extreme_hills_mutated
minecraft:flower_forest
minecraft:taiga_mutated
minecraft:swampland_mutated
minecraft:ice_plains_spikes
minecraft:jungle_mutated
minecraft:jungle_edge_mutated
minecraft:birch_forest_mutated
minecraft:birch_forest_hills_mutated
minecraft:roofed_forest_mutated
minecraft:cold_taiga_mutated
minecraft:redwood_taiga_mutated
minecraft:redwood_taiga_hills_mutated
minecraft:extreme_hills_plus_trees_mutated
minecraft:savanna_mutated
minecraft:savanna_plateau_mutated
minecraft:mesa_bryce
minecraft:mesa_plateau_stone_mutated
minecraft:mesa_plateau_mutated
minecraft:soulsand_valley
minecraft:crimson_forest
minecraft:warped_forest
minecraft:basalt_deltas
minecraft:jagged_peaks
minecraft:frozen_peaks
minecraft:snowy_slopes
minecraft:grove
minecraft:meadow
minecraft:lush_caves
minecraft:dripstone_caves
minecraft:stony_peaks
minecraft:deep_dark
minecraft:mangrove_swamp
minecraft:cherry_grove
minecraft:pale_garden
```

</details>

#### Static Enum: Enchant (#29)

Value count: 42

<details>
<summary>Show all values</summary>

```
protection
fire_protection
feather_falling
blast_protection
projectile_protection
thorns
respiration
depth_strider
aqua_affinity
sharpness
smite
bane_of_arthropods
knockback
fire_aspect
looting
efficiency
silk_touch
unbreaking
fortune
power
punch
flame
infinity
luck_of_the_sea
lure
frost_walker
mending
binding
vanishing
impaling
riptide
loyalty
channeling
multishot
piercing
quick_charge
soul_speed
swift_sneak
wind_burst
density
breach
lunge
```

</details>

#### Static Enum: Rotation (#30)

Value count: 4

<details>
<summary>Show all values</summary>

```
0_degrees
90_degrees
180_degrees
270_degrees
```

</details>

#### Static Enum: Mirror (#31)

Value count: 4

<details>
<summary>Show all values</summary>

```
x
z
none
xz
```

</details>

#### Static Enum: Easing (#32)

Value count: 32

<details>
<summary>Show all values</summary>

```
linear
spring
in_quad
out_quad
in_out_quad
in_cubic
out_cubic
in_out_cubic
in_quart
out_quart
in_out_quart
in_quint
out_quint
in_out_quint
in_sine
out_sine
in_out_sine
in_expo
out_expo
in_out_expo
in_circ
out_circ
in_out_circ
in_bounce
out_bounce
in_out_bounce
in_back
out_back
in_out_back
in_elastic
out_elastic
in_out_elastic
```

</details>

#### Static Enum: AimAssistTargetMode (#33)

Value count: 2

<details>
<summary>Show all values</summary>

```
distance
angle
```

</details>

#### Static Enum: AimAssistActionSet (#34)

Value count: 1

<details>
<summary>Show all values</summary>

```
set
```

</details>

#### Static Enum: AimAssistActionClear (#35)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: set (#36)

Value count: 1

<details>
<summary>Show all values</summary>

```
set
```

</details>

#### Static Enum: ease (#37)

Value count: 1

<details>
<summary>Show all values</summary>

```
ease
```

</details>

#### Static Enum: pos (#38)

Value count: 1

<details>
<summary>Show all values</summary>

```
pos
```

</details>

#### Static Enum: rot (#39)

Value count: 1

<details>
<summary>Show all values</summary>

```
rot
```

</details>

#### Static Enum: fov_set (#40)

Value count: 1

<details>
<summary>Show all values</summary>

```
fov_set
```

</details>

#### Static Enum: fov_clear (#41)

Value count: 1

<details>
<summary>Show all values</summary>

```
fov_clear
```

</details>

#### Static Enum: facing (#42)

Value count: 1

<details>
<summary>Show all values</summary>

```
facing
```

</details>

#### Static Enum: target_entity (#43)

Value count: 1

<details>
<summary>Show all values</summary>

```
target_entity
```

</details>

#### Static Enum: target_center_offset (#44)

Value count: 1

<details>
<summary>Show all values</summary>

```
target_center_offset
```

</details>

#### Static Enum: remove_target (#45)

Value count: 1

<details>
<summary>Show all values</summary>

```
remove_target
```

</details>

#### Static Enum: view_offset (#46)

Value count: 1

<details>
<summary>Show all values</summary>

```
view_offset
```

</details>

#### Static Enum: entity_offset (#47)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity_offset
```

</details>

#### Static Enum: default (#48)

Value count: 1

<details>
<summary>Show all values</summary>

```
default
```

</details>

#### Static Enum: clear (#49)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: fade (#50)

Value count: 1

<details>
<summary>Show all values</summary>

```
fade
```

</details>

#### Static Enum: time (#51)

Value count: 1

<details>
<summary>Show all values</summary>

```
time
```

</details>

#### Static Enum: color (#52)

Value count: 1

<details>
<summary>Show all values</summary>

```
color
```

</details>

#### Static Enum: CameraShakeActionAdd (#53)

Value count: 1

<details>
<summary>Show all values</summary>

```
add
```

</details>

#### Static Enum: CameraShakeActionStop (#54)

Value count: 1

<details>
<summary>Show all values</summary>

```
stop
```

</details>

#### Static Enum: CameraShakeType (#55)

Value count: 2

<details>
<summary>Show all values</summary>

```
positional
rotational
```

</details>

#### Static Enum: MaskMode (#56)

Value count: 2

<details>
<summary>Show all values</summary>

```
replace
masked
```

</details>

#### Static Enum: MaskModeFiltered (#57)

Value count: 1

<details>
<summary>Show all values</summary>

```
filtered
```

</details>

#### Static Enum: CloneMode (#58)

Value count: 3

<details>
<summary>Show all values</summary>

```
normal
force
move
```

</details>

#### Static Enum: CameraControlSchemeSet (#59)

Value count: 1

<details>
<summary>Show all values</summary>

```
set
```

</details>

#### Static Enum: CameraControlSchemeClear (#60)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: controlscheme (#61)

Value count: 5

<details>
<summary>Show all values</summary>

```
camera_relative_strafe
camera_relative
player_relative_strafe
player_relative
locked_player_relative_strafe
```

</details>

#### Static Enum: DamageCause (#62)

Value count: 36

<details>
<summary>Show all values</summary>

```
piston
lava
campfire
fire
anvil
magma
soul_campfire
wither
falling_block
fireworks
thorns
none
sonic_boom
contact
override
entity_attack
projectile
suffocation
mace_smash
fall
starve
ram_attack
fire_tick
stalactite
drowning
block_explosion
entity_explosion
void
self_destruct
magic
charging
stalagmite
fly_into_wall
lightning
freezing
temperature
```

</details>

#### Static Enum: DamageOriginActor (#64)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: DialogueOpenAction (#66)

Value count: 1

<details>
<summary>Show all values</summary>

```
open
```

</details>

#### Static Enum: DialogueChangeAction (#67)

Value count: 1

<details>
<summary>Show all values</summary>

```
change
```

</details>

#### Static Enum: Difficulty (#68)

Value count: 8

<details>
<summary>Show all values</summary>

```
normal
peaceful
easy
hard
p
e
n
h
```

</details>

#### Static Enum: ClearEffects (#69)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: AddInfiniteEffect (#70)

Value count: 1

<details>
<summary>Show all values</summary>

```
infinite
```

</details>

#### Static Enum: Effect (#71)

Value count: 37

<details>
<summary>Show all values</summary>

```
wither
speed
slowness
haste
mining_fatigue
strength
instant_health
instant_damage
jump_boost
nausea
regeneration
resistance
fire_resistance
water_breathing
invisibility
blindness
night_vision
hunger
weakness
poison
health_boost
absorption
saturation
levitation
fatal_poison
conduit_power
slow_falling
bad_omen
village_hero
darkness
trial_omen
wind_charged
weaving
oozing
infested
raid_omen
breath_of_the_nautilus
```

</details>

#### Static Enum: EventEntityAction (#72)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: Option_As (#74)

Value count: 1

<details>
<summary>Show all values</summary>

```
as
```

</details>

#### Static Enum: Option_At (#75)

Value count: 1

<details>
<summary>Show all values</summary>

```
at
```

</details>

#### Static Enum: Option_In (#76)

Value count: 1

<details>
<summary>Show all values</summary>

```
in
```

</details>

#### Static Enum: Option_Positioned (#77)

Value count: 1

<details>
<summary>Show all values</summary>

```
positioned
```

</details>

#### Static Enum: Option_Rotated (#78)

Value count: 1

<details>
<summary>Show all values</summary>

```
rotated
```

</details>

#### Static Enum: Option_Facing (#79)

Value count: 1

<details>
<summary>Show all values</summary>

```
facing
```

</details>

#### Static Enum: Option_Entity (#80)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: Option_Align (#81)

Value count: 1

<details>
<summary>Show all values</summary>

```
align
```

</details>

#### Static Enum: Option_Anchored (#82)

Value count: 1

<details>
<summary>Show all values</summary>

```
anchored
```

</details>

#### Static Enum: Option_If_Unless (#83)

Value count: 2

<details>
<summary>Show all values</summary>

```
if
unless
```

</details>

#### Static Enum: Option_Condition_Block (#84)

Value count: 1

<details>
<summary>Show all values</summary>

```
block
```

</details>

#### Static Enum: Option_Condition_Blocks (#85)

Value count: 1

<details>
<summary>Show all values</summary>

```
blocks
```

</details>

#### Static Enum: Option_Condition_Entity (#86)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: Option_Condition_Score (#87)

Value count: 1

<details>
<summary>Show all values</summary>

```
score
```

</details>

#### Static Enum: Option_Run (#88)

Value count: 1

<details>
<summary>Show all values</summary>

```
run
```

</details>

#### Static Enum: ActorLocation (#89)

Value count: 2

<details>
<summary>Show all values</summary>

```
eyes
feet
```

</details>

#### Static Enum: BlocksScanMode (#90)

Value count: 2

<details>
<summary>Show all values</summary>

```
masked
all
```

</details>

#### Static Enum: ScoreRangeMode (#91)

Value count: 1

<details>
<summary>Show all values</summary>

```
matches
```

</details>

#### Static Enum: FillMode (#92)

Value count: 4

<details>
<summary>Show all values</summary>

```
outline
hollow
destroy
keep
```

</details>

#### Static Enum: Replace (#93)

Value count: 1

<details>
<summary>Show all values</summary>

```
replace
```

</details>

#### Static Enum: add (#94)

Value count: 1

<details>
<summary>Show all values</summary>

```
push
```

</details>

#### Static Enum: delete (#95)

Value count: 2

<details>
<summary>Show all values</summary>

```
pop
remove
```

</details>

#### Static Enum: BoolGameRule (#96)

Value count: 33

<details>
<summary>Show all values</summary>

```
commandblockoutput
dodaylightcycle
doentitydrops
dofiretick
recipesunlock
dolimitedcrafting
domobloot
domobspawning
dotiledrops
doweathercycle
drowningdamage
falldamage
firedamage
keepinventory
mobgriefing
pvp
showcoordinates
locatorbar
showdaysplayed
naturalregeneration
tntexplodes
sendcommandfeedback
doinsomnia
commandblocksenabled
doimmediaterespawn
showdeathmessages
showtags
freezedamage
respawnblocksexplode
showbordereffect
showrecipemessages
projectilescanbreakblocks
tntexplosiondropdecay
```

</details>

#### Static Enum: IntGameRule (#97)

Value count: 5

<details>
<summary>Show all values</summary>

```
maxcommandchainlength
randomtickspeed
functioncommandlimit
spawnradius
playerssleepingpercentage
```

</details>

#### Static Enum: GameTestModeRun (#98)

Value count: 1

<details>
<summary>Show all values</summary>

```
run
```

</details>

#### Static Enum: GameTestModeRunThis (#99)

Value count: 1

<details>
<summary>Show all values</summary>

```
runthis
```

</details>

#### Static Enum: GameTestModeRunSet (#100)

Value count: 1

<details>
<summary>Show all values</summary>

```
runset
```

</details>

#### Static Enum: GameTestModeRunSetUntilFail (#101)

Value count: 1

<details>
<summary>Show all values</summary>

```
runsetuntilfail
```

</details>

#### Static Enum: GameTestModeClearAll (#102)

Value count: 1

<details>
<summary>Show all values</summary>

```
clearall
```

</details>

#### Static Enum: GameTestModeShowPosition (#103)

Value count: 1

<details>
<summary>Show all values</summary>

```
pos
```

</details>

#### Static Enum: GameTestModeCreateTest (#104)

Value count: 1

<details>
<summary>Show all values</summary>

```
create
```

</details>

#### Static Enum: GameTestRunNearbyTests (#105)

Value count: 1

<details>
<summary>Show all values</summary>

```
runthese
```

</details>

#### Static Enum: GameTestStopTests (#106)

Value count: 1

<details>
<summary>Show all values</summary>

```
stopall
```

</details>

#### Static Enum: HudElement (#108)

Value count: 14

<details>
<summary>Show all values</summary>

```
hunger
all
paperdoll
armor
tooltips
touch_controls
crosshair
hotbar
health
progress_bar
air_bubbles
horse_health
status_effects
item_text
```

</details>

#### Static Enum: HudVisibility (#109)

Value count: 2

<details>
<summary>Show all values</summary>

```
hide
reset
```

</details>

#### Static Enum: Option_Set (#110)

Value count: 1

<details>
<summary>Show all values</summary>

```
set
```

</details>

#### Static Enum: Option_Query (#111)

Value count: 1

<details>
<summary>Show all values</summary>

```
query
```

</details>

#### Static Enum: permission (#112)

Value count: 11

<details>
<summary>Show all values</summary>

```
camera
movement
jump
lateral_movement
sneak
dismount
mount
move_backward
move_forward
move_left
move_right
```

</details>

#### Static Enum: state (#113)

Value count: 2

<details>
<summary>Show all values</summary>

```
enabled
disabled
```

</details>

#### Static Enum: LocateSubcommandStructure (#115)

Value count: 1

<details>
<summary>Show all values</summary>

```
structure
```

</details>

#### Static Enum: LocateSubcommandBiome (#116)

Value count: 1

<details>
<summary>Show all values</summary>

```
biome
```

</details>

#### Static Enum: TargetSpawn (#117)

Value count: 1

<details>
<summary>Show all values</summary>

```
spawn
```

</details>

#### Static Enum: TargetGive (#118)

Value count: 1

<details>
<summary>Show all values</summary>

```
give
```

</details>

#### Static Enum: TargetInsert (#119)

Value count: 1

<details>
<summary>Show all values</summary>

```
insert
```

</details>

#### Static Enum: TargetReplace (#120)

Value count: 1

<details>
<summary>Show all values</summary>

```
replace
```

</details>

#### Static Enum: TargetEntity (#121)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: TargetBlock (#122)

Value count: 1

<details>
<summary>Show all values</summary>

```
block
```

</details>

#### Static Enum: SourceLoot (#123)

Value count: 1

<details>
<summary>Show all values</summary>

```
loot
```

</details>

#### Static Enum: SourceKill (#124)

Value count: 1

<details>
<summary>Show all values</summary>

```
kill
```

</details>

#### Static Enum: SourceMine (#125)

Value count: 1

<details>
<summary>Show all values</summary>

```
mine
```

</details>

#### Static Enum: BlockEquipmentSlot (#126)

Value count: 1

<details>
<summary>Show all values</summary>

```
slot.container
```

</details>

#### Static Enum: MobEvent (#127)

Value count: 4

<details>
<summary>Show all values</summary>

```
minecraft:pillager_patrols_event
minecraft:wandering_trader_event
minecraft:ender_dragon_event
events_enabled
```

</details>

#### Static Enum: MusicQueueAction (#128)

Value count: 1

<details>
<summary>Show all values</summary>

```
queue
```

</details>

#### Static Enum: MusicPlayAction (#129)

Value count: 1

<details>
<summary>Show all values</summary>

```
play
```

</details>

#### Static Enum: MusicStopAction (#130)

Value count: 1

<details>
<summary>Show all values</summary>

```
stop
```

</details>

#### Static Enum: MusicVolumeAction (#131)

Value count: 1

<details>
<summary>Show all values</summary>

```
volume
```

</details>

#### Static Enum: MusicRepeatMode (#132)

Value count: 2

<details>
<summary>Show all values</summary>

```
play_once
loop
```

</details>

#### Static Enum: stackType (#133)

Value count: 2

<details>
<summary>Show all values</summary>

```
server
client
```

</details>

#### Static Enum: verbose (#134)

Value count: 1

<details>
<summary>Show all values</summary>

```
verbose
```

</details>

#### Static Enum: exclude-vanilla (#135)

Value count: 1

<details>
<summary>Show all values</summary>

```
exclude-vanilla
```

</details>

#### Static Enum: PermissionsAction (#136)

Value count: 2

<details>
<summary>Show all values</summary>

```
list
reload
```

</details>

#### Static Enum: PlaceStructureAction (#139)

Value count: 1

<details>
<summary>Show all values</summary>

```
structure
```

</details>

#### Static Enum: PlaceJigsawAction (#140)

Value count: 1

<details>
<summary>Show all values</summary>

```
jigsaw
```

</details>

#### Static Enum: LiquidSettings (#141)

Value count: 2

<details>
<summary>Show all values</summary>

```
apply_waterlogging
ignore_waterlogging
```

</details>

#### Static Enum: PlaceFeatureAction (#142)

Value count: 1

<details>
<summary>Show all values</summary>

```
feature
```

</details>

#### Static Enum: PlaceFeatureRuleAction (#143)

Value count: 1

<details>
<summary>Show all values</summary>

```
featurerule
```

</details>

#### Static Enum: featureRules (#144)

Value count: 165

<details>
<summary>Show all values</summary>

```
minecraft:warped_fungus_feature
minecraft:nether_cave_carver_feature
minecraft:sculk_vein_feature
minecraft:small_dripstone_feature
minecraft:crimson_roots_feature
minecraft:warped_roots_feature
minecraft:bamboo_jungle_after_surface_bamboo_feature
minecraft:crimson_fungus_warped_feature
minecraft:crimson_roots_warped_feature
minecraft:savanna_surface_flowers_feature
minecraft:savanna_surface_tall_grass_feature
minecraft:overworld_surface_extra_brown_mushroom_feature
minecraft:birch_forest_before_surface_wildflowers_feature_rules
minecraft:grove_spruce_tree_feature
minecraft:bamboo_jungle_surface_tall_grass_feature
minecraft:cherry_biome_surface_double_plant_feature_rules
minecraft:cherry_biome_surface_tall_grass_feature_rules
minecraft:cherry_grove_cherry_tree_feature_rules
minecraft:deep_ocean_after_surface_seagrass_feature_rules
minecraft:forest_surface_tall_grass_feature
minecraft:cherry_grove_surface_pink_petals_feature_rules
minecraft:overworld_surface_extra_red_mushroom_feature
minecraft:swamp_after_surface_seagrass_feature_rules
minecraft:flower_forest_surface_flowers_feature
minecraft:meadow_flowers_feature
minecraft:lush_caves_underground_clay_ore_feature
minecraft:jungle_surface_flowers_feature
minecraft:warped_fungus_crimson_feature
minecraft:jungle_surface_tall_grass_feature
minecraft:overworld_underground_emerald_ore_feature
minecraft:meadow_surface_tall_grass_feature
minecraft:mesa_before_surface_gold_ore_feature
minecraft:pale_garden_pale_oak_tree_feature_rules
minecraft:meadow_after_surface_tall_grass_feature_rules
minecraft:mangrove_swamp_mangrove_tree_feature
minecraft:overworld_underground_gold_ore_lower_feature
minecraft:meadow_before_surface_wildflowers_feature_rules
minecraft:pale_garden_surface_double_plant_feature_rules
minecraft:mangrove_swamp_surface_tall_grass_feature
minecraft:minecraft:savanna_mutated_surface_tall_grass_feature
minecraft:mangrove_swamp_tall_mangrove_tree_feature
minecraft:meadow_surface_double_plant_feature_rules
minecraft:lush_caves_after_surface_vegetation_feature
minecraft:mega_taiga_surface_tall_grass_feature
minecraft:mega_taiga_after_surface_brown_mushroom_feature_rules
minecraft:plains_surface_tall_grass_feature
minecraft:overworld_underground_diamond_ore_large_feature
minecraft:overworld_surface_flowers_feature
minecraft:overworld_surface_tall_grass_feature
minecraft:taiga_first_double_plant_fern_feature
minecraft:pale_garden_surface_pale_moss_patch_feature_rules
minecraft:pale_garden_surface_tall_grass_feature_rules
minecraft:plains_surface_flowers_feature
minecraft:lush_caves_after_surface_azalea_root_system_feature
minecraft:mangrove_swamp_tall_mangrove_tree_with_beenest_feature
minecraft:swamp_surface_flowers_feature
minecraft:swamp_surface_tall_grass_feature
minecraft:swamp_surface_waterlily_feature
minecraft:taiga_surface_tall_grass_feature
minecraft:eyeblossom_feature_rules
minecraft:mangrove_swamp_mangrove_tree_with_beenest_feature
minecraft:grove_pine_tree_feature
minecraft:overworld_underground_lapis_ore_buried_feature
minecraft:desert_or_swamp_after_surface_fossil_feature
minecraft:taiga_first_sweet_berry_bush_feature
minecraft:crimson_feature
minecraft:crimson_roots_soul_sand_valley_feature
minecraft:deep_warm_ocean_after_surface_seagrass_feature_rules
minecraft:taiga_after_surface_brown_mushroom_feature_rules
minecraft:nether_sprouts_feature_rules
minecraft:taiga_after_surface_sweet_berry_bush_feature_rules
minecraft:roofed_forest_surface_roofed_tree_feature_rules
minecraft:overworld_underground_iron_ore_small_feature
minecraft:mesa_underground_gold_ore_feature
minecraft:overworld_underground_diamond_ore_feature_square
minecraft:overworld_underground_coal_ore_upper_feature
minecraft:overworld_underground_andesite_feature
minecraft:dripstone_caves_underground_copper_ore_feature
minecraft:overworld_underground_iron_ore_upper_feature
minecraft:mountains_underground_coal_ore_feature
minecraft:overworld_underground_gold_ore_feature
minecraft:overworld_underground_diamond_ore_buried_feature
minecraft:overworld_underground_andesite_lower_feature
minecraft:cold_taiga_after_surface_sweet_berry_bush_feature_rules
minecraft:overworld_underground_andesite_upper_feature
minecraft:overworld_underground_gravel_ore_feature
minecraft:overworld_underground_coal_ore_feature
minecraft:overworld_underground_copper_ore_feature
minecraft:overworld_underground_coal_ore_lower_feature
minecraft:overworld_underground_diamond_ore_feature
minecraft:overworld_underground_iron_ore_middle_feature
minecraft:overworld_underground_diorite_feature
minecraft:overworld_underground_diorite_lower_feature
minecraft:overworld_underground_diorite_upper_feature
minecraft:overworld_underground_redstone_ore_lower_feature
minecraft:overworld_underground_dirt_feature
minecraft:overworld_underground_extra_gravel_ore_feature
minecraft:overworld_underground_granite_feature
minecraft:overworld_underground_granite_lower_feature
minecraft:overworld_underground_granite_upper_feature
minecraft:overworld_underground_iron_ore_feature
minecraft:overworld_underground_lapis_ore_feature
minecraft:overworld_underground_redstone_ore_feature
minecraft:overworld_underground_tuff_feature
minecraft:nether_soul_sand_underground_feature_rules
minecraft:bamboo_jungle_before_surface_bamboo_feature_rules
minecraft:cold_taiga_first_sweet_berry_bush_feature
minecraft:mushroom_island_after_surface_brown_mushroom_feature_rules
minecraft:jungle_after_surface_tall_grass_feature_rules
minecraft:plains_first_double_plant_grass_feature
minecraft:plains_first_double_plant_sunflower_feature
minecraft:minecraft:savanna_mutated_after_surface_tall_grass_feature_rules
minecraft:savanna_first_double_plant_grass_feature
minecraft:ocean_after_surface_seagrass_feature_rules
minecraft:flower_forest_after_surface_flowers_feature_rules
minecraft:desert_after_surface_dry_grass_feature_rules
minecraft:mesa_after_surface_dry_grass_feature_rules
minecraft:overworld_after_surface_bush_feature_rules
minecraft:desert_or_swamp_after_surface_fossil_deepslate_feature
minecraft:savanna_after_surface_tall_grass_feature_rules
minecraft:plains_after_surface_double_plant_sunflower_feature_rules
minecraft:bamboo_jungle_after_surface_tall_grass_feature_rules
minecraft:overworld_underwater_magma_feature
minecraft:cherry_grove_after_surface_cherry_tree_feature_rules
minecraft:cherry_grove_pink_petals_feature_rules
minecraft:cold_ocean_after_surface_seagrass_feature_rules
minecraft:deep_cold_ocean_after_surface_seagrass_feature_rules
minecraft:swamp_after_surface_tall_grass_feature_rules
minecraft:swamp_after_surface_flowers_feature_rules
minecraft:meadow_after_surface_flowers_feature_rules
minecraft:forest_after_surface_tall_grass_feature_rules
minecraft:jungle_after_surface_flowers_feature_rules
minecraft:savanna_after_surface_flowers_feature_rules
minecraft:mangrove_swamp_after_surface_seagrass_feature_rules
minecraft:mangrove_swamp_after_surface_tall_grass_feature_rules
minecraft:meadow_after_surface_double_plant_feature_rules
minecraft:overworld_after_surface_extra_brown_mushroom_feature_rules
minecraft:swamp_after_surface_red_mushroom_feature_rules
minecraft:overworld_after_surface_extra_red_mushroom_feature_rules
minecraft:mega_taiga_after_surface_red_mushroom_feature_rules
minecraft:swamp_after_surface_brown_mushroom_feature_rules
minecraft:mega_taiga_after_surface_tall_grass_feature_rules
minecraft:overworld_after_surface_tall_grass_feature_rules
minecraft:mushroom_island_after_surface_red_mushroom_feature_rules
minecraft:overworld_after_surface_flowers_feature_rules
minecraft:plains_after_surface_flowers_feature_rules
minecraft:plains_after_surface_tall_grass_feature_rules
minecraft:river_after_surface_seagrass_feature_rules
minecraft:swamp_after_surface_waterlily_feature_rules
minecraft:taiga_after_surface_red_mushroom_feature_rules
minecraft:taiga_after_surface_tall_grass_feature_rules
minecraft:warm_ocean_after_surface_seagrass_feature_rules
minecraft:lush_caves_after_surface_cave_vines_feature
minecraft:lush_caves_after_surface_leaf_clay_feature
minecraft:lush_caves_after_surface_moss_ceiling_feature
minecraft:lush_caves_after_surface_spore_blossom_feature
minecraft:after_surface_silverfish_feature
minecraft:extreme_hills_after_surface_silverfish_feature
minecraft:jungle_after_surface_vines_feature
minecraft:overworld_amethyst_geode_feature
minecraft:overworld_underground_glow_lichen_feature
minecraft:overworld_underground_deepslate_feature
minecraft:overworld_extra_cave_carver_feature
minecraft:overworld_cave_carver_feature
minecraft:overworld_underwater_cave_carver_feature
```

</details>

#### Static Enum: reload_all (#146)

Value count: 1

<details>
<summary>Show all values</summary>

```
all
```

</details>

#### Static Enum: ReplaceItemBlock (#147)

Value count: 1

<details>
<summary>Show all values</summary>

```
block
```

</details>

#### Static Enum: ReplaceItemEntity (#148)

Value count: 1

<details>
<summary>Show all values</summary>

```
entity
```

</details>

#### Static Enum: ReplaceMode (#149)

Value count: 2

<details>
<summary>Show all values</summary>

```
destroy
keep
```

</details>

#### Static Enum: RideModeStart (#150)

Value count: 1

<details>
<summary>Show all values</summary>

```
start_riding
```

</details>

#### Static Enum: RideModeStop (#151)

Value count: 1

<details>
<summary>Show all values</summary>

```
stop_riding
```

</details>

#### Static Enum: RideModeEvict (#152)

Value count: 1

<details>
<summary>Show all values</summary>

```
evict_riders
```

</details>

#### Static Enum: RideModeSummonRider (#153)

Value count: 1

<details>
<summary>Show all values</summary>

```
summon_rider
```

</details>

#### Static Enum: RideModeSummonRide (#154)

Value count: 1

<details>
<summary>Show all values</summary>

```
summon_ride
```

</details>

#### Static Enum: FillType (#155)

Value count: 2

<details>
<summary>Show all values</summary>

```
until_full
if_group_fits
```

</details>

#### Static Enum: TeleportRules (#156)

Value count: 2

<details>
<summary>Show all values</summary>

```
teleport_rider
teleport_ride
```

</details>

#### Static Enum: RideRules (#157)

Value count: 3

<details>
<summary>Show all values</summary>

```
no_ride_change
reassign_rides
skip_riders
```

</details>

#### Static Enum: ScheduleActionDelay (#158)

Value count: 1

<details>
<summary>Show all values</summary>

```
delay
```

</details>

#### Static Enum: ScheduleActionOnAreaLoaded (#159)

Value count: 1

<details>
<summary>Show all values</summary>

```
on_area_loaded
```

</details>

#### Static Enum: ScheduleActionClear (#160)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: RequestActionAdd (#161)

Value count: 1

<details>
<summary>Show all values</summary>

```
add
```

</details>

#### Static Enum: RequestActionClear (#162)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: DelayMode (#163)

Value count: 2

<details>
<summary>Show all values</summary>

```
replace
append
```

</details>

#### Static Enum: CircleArea (#164)

Value count: 1

<details>
<summary>Show all values</summary>

```
circle
```

</details>

#### Static Enum: TickingArea (#165)

Value count: 1

<details>
<summary>Show all values</summary>

```
tickingarea
```

</details>

#### Static Enum: FunctionName (#166)

Value count: 1

<details>
<summary>Show all values</summary>

```
function
```

</details>

#### Static Enum: TickingAreaName (#167)

Value count: 1

<details>
<summary>Show all values</summary>

```
tickingarea
```

</details>

#### Static Enum: ScoreboardObjectivesCategory (#168)

Value count: 1

<details>
<summary>Show all values</summary>

```
objectives
```

</details>

#### Static Enum: ScoreboardPlayersCategory (#169)

Value count: 1

<details>
<summary>Show all values</summary>

```
players
```

</details>

#### Static Enum: ScoreboardAddAction (#170)

Value count: 1

<details>
<summary>Show all values</summary>

```
add
```

</details>

#### Static Enum: ScoreboardRemoveAction (#171)

Value count: 1

<details>
<summary>Show all values</summary>

```
remove
```

</details>

#### Static Enum: ScoreboardRandomAction (#172)

Value count: 1

<details>
<summary>Show all values</summary>

```
random
```

</details>

#### Static Enum: ScoreboardSetDisplayAction (#173)

Value count: 1

<details>
<summary>Show all values</summary>

```
setdisplay
```

</details>

#### Static Enum: ScoreboardListAction (#174)

Value count: 1

<details>
<summary>Show all values</summary>

```
list
```

</details>

#### Static Enum: ScoreboardResetAction (#175)

Value count: 1

<details>
<summary>Show all values</summary>

```
reset
```

</details>

#### Static Enum: ScoreboardTestAction (#176)

Value count: 1

<details>
<summary>Show all values</summary>

```
test
```

</details>

#### Static Enum: ScoreboardPlayersNumAction (#177)

Value count: 3

<details>
<summary>Show all values</summary>

```
set
add
remove
```

</details>

#### Static Enum: ScoreboardOperationAction (#178)

Value count: 1

<details>
<summary>Show all values</summary>

```
operation
```

</details>

#### Static Enum: ScoreboardSortOrder (#179)

Value count: 2

<details>
<summary>Show all values</summary>

```
ascending
descending
```

</details>

#### Static Enum: ScoreboardDisplaySlotSortable (#180)

Value count: 2

<details>
<summary>Show all values</summary>

```
list
sidebar
```

</details>

#### Static Enum: ScoreboardDisplaySlotNonSortable (#181)

Value count: 1

<details>
<summary>Show all values</summary>

```
belowname
```

</details>

#### Static Enum: ScoreboardCriteria (#182)

Value count: 1

<details>
<summary>Show all values</summary>

```
dummy
```

</details>

#### Static Enum: SetBlockMode (#183)

Value count: 3

<details>
<summary>Show all values</summary>

```
replace
destroy
keep
```

</details>

#### Static Enum: StructureSaveAction (#184)

Value count: 1

<details>
<summary>Show all values</summary>

```
save
```

</details>

#### Static Enum: StructureLoadAction (#185)

Value count: 1

<details>
<summary>Show all values</summary>

```
load
```

</details>

#### Static Enum: StructureDeleteAction (#186)

Value count: 1

<details>
<summary>Show all values</summary>

```
delete
```

</details>

#### Static Enum: StructureSaveMode (#187)

Value count: 2

<details>
<summary>Show all values</summary>

```
disk
memory
```

</details>

#### Static Enum: StructureAnimationMode (#188)

Value count: 2

<details>
<summary>Show all values</summary>

```
block_by_block
layer_by_layer
```

</details>

#### Static Enum: TeleportFacing (#189)

Value count: 1

<details>
<summary>Show all values</summary>

```
facing
```

</details>

#### Static Enum: TagChangeAction (#190)

Value count: 2

<details>
<summary>Show all values</summary>

```
add
remove
```

</details>

#### Static Enum: TagListAction (#191)

Value count: 1

<details>
<summary>Show all values</summary>

```
list
```

</details>

#### Static Enum: TestForBlocksMode (#194)

Value count: 2

<details>
<summary>Show all values</summary>

```
masked
all
```

</details>

#### Static Enum: TickingAreaModeAdd (#195)

Value count: 1

<details>
<summary>Show all values</summary>

```
add
```

</details>

#### Static Enum: TickingAreaModeRemove (#196)

Value count: 1

<details>
<summary>Show all values</summary>

```
remove
```

</details>

#### Static Enum: TickingAreaModeRemoveAll (#197)

Value count: 1

<details>
<summary>Show all values</summary>

```
remove_all
```

</details>

#### Static Enum: TickingAreaModeList (#198)

Value count: 1

<details>
<summary>Show all values</summary>

```
list
```

</details>

#### Static Enum: TickingAreaModePreload (#199)

Value count: 1

<details>
<summary>Show all values</summary>

```
preload
```

</details>

#### Static Enum: AddTickingAreaType (#200)

Value count: 1

<details>
<summary>Show all values</summary>

```
circle
```

</details>

#### Static Enum: AllDimensions (#201)

Value count: 1

<details>
<summary>Show all values</summary>

```
all-dimensions
```

</details>

#### Static Enum: TimeModeSet (#202)

Value count: 1

<details>
<summary>Show all values</summary>

```
set
```

</details>

#### Static Enum: TimeModeAdd (#203)

Value count: 1

<details>
<summary>Show all values</summary>

```
add
```

</details>

#### Static Enum: TimeModeQuery (#204)

Value count: 1

<details>
<summary>Show all values</summary>

```
query
```

</details>

#### Static Enum: TimeQuery (#205)

Value count: 3

<details>
<summary>Show all values</summary>

```
daytime
gametime
day
```

</details>

#### Static Enum: TimeSpec (#206)

Value count: 6

<details>
<summary>Show all values</summary>

```
day
sunrise
noon
sunset
night
midnight
```

</details>

#### Static Enum: TitleClear (#207)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: TitleReset (#208)

Value count: 1

<details>
<summary>Show all values</summary>

```
reset
```

</details>

#### Static Enum: TitleSet (#209)

Value count: 3

<details>
<summary>Show all values</summary>

```
title
subtitle
actionbar
```

</details>

#### Static Enum: TitleTimes (#210)

Value count: 1

<details>
<summary>Show all values</summary>

```
times
```

</details>

#### Static Enum: TitleRawClear (#211)

Value count: 1

<details>
<summary>Show all values</summary>

```
clear
```

</details>

#### Static Enum: TitleRawReset (#212)

Value count: 1

<details>
<summary>Show all values</summary>

```
reset
```

</details>

#### Static Enum: TitleRawSet (#213)

Value count: 3

<details>
<summary>Show all values</summary>

```
title
subtitle
actionbar
```

</details>

#### Static Enum: TitleRawTimes (#214)

Value count: 1

<details>
<summary>Show all values</summary>

```
times
```

</details>

#### Static Enum: WeatherType (#215)

Value count: 3

<details>
<summary>Show all values</summary>

```
clear
rain
thunder
```

</details>

#### Static Enum: WeatherQuery (#216)

Value count: 1

<details>
<summary>Show all values</summary>

```
query
```

</details>

#### Static Enum: Take (#218)

Value count: 1

<details>
<summary>Show all values</summary>

```
take
```

</details>

#### Static Enum: Give (#219)

Value count: 1

<details>
<summary>Show all values</summary>

```
give
```

</details>

#### Static Enum: Ability (#220)

Value count: 3

<details>
<summary>Show all values</summary>

```
mayfly
mute
worldbuilder
```

</details>

#### Static Enum: SaveMode (#243)

Value count: 3

<details>
<summary>Show all values</summary>

```
query
hold
resume
```

</details>

#### Static Enum: AllowListAction (#244)

Value count: 6

<details>
<summary>Show all values</summary>

```
add
remove
list
reload
on
off
```

</details>

#### Static Enum: BoolSettingName (#246)

Value count: 1

<details>
<summary>Show all values</summary>

```
allow-cheats
```

</details>

#### Static Enum: DifficultySettingName (#247)

Value count: 1

<details>
<summary>Show all values</summary>

```
difficulty
```

</details>

#### Static Enum: RedirectLocation (#248)

Value count: 2

<details>
<summary>Show all values</summary>

```
marketplace
character
```

</details>

#### Static Enum: 3PServerOfferList (#249)

Value count: 1

<details>
<summary>Show all values</summary>

```
server
```

</details>

### Dynamic Enums Used by Commands

#### Dynamic Enum: ScoreboardObjectives (#0)

Value count now: 0

<details>
<summary>Show values</summary>

```
(runtime-provided or currently empty)
```

</details>

#### Dynamic Enum: TagValues (#1)

Value count now: 0

<details>
<summary>Show values</summary>

```
(runtime-provided or currently empty)
```

</details>

#### Dynamic Enum: UnlockableRecipeValues (#2)

Value count now: 2757

<details>
<summary>Show values</summary>

```
*
minecraft:copper_spear
minecraft:diamond_spear
minecraft:golden_spear
minecraft:iron_spear
minecraft:stone_spear
minecraft:wooden_spear
minecraft:acacia_shelf_from_stripped_acacia_log
minecraft:bamboo_shelf_from_stripped_bamboo_block
minecraft:birch_shelf_from_stripped_birch_log
minecraft:cherry_shelf_from_stripped_cherry_log
minecraft:copper_axe
minecraft:copper_bars
minecraft:copper_boots
minecraft:copper_chain
minecraft:copper_chest
minecraft:copper_chestplate
minecraft:copper_helmet
minecraft:copper_hoe
minecraft:copper_ingot_from_nuggets
minecraft:copper_lantern
minecraft:copper_leggings
minecraft:copper_nugget
minecraft:copper_pickaxe
minecraft:copper_shovel
minecraft:copper_sword
minecraft:copper_torch
minecraft:copper_trapdoor
minecraft:crimson_shelf_from_stripped_crimson_stem
minecraft:dark_oak_shelf_from_stripped_dark_oak_log
minecraft:jungle_shelf_from_stripped_jungle_log
minecraft:mangrove_shelf_from_stripped_mangrove_log
minecraft:oak_shelf_from_stripped_oak_log
minecraft:pale_oak_shelf_from_stripped_pale_oak_log
minecraft:spruce_shelf_from_stripped_spruce_log
minecraft:warped_shelf_from_stripped_warped_stem
minecraft:waxing_copper_bars
minecraft:waxing_copper_chain
minecraft:waxing_copper_chest
minecraft:waxing_copper_golem_statue
minecraft:waxing_copper_lantern
minecraft:waxing_exposed_copper_bars
minecraft:waxing_exposed_copper_chain
minecraft:waxing_exposed_copper_chest
minecraft:waxing_exposed_copper_golem_statue
minecraft:waxing_exposed_copper_lantern
minecraft:waxing_exposed_lightning_rod
minecraft:waxing_lightning_rod
minecraft:waxing_oxidized_copper_bars
minecraft:waxing_oxidized_copper_chain
minecraft:waxing_oxidized_copper_chest
minecraft:waxing_oxidized_copper_golem_statue
minecraft:waxing_oxidized_copper_lantern
minecraft:waxing_oxidized_lightning_rod
minecraft:waxing_weathered_copper_bars
minecraft:waxing_weathered_copper_chain
minecraft:waxing_weathered_copper_chest
minecraft:waxing_weathered_copper_golem_statue
minecraft:waxing_weathered_copper_lantern
minecraft:waxing_weathered_lightning_rod
minecraft:dried_ghast
minecraft:lead
minecraft:saddle
minecraft:stonecutter_cut_red_sandstone_slab
minecraft:stonecutter_cut_sandstone_slab
minecraft:cake
minecraft:lodestone
minecraft:pink_dye_from_cactus_flower
minecraft:pumpkin_pie
minecraft:yellow_dye_from_wildflowers
minecraft:chiseled_resin_bricks_from_slabs
minecraft:creaking_heart
minecraft:gray_dye_from_closed_eyeblossom
minecraft:orange_dye_from_open_eyeblossom
minecraft:pale_moss_carpet
minecraft:pale_oak_boat
minecraft:pale_oak_button
minecraft:pale_oak_chest_boat
minecraft:pale_oak_door
minecraft:pale_oak_fence
minecraft:pale_oak_fence_gate
minecraft:pale_oak_hanging_sign
minecraft:pale_oak_planks_from_log
minecraft:pale_oak_planks_from_stripped_log
minecraft:pale_oak_planks_from_stripped_wood
minecraft:pale_oak_planks_from_wood
minecraft:pale_oak_pressure_plate
minecraft:pale_oak_sign
minecraft:pale_oak_slab
minecraft:pale_oak_stairs
minecraft:pale_oak_wood_from_stripped_log
minecraft:pale_oak_trapdoor
minecraft:pale_oak_wood_from_log
minecraft:purpur_slab
minecraft:red_sandstone_stairs_from_chiseled
minecraft:red_sandstone_stairs_from_cut
minecraft:resin_block
minecraft:resin_bricks
minecraft:resin_brick_slab
minecraft:resin_brick_stairs
minecraft:resin_brick_wall
minecraft:resin_clump_from_resin_block
minecraft:sandstone_stairs_from_chiseled
minecraft:sandstone_stairs_from_cut
minecraft:stonecutter_resin_brick_chiseled
minecraft:stonecutter_resin_brick_slab
minecraft:stonecutter_resin_brick_stairs
minecraft:stonecutter_resin_brick_wall
minecraft:stonecutter_stonebrick_chiseled2
minecraft:stonecutter_stonebrick_slab2
minecraft:stonecutter_stonebrick_stairs2
minecraft:stonecutter_stonebrick_wall2
minecraft:acacia_boat
minecraft:acacia_door
minecraft:acacia_fence
minecraft:acacia_fence_gate
minecraft:acacia_planks
minecraft:acacia_planks_from_stripped
minecraft:acacia_stairs
minecraft:acacia_wooden_slab
minecraft:andesite
minecraft:andesite_stairs
minecraft:birch_boat
minecraft:birch_door
minecraft:birch_fence
minecraft:birch_fence_gate
minecraft:birch_planks
minecraft:birch_planks_from_stripped
minecraft:birch_stairs
minecraft:birch_wooden_slab
minecraft:black_banner
minecraft:black_carpet
minecraft:black_carpet_from_white
minecraft:black_concrete_powder
minecraft:black_concrete_powder_from_ink_sac
minecraft:black_stained_glass
minecraft:black_stained_glass_from_ink_sac
minecraft:black_stained_glass_pane_from_pane
minecraft:black_stained_hardened_clay
minecraft:black_stained_hardened_clay_from_ink_sac
minecraft:blue_banner
minecraft:blue_carpet
minecraft:blue_carpet_from_white
minecraft:blue_concrete_powder
minecraft:blue_concrete_powder_from_lapis_lazuli
minecraft:blue_stained_glass
minecraft:blue_stained_glass_from_lapis_lazuli
minecraft:blue_stained_glass_pane_from_pane
minecraft:blue_stained_hardened_clay
minecraft:blue_stained_hardened_clay_from_lapis_lazuli
minecraft:boat
minecraft:brown_banner
minecraft:brown_carpet
minecraft:brown_carpet_from_white
minecraft:brown_concrete_powder
minecraft:brown_concrete_powder_from_cocoa_beans
minecraft:brown_stained_glass
minecraft:brown_stained_glass_from_cocoa_beans
minecraft:brown_stained_glass_pane_from_pane
minecraft:brown_stained_hardened_clay
minecraft:brown_stained_hardened_clay_from_cocoa_beans
minecraft:bundle
minecraft:cyan_banner
minecraft:cyan_carpet
minecraft:cyan_carpet_from_white
minecraft:cyan_concrete_powder
minecraft:cyan_stained_glass
minecraft:cyan_stained_glass_pane_from_pane
minecraft:cyan_stained_hardened_clay
minecraft:dark_oak_boat
minecraft:dark_oak_door
minecraft:dark_oak_fence
minecraft:dark_oak_fence_gate
minecraft:dark_oak_planks
minecraft:dark_oak_planks_from_stripped
minecraft:dark_oak_stairs
minecraft:dark_oak_wooden_slab
minecraft:dark_prismarine
minecraft:dark_prismarine_from_ink_sac
minecraft:diorite
minecraft:diorite_stairs
minecraft:fence
minecraft:fence_gate
minecraft:granite
minecraft:granite_stairs
minecraft:gray_banner
minecraft:gray_carpet
minecraft:gray_carpet_from_white
minecraft:gray_concrete_powder
minecraft:gray_stained_glass
minecraft:gray_stained_glass_pane_from_pane
minecraft:gray_stained_hardened_clay
minecraft:green_banner
minecraft:green_carpet
minecraft:green_carpet_from_white
minecraft:green_concrete_powder
minecraft:green_stained_glass
minecraft:green_stained_glass_pane_from_pane
minecraft:green_stained_hardened_clay
minecraft:jungle_boat
minecraft:jungle_door
minecraft:jungle_fence
minecraft:jungle_fence_gate
minecraft:jungle_planks
minecraft:jungle_planks_from_stripped
minecraft:jungle_stairs
minecraft:jungle_wooden_slab
minecraft:light_blue_banner
minecraft:light_blue_carpet
minecraft:light_blue_carpet_from_white
minecraft:light_blue_concrete_powder
minecraft:light_blue_stained_glass
minecraft:light_blue_stained_glass_pane_from_pane
minecraft:light_blue_stained_hardened_clay
minecraft:light_gray_banner
minecraft:light_gray_carpet
minecraft:light_gray__carpet_from_white
minecraft:light_gray_concrete_powder
minecraft:light_gray_stained_glass
minecraft:light_gray_stained_glass_pane_from_pane
minecraft:light_gray_stained_hardened_clay
minecraft:lime_banner
minecraft:lime_carpet
minecraft:lime__carpet_from_white
minecraft:lime_concrete_powder
minecraft:lime_stained_glass
minecraft:lime_stained_glass_pane_from_pane
minecraft:lime_stained_hardened_clay
minecraft:magenta_banner
minecraft:magenta_carpet
minecraft:magenta_carpet_from_white
minecraft:magenta_concrete_powder
minecraft:magenta_dye_from_lilac
minecraft:magenta_stained_glass
minecraft:magenta_stained_glass_pane_from_pane
minecraft:magenta_stained_hardened_clay
minecraft:oak_fence
minecraft:oak_planks
minecraft:oak_planks_from_stripped
minecraft:oak_stairs
minecraft:oak_wooden_slab
minecraft:orange_banner
minecraft:orange_carpet
minecraft:orange_carpet_from_white
minecraft:orange_concrete_powder
minecraft:orange_stained_glass
minecraft:orange_stained_glass_pane_from_pane
minecraft:orange_stained_hardened_clay
minecraft:painting
minecraft:pink_banner
minecraft:pink_carpet
minecraft:pink_carpet_from_white
minecraft:pink_concrete_powder
minecraft:pink_dye_from_peony
minecraft:pink_stained_glass
minecraft:pink_stained_glass_pane_from_pane
minecraft:pink_stained_hardened_clay
minecraft:polished_andesite
minecraft:polished_andesite_stairs
minecraft:polished_diorite
minecraft:polished_diorite_stairs
minecraft:polished_granite
minecraft:polished_granite_stairs
minecraft:prismarine_bricks
minecraft:prismarine_stairs_bricks
minecraft:prismarine_stairs_dark
minecraft:purple_banner
minecraft:purple_carpet
minecraft:purple_carpet_from_white
minecraft:purple_concrete_powder
minecraft:purple_stained_glass
minecraft:purple_stained_glass_pane_from_pane
minecraft:purple_stained_hardened_clay
minecraft:red_banner
minecraft:red_carpet
minecraft:red_carpet_from_white
minecraft:red_concrete_powder
minecraft:red_dye_from_rose_bush
minecraft:red_stained_glass
minecraft:red_stained_glass_pane_from_pane
minecraft:red_stained_hardened_clay
minecraft:sign_acacia
minecraft:sign_birch
minecraft:sign_darkoak
minecraft:sign_jungle
minecraft:sign_oak
minecraft:sign_spruce
minecraft:spruce_boat
minecraft:spruce_door
minecraft:spruce_fence
minecraft:spruce_fence_gate
minecraft:spruce_planks
minecraft:spruce_planks_from_stripped
minecraft:spruce_stairs
minecraft:spruce_wooden_slab
minecraft:stonecutter_andesite_stairs
minecraft:stonecutter_dark_prismarine_slab
minecraft:stonecutter_dark_prismarine_stairs
minecraft:stonecutter_diorite_stairs
minecraft:stonecutter_granite_stairs
minecraft:stonecutter_mossy_cobbledouble_stone_slab
minecraft:stonecutter_polished_andesite
minecraft:stonecutter_polished_andesite_stairs
minecraft:stonecutter_polished_andesite_stairs2
minecraft:stonecutter_polished_diorite
minecraft:stonecutter_polished_diorite_stairs
minecraft:stonecutter_polished_diorite_stairs2
minecraft:stonecutter_polished_granite
minecraft:stonecutter_polished_granite_stairs
minecraft:stonecutter_polished_granite_stairs2
minecraft:stonecutter_prismarine_brick_slab
minecraft:stonecutter_prismarine_brick_stairs
minecraft:stonecutter_prismarine_slab
minecraft:stonecutter_purpur_lines
minecraft:stonecutter_purpur_slab
minecraft:stonecutter_red_nether_brick_slab
minecraft:stonecutter_smooth_sanddouble_stone_slab
minecraft:string_to_wool
minecraft:white_banner
minecraft:white_carpet
minecraft:white_concrete_powder
minecraft:white_concrete_powder_from_bonemeal
minecraft:white_stained_glass
minecraft:white_stained_glass_from_bonemeal
minecraft:white_stained_glass_pane_from_pane
minecraft:white_stained_hardened_clay
minecraft:white_stained_hardened_clay_from_bonemeal
minecraft:wooden_door
minecraft:yellow_banner
minecraft:yellow_carpet
minecraft:yellow_carpet_from_white
minecraft:yellow_concrete_powder
minecraft:yellow_dye_from_sunflower
minecraft:yellow_stained_glass
minecraft:yellow_stained_glass_pane_from_pane
minecraft:yellow_stained_hardened_clay
minecraft:andesite_wall
minecraft:brick_wall
minecraft:cobblestone_wall
minecraft:cyan_dye_from_pitcher_plant
minecraft:diorite_wall
minecraft:end_brick_wall
minecraft:granite_wall
minecraft:mossy_cobblestone_wall
minecraft:mossy_stone_brick_wall
minecraft:nether_brick_wall
minecraft:prismarine_wall
minecraft:red_nether_brick_wall
minecraft:red_sandstone_wall
minecraft:sandstone_wall
minecraft:stonecutter_andesite_wall
minecraft:stonecutter_brick_wall
minecraft:stonecutter_cobblestone_wall
minecraft:stonecutter_diorite_wall
minecraft:stonecutter_endbrick_wall
minecraft:stonecutter_endbrick_wall2
minecraft:stonecutter_granite_wall
minecraft:stonecutter_mossy_cobblestone_wall
minecraft:stonecutter_mossy_stonebrick_wall
minecraft:stonecutter_nether_brick_wall
minecraft:stonecutter_prismarine_wall
minecraft:stonecutter_red_nether_brick_wall
minecraft:stonecutter_red_sandstone_wall
minecraft:stonecutter_sandstone_wall
minecraft:stonecutter_stonebrick_wall
minecraft:stone_brick_wall
minecraft:coarse_dirt
minecraft:quartz_block
minecraft:quartz_bricks
minecraft:pillar_quartz_block
minecraft:red_sandstone
minecraft:sandstone
minecraft:smooth_quartz_stairs
minecraft:smooth_red_sandstone
minecraft:smooth_red_sandstone_stairs
minecraft:smooth_sandstone
minecraft:smooth_sandstone_stairs
minecraft:stonecutter_quartz_chiseled
minecraft:stonecutter_quartz_lines
minecraft:stonecutter_red_sandstone_cut
minecraft:stonecutter_red_sandstone_heiroglyphs
minecraft:stonecutter_red_sanddouble_stone_slab
minecraft:stonecutter_sandstone_cut
minecraft:stonecutter_sandstone_heiroglyphs
minecraft:stonecutter_smooth_quartz_slab
minecraft:stonecutter_smooth_quartz_stairs
minecraft:stonecutter_smooth_red_sanddouble_stone_slab
minecraft:stonecutter_smooth_red_sandstone_stairs
minecraft:stonecutter_waxed_oxidized_cut_copper_to_cut_copper_slab
minecraft:yellow_dye_from_dandelion
minecraft:grindstone
minecraft:mossy_stonebrick
minecraft:mossy_stonebrick_from_moss
minecraft:mossy_stone_brick_stairs
minecraft:stonebrick
minecraft:stonecutter_andesite_slab
minecraft:stonecutter_diorite_slab
minecraft:stonecutter_endbrick_slab
minecraft:stonecutter_endbrick_slab2
minecraft:stonecutter_granite_slab
minecraft:stonecutter_mossy_stonebrick_slab
minecraft:stonecutter_mossy_stonebrick_stairs
minecraft:stonecutter_polished_andesite_slab
minecraft:stonecutter_polished_andesite_slab2
minecraft:stonecutter_polished_diorite_slab
minecraft:stonecutter_polished_diorite_slab2
minecraft:stonecutter_polished_granite_slab
minecraft:stonecutter_polished_granite_slab2
minecraft:stonecutter_stonebrick
minecraft:stonecutter_stonebrick_chiseled
minecraft:stonecutter_double_stone_slab
minecraft:stone_brick_stairs
minecraft:armor_stand
minecraft:bolt_armor_trim_smithing_template_duplicate
minecraft:bolt_armor_trim_smithing_template_duplicate_waxed
minecraft:chiseled_nether_bricks
minecraft:chiseled_tuff
minecraft:chiseled_tuff_bricks
minecraft:crafter
minecraft:crafting_table_chiseled_copper
minecraft:copper_bulb
minecraft:copper_door
minecraft:copper_grate
minecraft:exposed_chiseled_copper
minecraft:exposed_copper_bulb
minecraft:exposed_copper_grate
minecraft:oxidized_chiseled_copper
minecraft:oxidized_copper_bulb
minecraft:oxidized_copper_grate
minecraft:waxed_chiseled_copper
minecraft:waxed_copper_bulb
minecraft:crafting_table_waxed_copper_door
minecraft:waxed_copper_grate
minecraft:waxed_exposed_chiseled_copper
minecraft:waxed_exposed_copper_bulb
minecraft:waxed_exposed_copper_grate
minecraft:waxed_oxidized_chiseled_copper
minecraft:waxed_oxidized_copper_bulb
minecraft:waxed_oxidized_copper_grate
minecraft:waxed_weathered_chiseled_copper
minecraft:waxed_weathered_copper_bulb
minecraft:waxed_weathered_copper_grate
minecraft:weathered_chiseled_copper
minecraft:weathered_copper_bulb
minecraft:weathered_copper_grate
minecraft:flow_armor_trim_smithing_template_duplicate
minecraft:mace
minecraft:polished_tuff
minecraft:polished_tuff_slab
minecraft:polished_tuff_stairs
minecraft:polished_tuff_wall
minecraft:stonecutter_brick_slab
minecraft:stonecutter_cobbledouble_stone_slab
minecraft:stonecutter_copper_block_to_chiseled_copper
minecraft:stonecutter_copper_block_to_copper_grate
minecraft:stonecutter_cut_copper_to_chiseled_copper
minecraft:stonecutter_exposed_copper_to_exposed_chiseled_copper
minecraft:stonecutter_exposed_copper_to_exposed_copper_grate
minecraft:stonecutter_exposed_cut_copper_to_exposed_chiseled_copper
minecraft:stonecutter_nether_brick_slab
minecraft:stonecutter_oxidized_copper_to_oxidized_chiseled_copper
minecraft:stonecutter_oxidized_copper_to_oxidized_copper_grate
minecraft:stonecutter_oxidized_cut_copper_to_oxidized_chiseled_copper
minecraft:stonecutter_polished_tuff_to_chiseled_tuff_bricks
minecraft:stonecutter_polished_tuff_to_polished_tuff_slab
minecraft:stonecutter_polished_tuff_to_polished_tuff_stairs
minecraft:stonecutter_polished_tuff_to_polished_tuff_wall
minecraft:stonecutter_polished_tuff_to_tuff_bricks
minecraft:stonecutter_polished_tuff_to_tuff_brick_slab
minecraft:stonecutter_polished_tuff_to_tuff_brick_stairs
minecraft:stonecutter_polished_tuff_to_tuff_brick_wall
minecraft:stonecutter_quartz_slab
minecraft:stonecutter_sanddouble_stone_slab
minecraft:stonecutter_smooth_double_stone_slab
minecraft:stonecutter_stonebrick_slab
minecraft:stonecutter_tuff_bricks_to_chiseled_tuff_bricks
minecraft:stonecutter_tuff_bricks_to_tuff_brick_slab
minecraft:stonecutter_tuff_bricks_to_tuff_brick_stairs
minecraft:stonecutter_tuff_bricks_to_tuff_brick_wall
minecraft:stonecutter_tuff_to_chiseled_tuff
minecraft:stonecutter_tuff_to_chiseled_tuff_bricks
minecraft:stonecutter_tuff_to_polished_tuff
minecraft:stonecutter_tuff_to_polished_tuff_slab
minecraft:stonecutter_tuff_to_polished_tuff_stairs
minecraft:stonecutter_tuff_to_polished_tuff_wall
minecraft:stonecutter_tuff_to_tuff_bricks
minecraft:stonecutter_tuff_to_tuff_brick_slab
minecraft:stonecutter_tuff_to_tuff_brick_stairs
minecraft:stonecutter_tuff_to_tuff_brick_wall
minecraft:stonecutter_tuff_to_tuff_slab
minecraft:stonecutter_tuff_to_tuff_stairs
minecraft:stonecutter_tuff_to_tuff_wall
minecraft:stonecutter_waxed_cut_copper_to_waxed_chiseled_copper
minecraft:stonecutter_waxed_exposed_cut_copper_to_waxed_exposed_chiseled_copper
minecraft:stonecutter_waxed_oxidized_cut_copper_to_waxed_oxidized_chiseled_copper
minecraft:stonecutter_waxed_weathered_cut_copper_to_waxed_weathered_chiseled_copper
minecraft:stonecutter_weathered_copper_to_weathered_chiseled_copper
minecraft:stonecutter_weathered_copper_to_weathered_copper_grate
minecraft:stonecutter_weathered_cut_copper_to_weathered_chiseled_copper
minecraft:stonecutter_waxed_copper_to_waxed_chiseled_copper
minecraft:stonecutter_waxed_copper_to_waxed_copper_grate
minecraft:stonecutter_waxed_exposed_copper_to_waxed_exposed_chiseled_copper
minecraft:stonecutter_waxed_exposed_copper_to_waxed_exposed_copper_grate
minecraft:stonecutter_waxed_oxidized_copper_to_waxed_oxidized_chiseled_copper
minecraft:stonecutter_waxed_oxidized_copper_to_waxed_oxidized_copper_grate
minecraft:stonecutter_waxed_weathered_copper_to_waxed_weathered_chiseled_copper
minecraft:stonecutter_waxed_weathered_copper_to_waxed_weathered_copper_grate
minecraft:tuff_bricks
minecraft:tuff_brick_slab
minecraft:tuff_brick_stairs
minecraft:tuff_brick_wall
minecraft:tuff_slab
minecraft:tuff_stairs
minecraft:tuff_wall
minecraft:waxing_chiseled_copper
minecraft:waxing_copper_bulb
minecraft:waxing_copper_door
minecraft:waxing_copper_grate
minecraft:waxing_copper_trapdoor
minecraft:waxed_exposed_chiseled_copper_from_honeycomb
minecraft:waxing_exposed_copper_bulb
minecraft:waxing_exposed_copper_door
minecraft:waxing_exposed_copper_grate
minecraft:waxing_exposed_copper_trapdoor
minecraft:waxed_oxidized_chiseled_copper_from_honeycomb
minecraft:waxing_oxidized_copper_bulb
minecraft:waxing_oxidized_copper_door
minecraft:waxing_oxidized_copper_grate
minecraft:waxing_oxidized_copper_trapdoor
minecraft:waxed_weathered_chiseled_copper_from_honeycomb
minecraft:waxing_weathered_copper_bulb
minecraft:waxing_weathered_copper_door
minecraft:waxing_weathered_copper_grate
minecraft:waxing_weathered_copper_trapdoor
minecraft:wind_charge
minecraft:banner_pattern_flower
minecraft:blue_dye_from_cornflower
minecraft:WorkBench_recipeId_from_oak
minecraft:light_blue_dye_from_blue_orchid
minecraft:light_gray_dye_from_azure_bluet
minecraft:light_gray_dye_from_oxeye_daisy
minecraft:light_gray_dye_from_white_tulip
minecraft:magenta_dye_from_allium
minecraft:orange_dye_from_orange_tulip
minecraft:pink_dye_from_pink_tulip
minecraft:red_dye_from_poppy
minecraft:red_dye_from_tulip
minecraft:white_dye_from_lily_of_the_valley
minecraft:wolf_armor
minecraft:acacia_planks_from_stripped_wood
minecraft:acacia_planks_from_wood
minecraft:acacia_wood
minecraft:acacia_wood_stripped
minecraft:birch_planks_from_stripped_wood
minecraft:birch_planks_from_wood
minecraft:birch_wood
minecraft:birch_wood_stripped
minecraft:dark_oak_planks_from_stripped_wood
minecraft:dark_oak_planks_from_wood
minecraft:dark_oak_wood
minecraft:dark_oak_wood_stripped
minecraft:jungle_planks_from_stripped_wood
minecraft:jungle_planks_from_wood
minecraft:jungle_wood
minecraft:jungle_wood_stripped
minecraft:oak_planks_from_stripped_wood
minecraft:oak_planks_from_wood
minecraft:oak_wood
minecraft:oak_wood_stripped
minecraft:spruce_planks_from_stripped_wood
minecraft:spruce_planks_from_wood
minecraft:spruce_wood
minecraft:spruce_wood_stripped
minecraft:black_stained_glass_pane
minecraft:blue_stained_glass_pane
minecraft:brown_stained_glass_pane
minecraft:cyan_stained_glass_pane
minecraft:gray_stained_glass_pane
minecraft:green_stained_glass_pane
minecraft:light_blue_stained_glass_pane
minecraft:light_gray_stained_glass_pane
minecraft:lime_stained_glass_pane
minecraft:magenta_stained_glass_pane
minecraft:orange_stained_glass_pane
minecraft:pink_stained_glass_pane
minecraft:purple_stained_glass_pane
minecraft:red_stained_glass_pane
minecraft:white_stained_glass_pane
minecraft:yellow_stained_glass_pane
minecraft:acacia_chest_boat
minecraft:acacia_hanging_sign
minecraft:activator_rail
minecraft:amethyst_block
minecraft:anvil
minecraft:arrow
minecraft:bamboo_block
minecraft:bamboo_button
minecraft:bamboo_chest_raft
minecraft:bamboo_door
minecraft:bamboo_fence
minecraft:bamboo_fence_gate
minecraft:bamboo_hanging_sign
minecraft:bamboo_mosaic
minecraft:bamboo_mosaic_slab
minecraft:bamboo_mosaic_stairs
minecraft:bamboo_planks
minecraft:bamboo_planks_from_stripped
minecraft:bamboo_pressure_plate
minecraft:bamboo_raft
minecraft:bamboo_sign
minecraft:bamboo_slab
minecraft:bamboo_stairs
minecraft:bamboo_trapdoor
minecraft:banner_pattern_bricks
minecraft:banner_pattern_creeper
minecraft:banner_pattern_skull
minecraft:banner_pattern_thing
minecraft:banner_pattern_vines
minecraft:barrel_with_planks
minecraft:basic_map_to_enhanced
minecraft:beacon
minecraft:beehive
minecraft:beetroot_soup
minecraft:birch_chest_boat
minecraft:birch_hanging_sign
minecraft:blackstone_slab
minecraft:blackstone_stairs
minecraft:blackstone_wall
minecraft:black_candle
minecraft:black_candle_from_ink_sac
minecraft:black_dye_from_ink_sac
minecraft:black_dye_from_wither_rose
minecraft:blast_furnace
minecraft:blaze_powder
minecraft:blue_candle
minecraft:blue_candle_from_lapis_lazuli
minecraft:blue_dye_from_lapis_lazuli
minecraft:blue_ice
minecraft:bone_block
minecraft:bone_meal_from_block
minecraft:bone_meal_from_bone
minecraft:book
minecraft:Bookshelf_woodplanks_recipeId
minecraft:bow
minecraft:Bowl_recipeId
minecraft:bread
minecraft:brewing_stand
minecraft:brick_block
minecraft:brick_stairs
minecraft:brown_candle
minecraft:brown_candle_from_cocoa_beans
minecraft:brown_dye_from_cocoa_beans
minecraft:brush
minecraft:bucket
minecraft:calibrated_sculk_sensor
minecraft:campfire
minecraft:candle
minecraft:carrot_on_a_stick
minecraft:cartography_table
minecraft:cartography_table_locator_map
minecraft:cartography_table_map
minecraft:cauldron
minecraft:chain
minecraft:cherry_boat
minecraft:cherry_button
minecraft:cherry_chest_boat
minecraft:cherry_door
minecraft:cherry_fence
minecraft:cherry_fence_gate
minecraft:cherry_hanging_sign
minecraft:cherry_planks_from_log
minecraft:cherry_planks_from_stripped_log
minecraft:cherry_planks_from_stripped_wood
minecraft:cherry_planks_from_wood
minecraft:cherry_pressure_plate
minecraft:cherry_sign
minecraft:cherry_slab
minecraft:cherry_stairs
minecraft:cherry_wood_from_stripped_log
minecraft:cherry_trapdoor
minecraft:cherry_wood_from_log
minecraft:Chest_recipeId
minecraft:chest_boat
minecraft:chest_minecart
minecraft:chiseled_bookshelf
minecraft:chiseled_deepslate
minecraft:chiseled_deepslate_from_cobbled_deepslate_stonecutting
minecraft:chiseled_polished_blackstone
minecraft:clay
minecraft:clock
minecraft:coal
minecraft:coal_block
minecraft:coast_armor_trim_smithing_template_duplicate
minecraft:cobbled_deepslate_slab
minecraft:cobbled_deepslate_slab_from_cobbled_deepslate_stonecutting
minecraft:cobbled_deepslate_stairs
minecraft:cobbled_deepslate_stairs_from_cobbled_deepslate_stonecutting
minecraft:cobbled_deepslate_wall
minecraft:cobbled_deepslate_wall_from_cobbled_deepslate_stonecutting
minecraft:cobblestone_stairs
minecraft:comparator
minecraft:compass
minecraft:composter
minecraft:conduit
minecraft:cookie
minecraft:copper_block_from_ingots
minecraft:WorkBench_recipeId
minecraft:crafting_table_cut_copper
minecraft:crafting_table_cut_copper_slab
minecraft:crafting_table_cut_copper_stairs
minecraft:crafting_table_exposed_cut_copper
minecraft:crafting_table_exposed_cut_copper_slab
minecraft:crafting_table_exposed_cut_copper_stairs
minecraft:crafting_table_oxidized_cut_copper
minecraft:crafting_table_oxidized_cut_copper_slab
minecraft:crafting_table_oxidized_cut_copper_stairs
minecraft:crafting_table_waxed_cut_copper
minecraft:crafting_table_waxed_cut_copper_slab
minecraft:crafting_table_waxed_cut_copper_stairs
minecraft:crafting_table_waxed_exposed_cut_copper
minecraft:crafting_table_waxed_exposed_cut_copper_slab
minecraft:crafting_table_waxed_exposed_cut_copper_stairs
minecraft:crafting_table_waxed_oxidized_cut_copper
minecraft:crafting_table_waxed_oxidized_cut_copper_slab
minecraft:crafting_table_waxed_oxidized_cut_copper_stairs
minecraft:crafting_table_waxed_weathered_cut_copper
minecraft:crafting_table_waxed_weathered_cut_copper_slab
minecraft:crafting_table_waxed_weathered_cut_copper_stairs
minecraft:crafting_table_weathered_cut_copper
minecraft:crafting_table_weathered_cut_copper_slab
minecraft:crafting_table_weathered_cut_copper_stairs
minecraft:crimson_button
minecraft:crimson_door
minecraft:crimson_fence
minecraft:crimson_fence_gate
minecraft:crimson_hanging_sign
minecraft:crimson_hyphae
minecraft:stripped_crimson_hyphae
minecraft:crimson_planks
minecraft:crimson_planks_from_crimson_hyphae
minecraft:crimson_planks_from_stripped_crimson_hyphae
minecraft:crimson_planks_from_stripped_log
minecraft:crimson_pressure_plate
minecraft:crimson_sign
minecraft:crimson_slab
minecraft:crimson_stairs
minecraft:crimson_trapdoor
minecraft:crossbow
minecraft:cyan_candle
minecraft:cyan_dye
minecraft:cyan_dye_from_lapis_lazuli
minecraft:dark_oak_chest_boat
minecraft:dark_oak_hanging_sign
minecraft:DaylightDetector_recipeId
minecraft:deepslate_bricks
minecraft:deepslate_bricks_from_cobbled_deepslate_stonecutting
minecraft:deepslate_bricks_from_polished_deepslate_stonecutting
minecraft:deepslate_brick_slab
minecraft:deepslate_brick_slab_from_cobbled_deepslate_stonecutting
minecraft:deepslate_brick_slab_from_deepslate_bricks_stonecutting
minecraft:deepslate_brick_slab_from_polished_deepslate_stonecutting
minecraft:deepslate_brick_stairs
minecraft:deepslate_brick_stairs_from_cobbled_deepslate_stonecutting
minecraft:deepslate_brick_stairs_from_deepslate_bricks_stonecutting
minecraft:deepslate_brick_stairs_from_polished_deepslate_stonecut
minecraft:deepslate_brick_wall
minecraft:deepslate_brick_wall_from_cobbled_deepslate_stonecutting
minecraft:deepslate_brick_wall_from_deepslate_bricks_stonecutting
minecraft:deepslate_brick_wall_from_polished_deepslate_stonecutting
minecraft:deepslate_tiles
minecraft:deepslate_tiles_from_cobbled_deepslate_stonecutting
minecraft:deepslate_tiles_from_deepslate_bricks_stonecutting
minecraft:deepslate_tiles_from_polished_deepslate_stonecutting
minecraft:deepslate_tile_slab
minecraft:deepslate_tile_slab_from_cobbled_deepslate_stonecutting
minecraft:deepslate_tile_slab_from_deepslate_bricks_stonecutting
minecraft:deepslate_tile_slab_from_deepslate_tiles_stonecutting
minecraft:deepslate_tile_slab_from_polished_deepslate_stonecutting
minecraft:deepslate_tile_stairs
minecraft:deepslate_tile_stairs_from_cobbled_deepslate_stonecutting
minecraft:deepslate_tile_stairs_from_deepslate_bricks_stonecutting
minecraft:deepslate_tile_stairs_from_deepslate_tiles_stonecutting
minecraft:deepslate_tile_stairs_from_polished_deepslate_stonecutting
minecraft:deepslate_tile_wall
minecraft:deepslate_tile_wall_from_cobbled_deepslate_stonecutting
minecraft:deepslate_tile_wall_from_deepslate_bricks_stonecutting
minecraft:deepslate_tile_wall_from_deepslate_tiles_stonecutting
minecraft:deepslate_tile_wall_from_polished_deepslate_stonecutting
minecraft:detector_rail
minecraft:diamond
minecraft:diamond_axe
minecraft:diamond_block
minecraft:diamond_boots
minecraft:diamond_chestplate
minecraft:diamond_helmet
minecraft:diamond_hoe
minecraft:diamond_leggings
minecraft:diamond_pickaxe
minecraft:diamond_shovel
minecraft:diamond_sword
minecraft:dispenser
minecraft:dried_kelp
minecraft:dried_kelp_block
minecraft:dripstone_block
minecraft:dropper
minecraft:dune_armor_trim_smithing_template_duplicate
minecraft:emerald
minecraft:emerald_block
minecraft:empty_map_to_enhanced
minecraft:enchanting_table
minecraft:ender_chest
minecraft:ender_eye
minecraft:end_bricks
minecraft:end_brick_stairs
minecraft:end_crystal
minecraft:end_rod
minecraft:eye_armor_trim_smithing_template_duplicate
minecraft:fermented_spider_eye
minecraft:FireCharge_coal_sulphur_recipeId
minecraft:fishing_rod
minecraft:fletching_table
minecraft:flint_and_steel
minecraft:flower_pot
minecraft:furnace
minecraft:furnace_from_blackstone
minecraft:furnace_from_cobbled_deepslate
minecraft:glass_bottle
minecraft:glass_pane
minecraft:glowstone
minecraft:glow_frame
minecraft:golden_apple
minecraft:golden_axe
minecraft:golden_boots
minecraft:golden_carrot
minecraft:golden_chestplate
minecraft:golden_helmet
minecraft:golden_hoe
minecraft:golden_leggings
minecraft:golden_pickaxe
minecraft:golden_rail
minecraft:golden_shovel
minecraft:golden_sword
minecraft:gold_block
minecraft:gold_ingot_from_block
minecraft:gold_ingot_from_nuggets
minecraft:gold_nugget
minecraft:gray_candle
minecraft:gray_dye
minecraft:gray_dye_from_black_bonemeal
minecraft:gray_dye_from_ink_bonemeal
minecraft:gray_dye_from_ink_white
minecraft:green_candle
minecraft:hay_block
minecraft:heavy_weighted_pressure_plate
minecraft:honeycomb_block
minecraft:honey_block
minecraft:honey_bottle
minecraft:honey_bottle_to_sugar
minecraft:hopper
minecraft:hopper_minecart
minecraft:host_armor_trim_smithing_template_duplicate
minecraft:ingots_from_copper
minecraft:ingots_from_waxed_copper
minecraft:iron_axe
minecraft:iron_bars
minecraft:iron_block
minecraft:iron_boots
minecraft:iron_chestplate
minecraft:iron_door
minecraft:iron_helmet
minecraft:iron_hoe
minecraft:iron_ingot_from_block
minecraft:iron_ingot_from_nuggets
minecraft:iron_leggings
minecraft:iron_nugget
minecraft:iron_pickaxe
minecraft:iron_shovel
minecraft:iron_sword
minecraft:iron_trapdoor
minecraft:item_frame
minecraft:Jukebox_recipeId
minecraft:jungle_chest_boat
minecraft:jungle_hanging_sign
minecraft:ladder
minecraft:lantern
minecraft:lapis_block
minecraft:lapis_lazuli
minecraft:leather
minecraft:leather_boots
minecraft:leather_chestplate
minecraft:leather_helmet
minecraft:leather_horse_armor
minecraft:leather_leggings
minecraft:lectern
minecraft:lever
minecraft:lightning_rod
minecraft:light_blue_candle
minecraft:light_blue_dye
minecraft:light_blue_dye_from_blue_bonemeal
minecraft:light_blue_dye_from_lapis_bonemeal
minecraft:light_blue_dye_from_lapis_white
minecraft:light_gray_candle
minecraft:light_gray_dye
minecraft:light_gray_dye_from_black_bonemeal
minecraft:light_gray_dye_from_gray_bonemeal
minecraft:light_gray_dye_from_gray_white
minecraft:light_gray_dye_from_ink_bonemeal
minecraft:light_gray_dye_from_ink_white
minecraft:light_weighted_pressure_plate
minecraft:lime_candle
minecraft:lime_dye
minecraft:lime_dye_from_bonemeal
minecraft:lit_pumpkin
minecraft:locator_map
minecraft:loom
minecraft:magenta_candle
minecraft:magenta_dye
minecraft:magenta_dye_from_blue_ink_bonemeal
minecraft:magenta_dye_from_blue_ink_white
minecraft:magenta_dye_from_lapis_ink_bonemeal
minecraft:magenta_dye_from_lapis_ink_white
minecraft:magenta_dye_from_lapis_red_pink
minecraft:magenta_dye_from_purple_and_pink
minecraft:magma
minecraft:magma_cream
minecraft:mangrove_boat
minecraft:mangrove_button
minecraft:mangrove_chest_boat
minecraft:mangrove_door
minecraft:mangrove_fence
minecraft:mangrove_fence_gate
minecraft:mangrove_hanging_sign
minecraft:mangrove_planks
minecraft:mangrove_planks_from_stripped_log
minecraft:mangrove_planks_from_stripped_wood
minecraft:mangrove_planks_from_wood
minecraft:mangrove_pressure_plate
minecraft:mangrove_sign
minecraft:mangrove_slab
minecraft:mangrove_stairs
minecraft:mangrove_trapdoor
minecraft:mangrove_wood
minecraft:mangrove_wood_stripped
minecraft:map
minecraft:melon_block
minecraft:melon_seeds
minecraft:minecart
minecraft:mossy_cobblestone
minecraft:mossy_cobblestone_from_moss
minecraft:mossy_cobblestone_stairs
minecraft:moss_carpet
minecraft:muddy_mangrove_roots
minecraft:mud_bricks
minecraft:mud_brick_slab
minecraft:mud_brick_stairs
minecraft:mud_brick_wall
minecraft:mushroom_stew
minecraft:netherite_block
minecraft:netherite_ingot
minecraft:netherite_ingot_from_block
minecraft:netherite_upgrade_smithing_template_duplicate
minecraft:nether_brick
minecraft:nether_brick_fence
minecraft:nether_brick_stairs
minecraft:nether_wart_block
minecraft:noteblock
minecraft:oak_hanging_sign
minecraft:observer
minecraft:orange_candle
minecraft:orange_dye_from_red_yellow
minecraft:orange_dye_from_torchflower
minecraft:packed_ice
minecraft:packed_mud
minecraft:paper
minecraft:pink_candle
minecraft:pink_dye
minecraft:pink_dye_from_pink_petals
minecraft:pink_dye_from_red_bonemeal
minecraft:piston
minecraft:polished_basalt
minecraft:polished_blackstone
minecraft:polished_blackstone_bricks
minecraft:polished_blackstone_brick_slab
minecraft:polished_blackstone_brick_stairs
minecraft:polished_blackstone_brick_wall
minecraft:polished_blackstone_button
minecraft:polished_blackstone_pressure_plate
minecraft:polished_blackstone_slab
minecraft:polished_blackstone_stairs
minecraft:polished_blackstone_wall
minecraft:polished_deepslate
minecraft:polished_deepslate_from_cobbled_deepslate_stonecutting
minecraft:polished_deepslate_slab
minecraft:polished_deepslate_slab_from_cobbled_deepslate_stonecut
minecraft:polished_deepslate_slab_from_polished_deepslate_stonecutting
minecraft:polished_deepslate_stairs
minecraft:polished_deepslate_stairs_from_cobbled_deepslate_stonecutting
minecraft:polished_deepslate_stairs_from_polished_deepslate_stonecutting
minecraft:polished_deepslate_wall
minecraft:polished_deepslate_wall_from_cobbled_deepslate_stonecut
minecraft:polished_deepslate_wall_from_polished_deepslate_stonecut
minecraft:prismarine
minecraft:prismarine_stairs
minecraft:pumpkin_seeds
minecraft:purple_candle
minecraft:purple_dye
minecraft:purple_dye_from_lapis_lazuli
minecraft:purpur_block
minecraft:purpur_stairs
minecraft:quartz_stairs
minecraft:rabbit_stew_from_brown_mushroom
minecraft:rabbit_stew_from_red_mushroom
minecraft:rail
minecraft:raiser_armor_trim_smithing_template_duplicate
minecraft:raw_copper
minecraft:raw_copper_block
minecraft:raw_gold
minecraft:raw_gold_block
minecraft:raw_iron
minecraft:raw_iron_block
minecraft:record_5
minecraft:recovery_compass
minecraft:recovery_compass_from_lodestone_compass
minecraft:redstone
minecraft:redstone_block
minecraft:redstone_lamp
minecraft:redstone_torch
minecraft:red_candle
minecraft:red_dye_from_beetroot
minecraft:red_nether_brick
minecraft:red_nether_brick_stairs
minecraft:red_sandstone_stairs
minecraft:repeater
minecraft:respawn_anchor
minecraft:rib_armor_trim_smithing_template_duplicate
minecraft:sandstone_stairs
minecraft:scaffolding
minecraft:sealantern
minecraft:sentry_armor_trim_smithing_template_duplicate
minecraft:shaper_armor_trim_smithing_template_duplicate
minecraft:shears
minecraft:shield
minecraft:shulker_box
minecraft:silence_armor_trim_smithing_template_duplicate
minecraft:slime
minecraft:slime_ball
minecraft:smithing_table
minecraft:smoker
minecraft:snout_armor_trim_smithing_template_duplicate
minecraft:snow
minecraft:snow_layer
minecraft:soul_campfire
minecraft:soul_lantern
minecraft:soul_torch
minecraft:speckled_melon
minecraft:spire_armor_trim_smithing_template_duplicate
minecraft:spruce_chest_boat
minecraft:spruce_hanging_sign
minecraft:spyglass
minecraft:stick
minecraft:sticky_piston
minecraft:stonecutter
minecraft:stonecutter_blackstone_slab_from_blackstone
minecraft:stonecutter_blackstone_stairs_from_blackstone
minecraft:stonecutter_blackstone_wall_from_blackstone
minecraft:stonecutter_bricks_from_polished_blackstone
minecraft:stonecutter_brick_slab_from_polished_blackstone
minecraft:stonecutter_brick_stairs
minecraft:stonecutter_brick_stairs_from_polished_blackstone
minecraft:stonecutter_brick_wall_from_polished_blackstone
minecraft:stonecutter_chiseled_from_polished_blackstone
minecraft:stonecutter_chiseled_nether_bricks_from_nether_brick
minecraft:stonecutter_chiseled_polished_from_blackstone
minecraft:stonecutter_cobblestone_stairs
minecraft:stonecutter_copper_block_to_cut_copper
minecraft:stonecutter_copper_block_to_cut_copper_slab
minecraft:stonecutter_copper_block_to_cut_copper_stairs
minecraft:stonecutter_cut_copper_to_cut_copper_slab
minecraft:stonecutter_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_endbricks
minecraft:stonecutter_endbrick_stairs
minecraft:stonecutter_endbrick_stairs2
minecraft:stonecutter_exposed_copper_to_cut_copper
minecraft:stonecutter_exposed_copper_to_exposed_cut_copper_slab
minecraft:stonecutter_exposed_copper_to_cut_copper_stairs
minecraft:stonecutter_exposed_cut_copper_to_cut_copper_slab
minecraft:stonecutter_exposed_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_mossy_cobblestone_stairs
minecraft:stonecutter_mud_brick_slab
minecraft:stonecutter_mud_brick_stairs
minecraft:stonecutter_mud_brick_wall
minecraft:stonecutter_nether_brick_stairs
minecraft:stonecutter_oxidized_copper_to_cut_copper
minecraft:stonecutter_oxidized_copper_to_cut_copper_slab
minecraft:stonecutter_oxidized_copper_to_cut_copper_stairs
minecraft:stonecutter_oxidized_cut_copper_to_cut_copper_slab
minecraft:stonecutter_oxidized_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_polished_basalt_from_basalt
minecraft:stonecutter_polished_bricks_from_blackstone
minecraft:stonecutter_polished_brick_slab_from_blackstone
minecraft:stonecutter_polished_brick_stairs_from_blackstone
minecraft:stonecutter_polished_brick_wall_from_blackstone
minecraft:stonecutter_polished_from_blackstone
minecraft:stonecutter_polished_slab_from_blackstone
minecraft:stonecutter_polished_stairs_from_blackstone
minecraft:stonecutter_polished_wall_from_blackstone
minecraft:stonecutter_prismarine_stairs
minecraft:stonecutter_purpur_stairs
minecraft:stonecutter_quartz_bricks_from_quartz_block
minecraft:stonecutter_quartz_stairs
minecraft:stonecutter_red_nether_brick_stairs
minecraft:stonecutter_red_sandstone_stairs
minecraft:stonecutter_sandstone_stairs
minecraft:stonecutter_slab_from_polished_blackstone
minecraft:stonecutter_slab_from_polished_blackstone_bricks
minecraft:stonecutter_smooth_sandstone_stairs
minecraft:stonecutter_stairs_from_polished_blackstone
stonecutter_stairs_from_polished_blackstone_bricks
minecraft:stonecutter_stonebrick_stairs
minecraft:stonecutter_stone_stairs
minecraft:stonecutter_wall_from_polished_blackstone
minecraft:stonecutter_wall_from_polished_blackstone_bricks
minecraft:stonecutter_weathered_copper_to_cut_copper
minecraft:stonecutter_weathered_copper_to_cut_copper_slab
minecraft:stonecutter_weathered_copper_to_cut_copper_stairs
minecraft:stonecutter_weathered_cut_copper_to_cut_copper_slab
minecraft:stonecutter_weathered_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_copper_to_cut_copper
minecraft:stonecutter_waxed_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_cut_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_exposed_copper_to_cut_copper
minecraft:stonecutter_waxed_copper_to_exposed_cut_copper_slab
minecraft:stonecutter_waxed_exposed_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_exposed_cut_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_exposed_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_oxidized_copper_to_cut_copper
minecraft:stonecutter_waxed_oxidized_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_oxidized_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_oxidized_cut_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_weathered_copper_to_cut_copper
minecraft:stonecutter_waxed_weathered_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_weathered_copper_to_cut_copper_stairs
minecraft:stonecutter_waxed_weathered_cut_copper_to_cut_copper_slab
minecraft:stonecutter_waxed_weathered_cut_copper_to_cut_copper_stairs
minecraft:stone_axe
minecraft:stone_button
minecraft:stone_hoe
minecraft:stone_pickaxe
minecraft:stone_pressure_plate
minecraft:stone_shovel
minecraft:stone_stairs
minecraft:stone_sword
minecraft:stripped_mangrove_wood
minecraft:sugar
minecraft:target
minecraft:tide_armor_trim_smithing_template_duplicate
minecraft:tinted_glass
minecraft:tnt
minecraft:tnt_minecart
minecraft:torch
minecraft:trapped_chest
minecraft:tripwire_hook
minecraft:turtle_helmet
minecraft:vex_armor_trim_smithing_template_duplicate
minecraft:ward_armor_trim_smithing_template_duplicate
minecraft:warped_button
minecraft:warped_door
minecraft:warped_fence
minecraft:warped_fence_gate
minecraft:warped_fungus_on_a_stick
minecraft:warped_hanging_sign
minecraft:warped_hyphae
minecraft:stripped_warped_hyphae
minecraft:warped_planks
minecraft:warped_planks_from_stripped_log
minecraft:warped_planks_from_stripped_warped_hyphae
minecraft:warped_planks_from_warped_hyphae
minecraft:warped_pressure_plate
minecraft:warped_sign
minecraft:warped_slab
minecraft:warped_stairs
minecraft:warped_trapdoor
minecraft:waxing_copper_block
minecraft:waxing_cut_copper
minecraft:waxing_cut_copper_slab
minecraft:waxing_cut_copper_stairs
minecraft:waxing_exposed_copper
minecraft:waxing_exposed_cut_copper
minecraft:waxing_exposed_cut_copper_slab
minecraft:waxing_exposed_cut_copper_stairs
minecraft:waxing_oxidized_copper
minecraft:waxing_oxidized_cut_copper
minecraft:waxing_oxidized_cut_copper_slab
minecraft:waxing_oxidized_cut_copper_stairs
minecraft:waxing_weathered_copper
minecraft:waxing_weathered_cut_copper
minecraft:waxing_weathered_cut_copper_slab
minecraft:waxing_weathered_cut_copper_stairs
minecraft:wayfinder_armor_trim_smithing_template_duplicate
minecraft:wheat
minecraft:white_candle
minecraft:white_candle_from_bonemeal
minecraft:white_dye_from_bone_meal
minecraft:wild_armor_trim_smithing_template_duplicate
minecraft:wooden_axe
minecraft:wooden_hoe
minecraft:wooden_pickaxe
minecraft:wooden_shovel
minecraft:wooden_sword
minecraft:writable_book
minecraft:yellow_candle
wool_dye_wool_19_14
wool_dye_wool_19_13
wool_dye_wool_19_12
wool_dye_wool_19_11
wool_dye_wool_19_10
wool_dye_wool_19_9
wool_dye_wool_19_8
wool_dye_wool_19_7
wool_dye_wool_19_6
wool_dye_wool_19_5
wool_dye_wool_19_4
wool_dye_wool_19_3
wool_dye_wool_19_2
wool_dye_wool_19_1
wool_dye_wool_19_0
wool_dye_wool_18_15
wool_dye_wool_18_14
wool_dye_wool_18_13
wool_dye_wool_18_12
wool_dye_wool_18_11
wool_dye_wool_18_10
wool_dye_wool_18_9
wool_dye_wool_18_8
wool_dye_wool_18_7
wool_dye_wool_18_6
wool_dye_wool_18_5
wool_dye_wool_18_3
wool_dye_wool_18_2
wool_dye_wool_18_1
wool_dye_wool_18_0
wool_dye_wool_17_15
wool_dye_wool_17_14
wool_dye_wool_17_13
wool_dye_wool_17_12
wool_dye_wool_17_11
wool_dye_wool_17_10
wool_dye_wool_17_9
wool_dye_wool_17_8
wool_dye_wool_17_7
wool_dye_wool_17_6
wool_dye_wool_17_5
wool_dye_wool_17_4
wool_dye_wool_17_2
wool_dye_wool_17_1
wool_dye_wool_17_0
wool_dye_wool_16_15
wool_dye_wool_16_14
wool_dye_wool_16_13
wool_dye_wool_16_12
wool_dye_wool_16_11
wool_dye_wool_16_10
wool_dye_wool_16_9
wool_dye_wool_16_8
wool_dye_wool_16_7
wool_dye_wool_16_6
wool_dye_wool_16_5
wool_dye_wool_16_4
wool_dye_wool_16_3
wool_dye_wool_16_2
wool_dye_wool_16_1
wool_dye_wool_15_14
wool_dye_wool_15_13
wool_dye_wool_15_12
wool_dye_wool_15_11
wool_dye_wool_15_10
wool_dye_wool_15_9
wool_dye_wool_15_8
wool_dye_wool_15_7
wool_dye_wool_15_6
wool_dye_wool_15_5
wool_dye_wool_15_4
wool_dye_wool_15_3
wool_dye_wool_15_2
wool_dye_wool_15_1
wool_dye_wool_15_0
wool_dye_wool_14_15
wool_dye_wool_14_13
wool_dye_wool_14_12
wool_dye_wool_14_11
wool_dye_wool_14_10
wool_dye_wool_14_9
wool_dye_wool_14_8
wool_dye_wool_14_7
wool_dye_wool_14_6
wool_dye_wool_14_5
wool_dye_wool_14_4
wool_dye_wool_14_3
wool_dye_wool_14_2
wool_dye_wool_14_1
wool_dye_wool_14_0
wool_dye_wool_13_15
wool_dye_wool_13_14
wool_dye_wool_13_12
wool_dye_wool_13_11
wool_dye_wool_13_10
wool_dye_wool_13_9
wool_dye_wool_13_8
wool_dye_wool_13_7
wool_dye_wool_13_6
wool_dye_wool_13_5
wool_dye_wool_13_4
wool_dye_wool_13_3
wool_dye_wool_13_2
wool_dye_wool_13_1
wool_dye_wool_13_0
wool_dye_wool_12_15
wool_dye_wool_12_14
wool_dye_wool_12_13
wool_dye_wool_12_11
wool_dye_wool_12_10
wool_dye_wool_12_9
wool_dye_wool_12_8
wool_dye_wool_12_7
wool_dye_wool_12_6
wool_dye_wool_12_5
wool_dye_wool_12_4
wool_dye_wool_12_3
wool_dye_wool_12_2
wool_dye_wool_12_1
wool_dye_wool_12_0
wool_dye_wool_11_15
wool_dye_wool_11_14
wool_dye_wool_11_13
wool_dye_wool_11_12
wool_dye_wool_11_10
wool_dye_wool_11_9
wool_dye_wool_11_8
wool_dye_wool_11_7
wool_dye_wool_11_6
wool_dye_wool_11_5
wool_dye_wool_11_4
wool_dye_wool_11_3
wool_dye_wool_11_2
wool_dye_wool_11_1
wool_dye_wool_11_0
wool_dye_wool_10_15
wool_dye_wool_10_14
wool_dye_wool_10_13
wool_dye_wool_10_12
wool_dye_wool_10_11
wool_dye_wool_10_9
wool_dye_wool_10_8
wool_dye_wool_10_7
wool_dye_wool_10_6
wool_dye_wool_10_5
wool_dye_wool_10_4
wool_dye_wool_10_3
wool_dye_wool_10_2
wool_dye_wool_10_1
wool_dye_wool_10_0
wool_dye_wool_9_15
wool_dye_wool_9_14
wool_dye_wool_9_13
wool_dye_wool_9_12
wool_dye_wool_9_11
wool_dye_wool_9_10
wool_dye_wool_9_8
wool_dye_wool_9_7
wool_dye_wool_9_6
wool_dye_wool_9_5
wool_dye_wool_9_4
wool_dye_wool_9_3
wool_dye_wool_9_2
wool_dye_wool_9_1
wool_dye_wool_9_0
wool_dye_wool_8_15
wool_dye_wool_8_14
wool_dye_wool_8_13
wool_dye_wool_8_12
wool_dye_wool_8_11
wool_dye_wool_8_10
wool_dye_wool_8_9
wool_dye_wool_8_7
wool_dye_wool_8_6
wool_dye_wool_8_5
wool_dye_wool_8_4
wool_dye_wool_8_3
wool_dye_wool_8_2
wool_dye_wool_8_1
wool_dye_wool_8_0
wool_dye_wool_7_15
wool_dye_wool_7_14
wool_dye_wool_7_13
wool_dye_wool_7_12
wool_dye_wool_7_11
wool_dye_wool_7_10
wool_dye_wool_7_9
wool_dye_wool_7_8
wool_dye_wool_7_6
wool_dye_wool_7_5
wool_dye_wool_7_4
wool_dye_wool_7_3
wool_dye_wool_7_2
wool_dye_wool_7_1
wool_dye_wool_7_0
wool_dye_wool_6_15
wool_dye_wool_6_14
wool_dye_wool_6_13
wool_dye_wool_6_12
wool_dye_wool_6_11
wool_dye_wool_6_10
wool_dye_wool_6_9
wool_dye_wool_6_8
wool_dye_wool_6_7
wool_dye_wool_6_5
wool_dye_wool_6_4
wool_dye_wool_6_3
wool_dye_wool_6_2
wool_dye_wool_6_1
wool_dye_wool_6_0
wool_dye_wool_5_15
wool_dye_wool_5_14
wool_dye_wool_5_13
wool_dye_wool_5_12
wool_dye_wool_5_11
wool_dye_wool_5_10
wool_dye_wool_5_9
wool_dye_wool_5_8
wool_dye_wool_5_7
wool_dye_wool_5_6
wool_dye_wool_5_4
wool_dye_wool_5_3
wool_dye_wool_5_2
wool_dye_wool_5_1
wool_dye_wool_5_0
wool_dye_wool_4_15
wool_dye_wool_4_14
wool_dye_wool_4_13
wool_dye_wool_4_12
wool_dye_wool_4_11
wool_dye_wool_4_10
wool_dye_wool_4_9
wool_dye_wool_4_8
wool_dye_wool_4_7
wool_dye_wool_4_6
wool_dye_wool_4_5
wool_dye_wool_4_3
wool_dye_wool_4_2
wool_dye_wool_4_1
wool_dye_wool_4_0
wool_dye_wool_3_15
wool_dye_wool_3_14
wool_dye_wool_3_13
wool_dye_wool_3_12
wool_dye_wool_3_11
wool_dye_wool_3_10
wool_dye_wool_3_9
wool_dye_wool_3_8
wool_dye_wool_3_7
wool_dye_wool_3_6
wool_dye_wool_3_5
wool_dye_wool_3_4
wool_dye_wool_3_2
wool_dye_wool_3_1
wool_dye_wool_3_0
wool_dye_wool_2_15
wool_dye_wool_2_14
wool_dye_wool_2_13
wool_dye_wool_2_12
wool_dye_wool_2_11
wool_dye_wool_2_10
wool_dye_wool_2_9
wool_dye_wool_2_8
wool_dye_wool_2_7
wool_dye_wool_2_6
wool_dye_wool_2_5
wool_dye_wool_2_4
wool_dye_wool_2_3
wool_dye_wool_2_1
wool_dye_wool_2_0
wool_dye_wool_1_15
wool_dye_wool_1_14
wool_dye_wool_1_13
wool_dye_wool_1_12
wool_dye_wool_1_11
wool_dye_wool_1_10
wool_dye_wool_1_9
wool_dye_wool_1_8
wool_dye_wool_1_7
wool_dye_wool_1_6
wool_dye_wool_1_5
wool_dye_wool_1_4
wool_dye_wool_1_3
wool_dye_wool_1_2
wool_dye_wool_1_0
wool_dye_wool_0_15
wool_dye_wool_0_14
wool_dye_wool_0_13
wool_dye_wool_0_12
wool_dye_wool_0_11
wool_dye_wool_0_10
wool_dye_wool_0_9
wool_dye_wool_0_8
wool_dye_wool_0_7
wool_dye_wool_0_6
wool_dye_wool_0_5
wool_dye_wool_0_4
wool_dye_wool_0_3
wool_dye_wool_0_2
wool_dye_wool_0_1
shulkerBox_shulker_box_color_dye_19_0
shulkerBox_shulker_box_color_block_19_14_0
shulkerBox_shulker_box_color_block_19_13_0
shulkerBox_shulker_box_color_block_19_12_0
shulkerBox_shulker_box_color_block_19_11_0
shulkerBox_shulker_box_color_block_19_10_0
shulkerBox_shulker_box_color_block_19_9_0
shulkerBox_shulker_box_color_block_19_8_0
shulkerBox_shulker_box_color_block_19_7_0
shulkerBox_shulker_box_color_block_19_6_0
shulkerBox_shulker_box_color_block_19_5_0
shulkerBox_shulker_box_color_block_19_4_0
shulkerBox_shulker_box_color_block_19_3_0
shulkerBox_shulker_box_color_block_19_2_0
shulkerBox_shulker_box_color_block_19_1_0
shulkerBox_shulker_box_color_block_19_0_0
shulkerBox_shulker_box_color_dye_18_0
shulkerBox_shulker_box_color_block_18_15_0
shulkerBox_shulker_box_color_block_18_14_0
shulkerBox_shulker_box_color_block_18_13_0
shulkerBox_shulker_box_color_block_18_12_0
shulkerBox_shulker_box_color_block_18_11_0
shulkerBox_shulker_box_color_block_18_10_0
shulkerBox_shulker_box_color_block_18_9_0
shulkerBox_shulker_box_color_block_18_8_0
shulkerBox_shulker_box_color_block_18_7_0
shulkerBox_shulker_box_color_block_18_6_0
shulkerBox_shulker_box_color_block_18_5_0
shulkerBox_shulker_box_color_block_18_3_0
shulkerBox_shulker_box_color_block_18_2_0
shulkerBox_shulker_box_color_block_18_1_0
shulkerBox_shulker_box_color_block_18_0_0
shulkerBox_shulker_box_color_dye_17_0
shulkerBox_shulker_box_color_block_17_15_0
shulkerBox_shulker_box_color_block_17_14_0
shulkerBox_shulker_box_color_block_17_13_0
shulkerBox_shulker_box_color_block_17_12_0
shulkerBox_shulker_box_color_block_17_11_0
shulkerBox_shulker_box_color_block_17_10_0
shulkerBox_shulker_box_color_block_17_9_0
shulkerBox_shulker_box_color_block_17_8_0
shulkerBox_shulker_box_color_block_17_7_0
shulkerBox_shulker_box_color_block_17_6_0
shulkerBox_shulker_box_color_block_17_5_0
shulkerBox_shulker_box_color_block_17_4_0
shulkerBox_shulker_box_color_block_17_2_0
shulkerBox_shulker_box_color_block_17_1_0
shulkerBox_shulker_box_color_block_17_0_0
shulkerBox_shulker_box_color_dye_16_0
shulkerBox_shulker_box_color_block_16_15_0
shulkerBox_shulker_box_color_block_16_14_0
shulkerBox_shulker_box_color_block_16_13_0
shulkerBox_shulker_box_color_block_16_12_0
shulkerBox_shulker_box_color_block_16_11_0
shulkerBox_shulker_box_color_block_16_10_0
shulkerBox_shulker_box_color_block_16_9_0
shulkerBox_shulker_box_color_block_16_8_0
shulkerBox_shulker_box_color_block_16_7_0
shulkerBox_shulker_box_color_block_16_6_0
shulkerBox_shulker_box_color_block_16_5_0
shulkerBox_shulker_box_color_block_16_4_0
shulkerBox_shulker_box_color_block_16_3_0
shulkerBox_shulker_box_color_block_16_2_0
shulkerBox_shulker_box_color_block_16_1_0
shulkerBox_shulker_box_color_dye_15_0
shulkerBox_shulker_box_color_block_15_14_0
shulkerBox_shulker_box_color_block_15_13_0
shulkerBox_shulker_box_color_block_15_12_0
shulkerBox_shulker_box_color_block_15_11_0
shulkerBox_shulker_box_color_block_15_10_0
shulkerBox_shulker_box_color_block_15_9_0
shulkerBox_shulker_box_color_block_15_8_0
shulkerBox_shulker_box_color_block_15_7_0
shulkerBox_shulker_box_color_block_15_6_0
shulkerBox_shulker_box_color_block_15_5_0
shulkerBox_shulker_box_color_block_15_4_0
shulkerBox_shulker_box_color_block_15_3_0
shulkerBox_shulker_box_color_block_15_2_0
shulkerBox_shulker_box_color_block_15_1_0
shulkerBox_shulker_box_color_block_15_0_0
shulkerBox_shulker_box_color_dye_14_0
shulkerBox_shulker_box_color_block_14_15_0
shulkerBox_shulker_box_color_block_14_13_0
shulkerBox_shulker_box_color_block_14_12_0
shulkerBox_shulker_box_color_block_14_11_0
shulkerBox_shulker_box_color_block_14_10_0
shulkerBox_shulker_box_color_block_14_9_0
shulkerBox_shulker_box_color_block_14_8_0
shulkerBox_shulker_box_color_block_14_7_0
shulkerBox_shulker_box_color_block_14_6_0
shulkerBox_shulker_box_color_block_14_5_0
shulkerBox_shulker_box_color_block_14_4_0
shulkerBox_shulker_box_color_block_14_3_0
shulkerBox_shulker_box_color_block_14_2_0
shulkerBox_shulker_box_color_block_14_1_0
shulkerBox_shulker_box_color_block_14_0_0
shulkerBox_shulker_box_color_dye_13_0
shulkerBox_shulker_box_color_block_13_15_0
shulkerBox_shulker_box_color_block_13_14_0
shulkerBox_shulker_box_color_block_13_12_0
shulkerBox_shulker_box_color_block_13_11_0
shulkerBox_shulker_box_color_block_13_10_0
shulkerBox_shulker_box_color_block_13_9_0
shulkerBox_shulker_box_color_block_13_8_0
shulkerBox_shulker_box_color_block_13_7_0
shulkerBox_shulker_box_color_block_13_6_0
shulkerBox_shulker_box_color_block_13_5_0
shulkerBox_shulker_box_color_block_13_4_0
shulkerBox_shulker_box_color_block_13_3_0
shulkerBox_shulker_box_color_block_13_2_0
shulkerBox_shulker_box_color_block_13_1_0
shulkerBox_shulker_box_color_block_13_0_0
shulkerBox_shulker_box_color_dye_12_0
shulkerBox_shulker_box_color_block_12_15_0
shulkerBox_shulker_box_color_block_12_14_0
shulkerBox_shulker_box_color_block_12_13_0
shulkerBox_shulker_box_color_block_12_11_0
shulkerBox_shulker_box_color_block_12_10_0
shulkerBox_shulker_box_color_block_12_9_0
shulkerBox_shulker_box_color_block_12_8_0
shulkerBox_shulker_box_color_block_12_7_0
shulkerBox_shulker_box_color_block_12_6_0
shulkerBox_shulker_box_color_block_12_5_0
shulkerBox_shulker_box_color_block_12_4_0
shulkerBox_shulker_box_color_block_12_3_0
shulkerBox_shulker_box_color_block_12_2_0
shulkerBox_shulker_box_color_block_12_1_0
shulkerBox_shulker_box_color_block_12_0_0
shulkerBox_shulker_box_color_dye_11_0
shulkerBox_shulker_box_color_block_11_15_0
shulkerBox_shulker_box_color_block_11_14_0
shulkerBox_shulker_box_color_block_11_13_0
shulkerBox_shulker_box_color_block_11_12_0
shulkerBox_shulker_box_color_block_11_10_0
shulkerBox_shulker_box_color_block_11_9_0
shulkerBox_shulker_box_color_block_11_8_0
shulkerBox_shulker_box_color_block_11_7_0
shulkerBox_shulker_box_color_block_11_6_0
shulkerBox_shulker_box_color_block_11_5_0
shulkerBox_shulker_box_color_block_11_4_0
shulkerBox_shulker_box_color_block_11_3_0
shulkerBox_shulker_box_color_block_11_2_0
shulkerBox_shulker_box_color_block_11_1_0
shulkerBox_shulker_box_color_block_11_0_0
shulkerBox_shulker_box_color_dye_10_0
shulkerBox_shulker_box_color_block_10_15_0
shulkerBox_shulker_box_color_block_10_14_0
shulkerBox_shulker_box_color_block_10_13_0
shulkerBox_shulker_box_color_block_10_12_0
shulkerBox_shulker_box_color_block_10_11_0
shulkerBox_shulker_box_color_block_10_9_0
shulkerBox_shulker_box_color_block_10_8_0
shulkerBox_shulker_box_color_block_10_7_0
shulkerBox_shulker_box_color_block_10_6_0
shulkerBox_shulker_box_color_block_10_5_0
shulkerBox_shulker_box_color_block_10_4_0
shulkerBox_shulker_box_color_block_10_3_0
shulkerBox_shulker_box_color_block_10_2_0
shulkerBox_shulker_box_color_block_10_1_0
shulkerBox_shulker_box_color_block_10_0_0
shulkerBox_shulker_box_color_dye_9_0
shulkerBox_shulker_box_color_block_9_15_0
shulkerBox_shulker_box_color_block_9_14_0
shulkerBox_shulker_box_color_block_9_13_0
shulkerBox_shulker_box_color_block_9_12_0
shulkerBox_shulker_box_color_block_9_11_0
shulkerBox_shulker_box_color_block_9_10_0
shulkerBox_shulker_box_color_block_9_8_0
shulkerBox_shulker_box_color_block_9_7_0
shulkerBox_shulker_box_color_block_9_6_0
shulkerBox_shulker_box_color_block_9_5_0
shulkerBox_shulker_box_color_block_9_4_0
shulkerBox_shulker_box_color_block_9_3_0
shulkerBox_shulker_box_color_block_9_2_0
shulkerBox_shulker_box_color_block_9_1_0
shulkerBox_shulker_box_color_block_9_0_0
shulkerBox_shulker_box_color_dye_8_0
shulkerBox_shulker_box_color_block_8_15_0
shulkerBox_shulker_box_color_block_8_14_0
shulkerBox_shulker_box_color_block_8_13_0
shulkerBox_shulker_box_color_block_8_12_0
shulkerBox_shulker_box_color_block_8_11_0
shulkerBox_shulker_box_color_block_8_10_0
shulkerBox_shulker_box_color_block_8_9_0
shulkerBox_shulker_box_color_block_8_7_0
shulkerBox_shulker_box_color_block_8_6_0
shulkerBox_shulker_box_color_block_8_5_0
shulkerBox_shulker_box_color_block_8_4_0
shulkerBox_shulker_box_color_block_8_3_0
shulkerBox_shulker_box_color_block_8_2_0
shulkerBox_shulker_box_color_block_8_1_0
shulkerBox_shulker_box_color_block_8_0_0
shulkerBox_shulker_box_color_dye_7_0
shulkerBox_shulker_box_color_block_7_15_0
shulkerBox_shulker_box_color_block_7_14_0
shulkerBox_shulker_box_color_block_7_13_0
shulkerBox_shulker_box_color_block_7_12_0
shulkerBox_shulker_box_color_block_7_11_0
shulkerBox_shulker_box_color_block_7_10_0
shulkerBox_shulker_box_color_block_7_9_0
shulkerBox_shulker_box_color_block_7_8_0
shulkerBox_shulker_box_color_block_7_6_0
shulkerBox_shulker_box_color_block_7_5_0
shulkerBox_shulker_box_color_block_7_4_0
shulkerBox_shulker_box_color_block_7_3_0
shulkerBox_shulker_box_color_block_7_2_0
shulkerBox_shulker_box_color_block_7_1_0
shulkerBox_shulker_box_color_block_7_0_0
shulkerBox_shulker_box_color_dye_6_0
shulkerBox_shulker_box_color_block_6_15_0
shulkerBox_shulker_box_color_block_6_14_0
shulkerBox_shulker_box_color_block_6_13_0
shulkerBox_shulker_box_color_block_6_12_0
shulkerBox_shulker_box_color_block_6_11_0
shulkerBox_shulker_box_color_block_6_10_0
shulkerBox_shulker_box_color_block_6_9_0
shulkerBox_shulker_box_color_block_6_8_0
shulkerBox_shulker_box_color_block_6_7_0
shulkerBox_shulker_box_color_block_6_5_0
shulkerBox_shulker_box_color_block_6_4_0
shulkerBox_shulker_box_color_block_6_3_0
shulkerBox_shulker_box_color_block_6_2_0
shulkerBox_shulker_box_color_block_6_1_0
shulkerBox_shulker_box_color_block_6_0_0
shulkerBox_shulker_box_color_dye_5_0
shulkerBox_shulker_box_color_block_5_15_0
shulkerBox_shulker_box_color_block_5_14_0
shulkerBox_shulker_box_color_block_5_13_0
shulkerBox_shulker_box_color_block_5_12_0
shulkerBox_shulker_box_color_block_5_11_0
shulkerBox_shulker_box_color_block_5_10_0
shulkerBox_shulker_box_color_block_5_9_0
shulkerBox_shulker_box_color_block_5_8_0
shulkerBox_shulker_box_color_block_5_7_0
shulkerBox_shulker_box_color_block_5_6_0
shulkerBox_shulker_box_color_block_5_4_0
shulkerBox_shulker_box_color_block_5_3_0
shulkerBox_shulker_box_color_block_5_2_0
shulkerBox_shulker_box_color_block_5_1_0
shulkerBox_shulker_box_color_block_5_0_0
shulkerBox_shulker_box_color_dye_4_0
shulkerBox_shulker_box_color_block_4_15_0
shulkerBox_shulker_box_color_block_4_14_0
shulkerBox_shulker_box_color_block_4_13_0
shulkerBox_shulker_box_color_block_4_12_0
shulkerBox_shulker_box_color_block_4_11_0
shulkerBox_shulker_box_color_block_4_10_0
shulkerBox_shulker_box_color_block_4_9_0
shulkerBox_shulker_box_color_block_4_8_0
shulkerBox_shulker_box_color_block_4_7_0
shulkerBox_shulker_box_color_block_4_6_0
shulkerBox_shulker_box_color_block_4_5_0
shulkerBox_shulker_box_color_block_4_3_0
shulkerBox_shulker_box_color_block_4_2_0
shulkerBox_shulker_box_color_block_4_1_0
shulkerBox_shulker_box_color_block_4_0_0
shulkerBox_shulker_box_color_dye_3_0
shulkerBox_shulker_box_color_block_3_15_0
shulkerBox_shulker_box_color_block_3_14_0
shulkerBox_shulker_box_color_block_3_13_0
shulkerBox_shulker_box_color_block_3_12_0
shulkerBox_shulker_box_color_block_3_11_0
shulkerBox_shulker_box_color_block_3_10_0
shulkerBox_shulker_box_color_block_3_9_0
shulkerBox_shulker_box_color_block_3_8_0
shulkerBox_shulker_box_color_block_3_7_0
shulkerBox_shulker_box_color_block_3_6_0
shulkerBox_shulker_box_color_block_3_5_0
shulkerBox_shulker_box_color_block_3_4_0
shulkerBox_shulker_box_color_block_3_2_0
shulkerBox_shulker_box_color_block_3_1_0
shulkerBox_shulker_box_color_block_3_0_0
shulkerBox_shulker_box_color_dye_2_0
shulkerBox_shulker_box_color_block_2_15_0
shulkerBox_shulker_box_color_block_2_14_0
shulkerBox_shulker_box_color_block_2_13_0
shulkerBox_shulker_box_color_block_2_12_0
shulkerBox_shulker_box_color_block_2_11_0
shulkerBox_shulker_box_color_block_2_10_0
shulkerBox_shulker_box_color_block_2_9_0
shulkerBox_shulker_box_color_block_2_8_0
shulkerBox_shulker_box_color_block_2_7_0
shulkerBox_shulker_box_color_block_2_6_0
shulkerBox_shulker_box_color_block_2_5_0
shulkerBox_shulker_box_color_block_2_4_0
shulkerBox_shulker_box_color_block_2_3_0
shulkerBox_shulker_box_color_block_2_1_0
shulkerBox_shulker_box_color_block_2_0_0
shulkerBox_shulker_box_color_dye_1_0
shulkerBox_shulker_box_color_block_1_15_0
shulkerBox_shulker_box_color_block_1_14_0
shulkerBox_shulker_box_color_block_1_13_0
shulkerBox_shulker_box_color_block_1_12_0
shulkerBox_shulker_box_color_block_1_11_0
shulkerBox_shulker_box_color_block_1_10_0
shulkerBox_shulker_box_color_block_1_9_0
shulkerBox_shulker_box_color_block_1_8_0
shulkerBox_shulker_box_color_block_1_7_0
shulkerBox_shulker_box_color_block_1_6_0
shulkerBox_shulker_box_color_block_1_5_0
shulkerBox_shulker_box_color_block_1_4_0
shulkerBox_shulker_box_color_block_1_3_0
shulkerBox_shulker_box_color_block_1_2_0
shulkerBox_shulker_box_color_block_1_0_0
shulkerBox_shulker_box_color_dye_0_0
shulkerBox_shulker_box_color_block_0_15_0
shulkerBox_shulker_box_color_block_0_14_0
shulkerBox_shulker_box_color_block_0_13_0
shulkerBox_shulker_box_color_block_0_12_0
shulkerBox_shulker_box_color_block_0_11_0
shulkerBox_shulker_box_color_block_0_10_0
shulkerBox_shulker_box_color_block_0_9_0
shulkerBox_shulker_box_color_block_0_8_0
shulkerBox_shulker_box_color_block_0_7_0
shulkerBox_shulker_box_color_block_0_6_0
shulkerBox_shulker_box_color_block_0_5_0
shulkerBox_shulker_box_color_block_0_4_0
shulkerBox_shulker_box_color_block_0_3_0
shulkerBox_shulker_box_color_block_0_2_0
shulkerBox_shulker_box_color_block_0_1_0
bundle_dye_19
bundle_dye_19_18
bundle_dye_19_17
bundle_dye_19_16
bundle_dye_19_14
bundle_dye_19_13
bundle_dye_19_12
bundle_dye_19_11
bundle_dye_19_10
bundle_dye_19_9
bundle_dye_19_8
bundle_dye_19_7
bundle_dye_19_6
bundle_dye_19_5
bundle_dye_19_4
bundle_dye_19_3
bundle_dye_19_2
bundle_dye_19_1
bundle_dye_19_0
bundle_dye_18
bundle_dye_18_19
bundle_dye_18_17
bundle_dye_18_16
bundle_dye_18_15
bundle_dye_18_14
bundle_dye_18_13
bundle_dye_18_12
bundle_dye_18_11
bundle_dye_18_10
bundle_dye_18_9
bundle_dye_18_8
bundle_dye_18_7
bundle_dye_18_6
bundle_dye_18_5
bundle_dye_18_3
bundle_dye_18_2
bundle_dye_18_1
bundle_dye_18_0
bundle_dye_17
bundle_dye_17_19
bundle_dye_17_18
bundle_dye_17_16
bundle_dye_17_15
bundle_dye_17_14
bundle_dye_17_13
bundle_dye_17_12
bundle_dye_17_11
bundle_dye_17_10
bundle_dye_17_9
bundle_dye_17_8
bundle_dye_17_7
bundle_dye_17_6
bundle_dye_17_5
bundle_dye_17_4
bundle_dye_17_2
bundle_dye_17_1
bundle_dye_17_0
bundle_dye_16
bundle_dye_16_19
bundle_dye_16_18
bundle_dye_16_17
bundle_dye_16_15
bundle_dye_16_14
bundle_dye_16_13
bundle_dye_16_12
bundle_dye_16_11
bundle_dye_16_10
bundle_dye_16_9
bundle_dye_16_8
bundle_dye_16_7
bundle_dye_16_6
bundle_dye_16_5
bundle_dye_16_4
bundle_dye_16_3
bundle_dye_16_2
bundle_dye_16_1
bundle_dye_15
bundle_dye_15_18
bundle_dye_15_17
bundle_dye_15_16
bundle_dye_15_14
bundle_dye_15_13
bundle_dye_15_12
bundle_dye_15_11
bundle_dye_15_10
bundle_dye_15_9
bundle_dye_15_8
bundle_dye_15_7
bundle_dye_15_6
bundle_dye_15_5
bundle_dye_15_4
bundle_dye_15_3
bundle_dye_15_2
bundle_dye_15_1
bundle_dye_15_0
bundle_dye_14
bundle_dye_14_19
bundle_dye_14_18
bundle_dye_14_17
bundle_dye_14_16
bundle_dye_14_15
bundle_dye_14_13
bundle_dye_14_12
bundle_dye_14_11
bundle_dye_14_10
bundle_dye_14_9
bundle_dye_14_8
bundle_dye_14_7
bundle_dye_14_6
bundle_dye_14_5
bundle_dye_14_4
bundle_dye_14_3
bundle_dye_14_2
bundle_dye_14_1
bundle_dye_14_0
bundle_dye_13
bundle_dye_13_19
bundle_dye_13_18
bundle_dye_13_17
bundle_dye_13_16
bundle_dye_13_15
bundle_dye_13_14
bundle_dye_13_12
bundle_dye_13_11
bundle_dye_13_10
bundle_dye_13_9
bundle_dye_13_8
bundle_dye_13_7
bundle_dye_13_6
bundle_dye_13_5
bundle_dye_13_4
bundle_dye_13_3
bundle_dye_13_2
bundle_dye_13_1
bundle_dye_13_0
bundle_dye_12
bundle_dye_12_19
bundle_dye_12_18
bundle_dye_12_17
bundle_dye_12_16
bundle_dye_12_15
bundle_dye_12_14
bundle_dye_12_13
bundle_dye_12_11
bundle_dye_12_10
bundle_dye_12_9
bundle_dye_12_8
bundle_dye_12_7
bundle_dye_12_6
bundle_dye_12_5
bundle_dye_12_4
bundle_dye_12_3
bundle_dye_12_2
bundle_dye_12_1
bundle_dye_12_0
bundle_dye_11
bundle_dye_11_19
bundle_dye_11_18
bundle_dye_11_17
bundle_dye_11_16
bundle_dye_11_15
bundle_dye_11_14
bundle_dye_11_13
bundle_dye_11_12
bundle_dye_11_10
bundle_dye_11_9
bundle_dye_11_8
bundle_dye_11_7
bundle_dye_11_6
bundle_dye_11_5
bundle_dye_11_4
bundle_dye_11_3
bundle_dye_11_2
bundle_dye_11_1
bundle_dye_11_0
bundle_dye_10
bundle_dye_10_19
bundle_dye_10_18
bundle_dye_10_17
bundle_dye_10_16
bundle_dye_10_15
bundle_dye_10_14
bundle_dye_10_13
bundle_dye_10_12
bundle_dye_10_11
bundle_dye_10_9
bundle_dye_10_8
bundle_dye_10_7
bundle_dye_10_6
bundle_dye_10_5
bundle_dye_10_4
bundle_dye_10_3
bundle_dye_10_2
bundle_dye_10_1
bundle_dye_10_0
bundle_dye_9
bundle_dye_9_19
bundle_dye_9_18
bundle_dye_9_17
bundle_dye_9_16
bundle_dye_9_15
bundle_dye_9_14
bundle_dye_9_13
bundle_dye_9_12
bundle_dye_9_11
bundle_dye_9_10
bundle_dye_9_8
bundle_dye_9_7
bundle_dye_9_6
bundle_dye_9_5
bundle_dye_9_4
bundle_dye_9_3
bundle_dye_9_2
bundle_dye_9_1
bundle_dye_9_0
bundle_dye_8
bundle_dye_8_19
bundle_dye_8_18
bundle_dye_8_17
bundle_dye_8_16
bundle_dye_8_15
bundle_dye_8_14
bundle_dye_8_13
bundle_dye_8_12
bundle_dye_8_11
bundle_dye_8_10
bundle_dye_8_9
bundle_dye_8_7
bundle_dye_8_6
bundle_dye_8_5
bundle_dye_8_4
bundle_dye_8_3
bundle_dye_8_2
bundle_dye_8_1
bundle_dye_8_0
bundle_dye_7
bundle_dye_7_19
bundle_dye_7_18
bundle_dye_7_17
bundle_dye_7_16
bundle_dye_7_15
bundle_dye_7_14
bundle_dye_7_13
bundle_dye_7_12
bundle_dye_7_11
bundle_dye_7_10
bundle_dye_7_9
bundle_dye_7_8
bundle_dye_7_6
bundle_dye_7_5
bundle_dye_7_4
bundle_dye_7_3
bundle_dye_7_2
bundle_dye_7_1
bundle_dye_7_0
bundle_dye_6
bundle_dye_6_19
bundle_dye_6_18
bundle_dye_6_17
bundle_dye_6_16
bundle_dye_6_15
bundle_dye_6_14
bundle_dye_6_13
bundle_dye_6_12
bundle_dye_6_11
bundle_dye_6_10
bundle_dye_6_9
bundle_dye_6_8
bundle_dye_6_7
bundle_dye_6_5
bundle_dye_6_4
bundle_dye_6_3
bundle_dye_6_2
bundle_dye_6_1
bundle_dye_6_0
bundle_dye_5
bundle_dye_5_19
bundle_dye_5_18
bundle_dye_5_17
bundle_dye_5_16
bundle_dye_5_15
bundle_dye_5_14
bundle_dye_5_13
bundle_dye_5_12
bundle_dye_5_11
bundle_dye_5_10
bundle_dye_5_9
bundle_dye_5_8
bundle_dye_5_7
bundle_dye_5_6
bundle_dye_5_4
bundle_dye_5_3
bundle_dye_5_2
bundle_dye_5_1
bundle_dye_5_0
bundle_dye_4
bundle_dye_4_19
bundle_dye_4_17
bundle_dye_4_16
bundle_dye_4_15
bundle_dye_4_14
bundle_dye_4_13
bundle_dye_4_12
bundle_dye_4_11
bundle_dye_4_10
bundle_dye_4_9
bundle_dye_4_8
bundle_dye_4_7
bundle_dye_4_6
bundle_dye_4_5
bundle_dye_4_3
bundle_dye_4_2
bundle_dye_4_1
bundle_dye_4_0
bundle_dye_3
bundle_dye_3_19
bundle_dye_3_18
bundle_dye_3_16
bundle_dye_3_15
bundle_dye_3_14
bundle_dye_3_13
bundle_dye_3_12
bundle_dye_3_11
bundle_dye_3_10
bundle_dye_3_9
bundle_dye_3_8
bundle_dye_3_7
bundle_dye_3_6
bundle_dye_3_5
bundle_dye_3_4
bundle_dye_3_2
bundle_dye_3_1
bundle_dye_3_0
bundle_dye_2
bundle_dye_2_19
bundle_dye_2_18
bundle_dye_2_17
bundle_dye_2_16
bundle_dye_2_15
bundle_dye_2_14
bundle_dye_2_13
bundle_dye_2_12
bundle_dye_2_11
bundle_dye_2_10
bundle_dye_2_9
bundle_dye_2_8
bundle_dye_2_7
bundle_dye_2_6
bundle_dye_2_5
bundle_dye_2_4
bundle_dye_2_3
bundle_dye_2_1
bundle_dye_2_0
bundle_dye_1
bundle_dye_1_19
bundle_dye_1_18
bundle_dye_1_17
bundle_dye_1_16
bundle_dye_1_15
bundle_dye_1_14
bundle_dye_1_13
bundle_dye_1_12
bundle_dye_1_11
bundle_dye_1_10
bundle_dye_1_9
bundle_dye_1_8
bundle_dye_1_7
bundle_dye_1_6
bundle_dye_1_5
bundle_dye_1_4
bundle_dye_1_3
bundle_dye_1_2
bundle_dye_1_0
bundle_dye_0
bundle_dye_0_19
bundle_dye_0_18
bundle_dye_0_17
bundle_dye_0_15
bundle_dye_0_14
bundle_dye_0_13
bundle_dye_0_12
bundle_dye_0_11
bundle_dye_0_10
bundle_dye_0_9
bundle_dye_0_8
bundle_dye_0_7
bundle_dye_0_6
bundle_dye_0_5
bundle_dye_0_4
bundle_dye_0_3
bundle_dye_0_2
bundle_dye_0_1
harness_color_19
harness_color_19_18
harness_color_19_17
harness_color_19_16
harness_color_19_14
harness_color_19_13
harness_color_19_12
harness_color_19_11
harness_color_19_10
harness_color_19_9
harness_color_19_8
harness_color_19_7
harness_color_19_6
harness_color_19_5
harness_color_19_4
harness_color_19_3
harness_color_19_2
harness_color_19_1
harness_color_19_0
harness_color_18
harness_color_18_19
harness_color_18_17
harness_color_18_16
harness_color_18_15
harness_color_18_14
harness_color_18_13
harness_color_18_12
harness_color_18_11
harness_color_18_10
harness_color_18_9
harness_color_18_8
harness_color_18_7
harness_color_18_6
harness_color_18_5
harness_color_18_3
harness_color_18_2
harness_color_18_1
harness_color_18_0
harness_color_17
harness_color_17_19
harness_color_17_18
harness_color_17_16
harness_color_17_15
harness_color_17_14
harness_color_17_13
harness_color_17_12
harness_color_17_11
harness_color_17_10
harness_color_17_9
harness_color_17_8
harness_color_17_7
harness_color_17_6
harness_color_17_5
harness_color_17_4
harness_color_17_2
harness_color_17_1
harness_color_17_0
harness_color_16
harness_color_16_19
harness_color_16_18
harness_color_16_17
harness_color_16_15
harness_color_16_14
harness_color_16_13
harness_color_16_12
harness_color_16_11
harness_color_16_10
harness_color_16_9
harness_color_16_8
harness_color_16_7
harness_color_16_6
harness_color_16_5
harness_color_16_4
harness_color_16_3
harness_color_16_2
harness_color_16_1
harness_color_15
harness_color_15_18
harness_color_15_17
harness_color_15_16
harness_color_15_14
harness_color_15_13
harness_color_15_12
harness_color_15_11
harness_color_15_10
harness_color_15_9
harness_color_15_8
harness_color_15_7
harness_color_15_6
harness_color_15_5
harness_color_15_4
harness_color_15_3
harness_color_15_2
harness_color_15_1
harness_color_15_0
harness_color_14
harness_color_14_19
harness_color_14_18
harness_color_14_17
harness_color_14_16
harness_color_14_15
harness_color_14_13
harness_color_14_12
harness_color_14_11
harness_color_14_10
harness_color_14_9
harness_color_14_8
harness_color_14_7
harness_color_14_6
harness_color_14_5
harness_color_14_4
harness_color_14_3
harness_color_14_2
harness_color_14_1
harness_color_14_0
harness_color_13
harness_color_13_19
harness_color_13_18
harness_color_13_17
harness_color_13_16
harness_color_13_15
harness_color_13_14
harness_color_13_12
harness_color_13_11
harness_color_13_10
harness_color_13_9
harness_color_13_8
harness_color_13_7
harness_color_13_6
harness_color_13_5
harness_color_13_4
harness_color_13_3
harness_color_13_2
harness_color_13_1
harness_color_13_0
harness_color_12
harness_color_12_19
harness_color_12_18
harness_color_12_17
harness_color_12_16
harness_color_12_15
harness_color_12_14
harness_color_12_13
harness_color_12_11
harness_color_12_10
harness_color_12_9
harness_color_12_8
harness_color_12_7
harness_color_12_6
harness_color_12_5
harness_color_12_4
harness_color_12_3
harness_color_12_2
harness_color_12_1
harness_color_12_0
harness_color_11
harness_color_11_19
harness_color_11_18
harness_color_11_17
harness_color_11_16
harness_color_11_15
harness_color_11_14
harness_color_11_13
harness_color_11_12
harness_color_11_10
harness_color_11_9
harness_color_11_8
harness_color_11_7
harness_color_11_6
harness_color_11_5
harness_color_11_4
harness_color_11_3
harness_color_11_2
harness_color_11_1
harness_color_11_0
harness_color_10
harness_color_10_19
harness_color_10_18
harness_color_10_17
harness_color_10_16
harness_color_10_15
harness_color_10_14
harness_color_10_13
harness_color_10_12
harness_color_10_11
harness_color_10_9
harness_color_10_8
harness_color_10_7
harness_color_10_6
harness_color_10_5
harness_color_10_4
harness_color_10_3
harness_color_10_2
harness_color_10_1
harness_color_10_0
harness_color_9
harness_color_9_19
harness_color_9_18
harness_color_9_17
harness_color_9_16
harness_color_9_15
harness_color_9_14
harness_color_9_13
harness_color_9_12
harness_color_9_11
harness_color_9_10
harness_color_9_8
harness_color_9_7
harness_color_9_6
harness_color_9_5
harness_color_9_4
harness_color_9_3
harness_color_9_2
harness_color_9_1
harness_color_9_0
harness_color_8
harness_color_8_19
harness_color_8_18
harness_color_8_17
harness_color_8_16
harness_color_8_15
harness_color_8_14
harness_color_8_13
harness_color_8_12
harness_color_8_11
harness_color_8_10
harness_color_8_9
harness_color_8_7
harness_color_8_6
harness_color_8_5
harness_color_8_4
harness_color_8_3
harness_color_8_2
harness_color_8_1
harness_color_8_0
harness_color_7
harness_color_7_19
harness_color_7_18
harness_color_7_17
harness_color_7_16
harness_color_7_15
harness_color_7_14
harness_color_7_13
harness_color_7_12
harness_color_7_11
harness_color_7_10
harness_color_7_9
harness_color_7_8
harness_color_7_6
harness_color_7_5
harness_color_7_4
harness_color_7_3
harness_color_7_2
harness_color_7_1
harness_color_7_0
harness_color_6
harness_color_6_19
harness_color_6_18
harness_color_6_17
harness_color_6_16
harness_color_6_15
harness_color_6_14
harness_color_6_13
harness_color_6_12
harness_color_6_11
harness_color_6_10
harness_color_6_9
harness_color_6_8
harness_color_6_7
harness_color_6_5
harness_color_6_4
harness_color_6_3
harness_color_6_2
harness_color_6_1
harness_color_6_0
harness_color_5
harness_color_5_19
harness_color_5_18
harness_color_5_17
harness_color_5_16
harness_color_5_15
harness_color_5_14
harness_color_5_13
harness_color_5_12
harness_color_5_11
harness_color_5_10
harness_color_5_9
harness_color_5_8
harness_color_5_7
harness_color_5_6
harness_color_5_4
harness_color_5_3
harness_color_5_2
harness_color_5_1
harness_color_5_0
harness_color_4
harness_color_4_19
harness_color_4_17
harness_color_4_16
harness_color_4_15
harness_color_4_14
harness_color_4_13
harness_color_4_12
harness_color_4_11
harness_color_4_10
harness_color_4_9
harness_color_4_8
harness_color_4_7
harness_color_4_6
harness_color_4_5
harness_color_4_3
harness_color_4_2
harness_color_4_1
harness_color_4_0
harness_color_3
harness_color_3_19
harness_color_3_18
harness_color_3_16
harness_color_3_15
harness_color_3_14
harness_color_3_13
harness_color_3_12
harness_color_3_11
harness_color_3_10
harness_color_3_9
harness_color_3_8
harness_color_3_7
harness_color_3_6
harness_color_3_5
harness_color_3_4
harness_color_3_2
harness_color_3_1
harness_color_3_0
harness_color_2
harness_color_2_19
harness_color_2_18
harness_color_2_17
harness_color_2_16
harness_color_2_15
harness_color_2_14
harness_color_2_13
harness_color_2_12
harness_color_2_11
harness_color_2_10
harness_color_2_9
harness_color_2_8
harness_color_2_7
harness_color_2_6
harness_color_2_5
harness_color_2_4
harness_color_2_3
harness_color_2_1
harness_color_2_0
harness_color_1
harness_color_1_19
harness_color_1_18
harness_color_1_17
harness_color_1_16
harness_color_1_15
harness_color_1_14
harness_color_1_13
harness_color_1_12
harness_color_1_11
harness_color_1_10
harness_color_1_9
harness_color_1_8
harness_color_1_7
harness_color_1_6
harness_color_1_5
harness_color_1_4
harness_color_1_3
harness_color_1_2
harness_color_1_0
harness_color_0
harness_color_0_19
harness_color_0_18
harness_color_0_17
harness_color_0_15
harness_color_0_14
harness_color_0_13
harness_color_0_12
harness_color_0_11
harness_color_0_10
harness_color_0_9
harness_color_0_8
harness_color_0_7
harness_color_0_6
harness_color_0_5
harness_color_0_4
harness_color_0_3
harness_color_0_2
harness_color_0_1
bed_color_19
bed_color_18
bed_color_17
bed_color_16
bed_color_15
bed_color_14
bed_color_13
bed_color_12
bed_color_11
bed_color_10
bed_color_9
bed_color_8
bed_color_7
bed_color_6
bed_color_5
bed_color_4
bed_color_3
bed_color_2
bed_color_1
bed_color_0
bed_color_bamboo_0
bed_color_bamboo_1
bed_color_bamboo_2
bed_color_bamboo_3
bed_color_bamboo_4
bed_color_bamboo_5
bed_color_bamboo_6
bed_color_bamboo_7
bed_color_bamboo_8
bed_color_bamboo_9
bed_color_bamboo_10
bed_color_bamboo_11
bed_color_bamboo_12
bed_color_bamboo_13
bed_color_bamboo_14
bed_color_bamboo_15
Stick_bamboo_recipeId
WoodButton_recipeId
WoodPressurePlate_recipeId
ButtonAcacia_recipeId
PressurePlateAcacia_recipeId
ButtonBirch_recipeId
PressurePlateBirch_recipeId
ButtonDarkOak_recipeId
PressurePlateDarkOak_recipeId
ButtonJungle_recipeId
PressurePlateJungle_recipeId
ButtonSpruce_recipeId
PressurePlateSpruce_recipeId
Trapdoor_recipeId
TrapdoorAcacia_recipeId
TrapdoorBirch_recipeId
TrapdoorDarkOak_recipeId
TrapdoorJungle_recipeId
TrapdoorSpruce_recipeId
StoneSlab4_recipeId
StoneSlab_recipeId
StoneSlab4_stoneBrick_recipeId
StoneSlab_StoneBrick_recipeId
StoneSlab_Brick_recipeId
Painting_Cobblestone_recipeId
Painting_NetherBrick_recipeId
Painting_VanillaBlocks_recipeId
stoneslab2_RedSandstone_recipeId
stoneslab_sandstone_heiroglyphs_recipeId
stoneslab2_redsandstone_heiroglyphs_recipeId
stoneslab2_purpur_recipeId
stoneslab4_smoothquartz_smooth_recipeId
stoneslab_quartz_recipeId
stoneslab_recipeId
stoneslab2_prismarine_recipeId
stoneslab2_prismarine_bricks_recipeId
stoneslab2_recipeId
stoneslab2_smoothsandstone_smooth_recipeId
stoneslab2_rednetherbrick_recipeId
slab3_endstonebrick_recipeId
stoneslab3_smooth_recipeId
stoneslab3_polished_andesite_andesitesmooth_recipeId
stoneslab3_andesite_recipeId
stoneslab3_diorite_recipeId
stoneslab3_polished_diorite_dioritesmooth_recipeId
stoneslab3_granite
stoneslab3_polishedGranite_GraniteSmooth_recipeId
stoneslab4_cut_sandstone_cut_recipeId
stoneslab4_cut_redsandstone_cut_recipeId
oak_stairs_oak_recipeId
spruce_stairs_spruce_recipeId
birch_stairs_birch_recipeId
jungle_stairs_jungle_recipeId
acacia_stairs_acacia_recipeId
dark_oak_stairs_dark_oak_recipeId
chiseled_quartz_recipeId
heiroglyphs_redsandstone_recipeId
heiroglyphs_sandstone_recipeId
chiseled_stonebrick_recipeId
lines_purpur_recipeId
paper_sulphur_recipeId
weapon_arrow_recipe_5
weapon_arrow_recipe_6
weapon_arrow_recipe_7
weapon_arrow_recipe_8
weapon_arrow_recipe_9
weapon_arrow_recipe_10
weapon_arrow_recipe_11
weapon_arrow_recipe_12
weapon_arrow_recipe_13
weapon_arrow_recipe_14
weapon_arrow_recipe_15
weapon_arrow_recipe_16
weapon_arrow_recipe_17
weapon_arrow_recipe_18
weapon_arrow_recipe_19
weapon_arrow_recipe_20
weapon_arrow_recipe_21
weapon_arrow_recipe_22
weapon_arrow_recipe_23
weapon_arrow_recipe_24
weapon_arrow_recipe_25
weapon_arrow_recipe_26
weapon_arrow_recipe_27
weapon_arrow_recipe_28
weapon_arrow_recipe_29
weapon_arrow_recipe_30
weapon_arrow_recipe_31
weapon_arrow_recipe_32
weapon_arrow_recipe_33
weapon_arrow_recipe_34
weapon_arrow_recipe_35
weapon_arrow_recipe_36
weapon_arrow_recipe_37
weapon_arrow_recipe_38
weapon_arrow_recipe_39
weapon_arrow_recipe_40
weapon_arrow_recipe_41
weapon_arrow_recipe_42
weapon_arrow_recipe_43
weapon_arrow_recipe_44
weapon_arrow_recipe_45
weapon_arrow_recipe_46
decorated_pot_base_recipeId
```

</details>

#### Dynamic Enum: StructureFeature (#5)

Value count now: 17

<details>
<summary>Show values</summary>

```
minecraft:end_city
minecraft:fortress
minecraft:mineshaft
minecraft:monument
minecraft:stronghold
minecraft:temple
minecraft:village
minecraft:mansion
minecraft:shipwreck
minecraft:buried_treasure
minecraft:ruins
minecraft:pillager_outpost
minecraft:ruined_portal
minecraft:bastion_remnant
minecraft:ancient_city
minecraft:trail_ruins
minecraft:trial_chambers
```

</details>

#### Dynamic Enum: JigsawStructure (#6)

Value count now: 2

<details>
<summary>Show values</summary>

```
minecraft:trail_ruins
minecraft:trial_chambers
```

</details>

#### Dynamic Enum: EntityEvents (#7)

Value count now: 451

<details>
<summary>Show values</summary>

```
abort_sheltering
admire_item_started_event
admire_item_stopped_event
ageable_grow_up
attack_cooldown_complete_event
attacked
be_sheared
become_angry
become_angry_event
become_calm_event
become_cow
become_pregnant
become_stray_event
become_witch
become_zombie
become_zombie_event
calmed_down
change_to_skeleton
collected_nectar
countdown_to_perish_event
dried_out
enter_water
escaped_event
fed_open_eyeblossom
fed_wither_rose
find_flower_timeout
find_hive_event
find_hive_timeout
from_explosion
from_village
go_back_to_spawn_failed
got_in_powder_snow
got_out_of_powder_snow
grow_up
hive_destroyed
important_block_destroyed_event
in_desert
in_snow
killed_enemy_event
laid_egg
minecraft:add_attributes
minecraft:add_biome_and_skin
minecraft:add_can_ride
minecraft:add_damage_timer
minecraft:add_periodic_damage
minecraft:ageable_grow_up
minecraft:ageable_set_baby
minecraft:all_riders_dismounted
minecraft:ambient_night
minecraft:ambient_normal
minecraft:ambient_sleep
minecraft:as_adult
minecraft:as_baby
minecraft:as_baby_jockey
minecraft:as_ranged_adult
minecraft:as_ranged_baby
minecraft:as_ranged_baby_jockey
minecraft:as_rider
minecraft:ate_allium
minecraft:ate_bluet
minecraft:ate_closed_eyeblossom
minecraft:ate_cornflower
minecraft:ate_daisy
minecraft:ate_dandelion
minecraft:ate_lily
minecraft:ate_open_eyeblossom
minecraft:ate_orchid
minecraft:ate_poppy
minecraft:ate_rose
minecraft:ate_torchflower
minecraft:ate_tulip
minecraft:baby_on_calm
minecraft:become_aggressive
minecraft:become_aggro
minecraft:become_anenonme
minecraft:become_angry
minecraft:become_armorable
minecraft:become_armorer
minecraft:become_black_tang
minecraft:become_blue_dory
minecraft:become_brown
minecraft:become_brown_adult
minecraft:become_butcher
minecraft:become_butterfly_fish
minecraft:become_calm
minecraft:become_cartographer
minecraft:become_cc_betta
minecraft:become_charged
minecraft:become_cichlid
minecraft:become_cleric
minecraft:become_clownfish
minecraft:become_dog_fish
minecraft:become_e_red_snapper
minecraft:become_farmer
minecraft:become_fisherman
minecraft:become_fletcher
minecraft:become_goat_fish
minecraft:become_hostile
minecraft:become_immobile
minecraft:become_leatherworker
minecraft:become_librarian
minecraft:become_mason
minecraft:become_mobile
minecraft:become_moorish_idol
minecraft:become_neutral
minecraft:become_ornate_butterfly
minecraft:become_parrot_fish
minecraft:become_pregnant
minecraft:become_queen_angel_fish
minecraft:become_red
minecraft:become_red_adult
minecraft:become_red_cichlid
minecraft:become_red_lipped_benny
minecraft:become_red_snapper
minecraft:become_scared
minecraft:become_sheperd
minecraft:become_statue
minecraft:become_stunned
minecraft:become_threadfin
minecraft:become_tomato_clown
minecraft:become_toolsmith
minecraft:become_triggerfish
minecraft:become_unskilled
minecraft:become_weaponsmith
minecraft:become_yellow_tail_parrot
minecraft:become_yellow_tang
minecraft:begin_oxidizing
minecraft:born_default
minecraft:born_screamer
minecraft:calm
minecraft:camel_husk_saddled
minecraft:camel_husk_unsaddled
minecraft:camel_saddled
minecraft:camel_unsaddled
minecraft:cat_gifted_owner
minecraft:clear_add_raid_omen
minecraft:cold_color
minecraft:command_block_activate
minecraft:command_block_deactivate
minecraft:convert_to_drowned
minecraft:convert_to_zombie
minecraft:crumble
minecraft:crumble_and_notify_creaking_heart
minecraft:crystal_explode
minecraft:damaged_by_entity
minecraft:damaged_by_player
minecraft:defend_wandering_trader
minecraft:donkey_saddled
minecraft:donkey_unsaddled
minecraft:emerged
minecraft:end_roar
minecraft:entered_bubble_column_down
minecraft:entered_bubble_column_up
minecraft:entity_born
minecraft:entity_born_wild
minecraft:entity_spawned
minecraft:entity_spawned_by_creaking_heart
minecraft:entity_spawned_with_biome_specific_jockey
minecraft:entity_spawned_with_default_jockey
minecraft:entity_transformed
minecraft:exited_bubble_column
minecraft:exited_disturbed_hive
minecraft:exited_hive
minecraft:exited_hive_on_fire
minecraft:explode
minecraft:flowerless
minecraft:fox_configure_day
minecraft:fox_configure_defending
minecraft:fox_configure_docile_day
minecraft:fox_configure_docile_night
minecraft:fox_configure_night
minecraft:fox_configure_thunderstorm
minecraft:from_full_puff
minecraft:from_player
minecraft:from_player_default
minecraft:from_player_exposed
minecraft:from_player_oxidized
minecraft:from_player_spawned
minecraft:from_player_weathered
minecraft:from_serialized_entity
minecraft:from_village
minecraft:from_wandering_trader
minecraft:gain_raid_omen
minecraft:go_lay_egg
minecraft:has_target
minecraft:hatch_cold
minecraft:hatch_warm
minecraft:hive_full
minecraft:hopper_activate
minecraft:hopper_deactivate
minecraft:horse_saddled
minecraft:horse_unsaddled
minecraft:hostile_dismounted
minecraft:hostile_mounted
minecraft:increase_max_health
minecraft:increment_swaying_ticks
minecraft:join_caravan
minecraft:laid_egg
minecraft:leave_caravan
minecraft:lost_target
minecraft:mad_at_wolf
minecraft:make_black
minecraft:make_brown
minecraft:make_chestnut
minecraft:make_creamy
minecraft:make_darkbrown
minecraft:make_gray
minecraft:make_white
minecraft:maximum_oxidation
minecraft:melee_mode
minecraft:mule_saddled
minecraft:mule_unsaddled
minecraft:no_threat_detected
minecraft:on_anger
minecraft:on_armor_equip
minecraft:on_calm
minecraft:on_chest
minecraft:on_deflate
minecraft:on_dismount
minecraft:on_drowned_dismount
minecraft:on_drowned_mount
minecraft:on_eat_block
minecraft:on_full_puff
minecraft:on_half_puff
minecraft:on_harnessed
minecraft:on_hurt_event
minecraft:on_instant_prime
minecraft:on_leash
minecraft:on_mount
minecraft:on_normal_puff
minecraft:on_not_riding_player
minecraft:on_passenger_dismount
minecraft:on_passenger_mount
minecraft:on_player_dismount
minecraft:on_player_mount
minecraft:on_prime
minecraft:on_riding_player
minecraft:on_saddled
minecraft:on_saddled_in_water
minecraft:on_saddled_out_of_water
minecraft:on_scared
minecraft:on_sheared
minecraft:on_start_riding_camel_husk
minecraft:on_start_riding_zombie_horse
minecraft:on_stop_riding_camel_husk
minecraft:on_stop_riding_zombie_horse
minecraft:on_stop_tempting
minecraft:on_take_flower
minecraft:on_tame
minecraft:on_target_start_looking
minecraft:on_target_stop_looking
minecraft:on_trust
minecraft:on_unharnessed
minecraft:on_unleash
minecraft:on_unleashed
minecraft:on_unsaddled
minecraft:oxidize_copper
minecraft:panda_aggressive
minecraft:panda_brown
minecraft:panda_lazy
minecraft:panda_playful
minecraft:panda_weak
minecraft:panda_worried
minecraft:pet_slept_with_owner
minecraft:promote_to_illager_captain
minecraft:promote_to_patrol_captain
minecraft:raid_expired
minecraft:randomize_sound_variant
minecraft:ranged_mode
minecraft:remove_oxidation_layer
minecraft:remove_persistence
minecraft:remove_raid_trigger
minecraft:reset_swaying_ticks
minecraft:restart_oxidation_timer
minecraft:resupply_trades
minecraft:rider_mounted
minecraft:roll_up
minecraft:schedule_bed_villager
minecraft:schedule_gather_villager
minecraft:schedule_home_villager
minecraft:schedule_play_villager
minecraft:schedule_wander_villager
minecraft:schedule_work_farmer
minecraft:schedule_work_fisher
minecraft:schedule_work_librarian
minecraft:schedule_work_pro_villager
minecraft:scheduled
minecraft:serialize_entity_succeeded
minecraft:set_trap
minecraft:sink
minecraft:spawn_adult
minecraft:spawn_adult_with_rider
minecraft:spawn_armorer
minecraft:spawn_as_illager_captain
minecraft:spawn_as_patrol_follower
minecraft:spawn_as_rider
minecraft:spawn_as_strider_jockey
minecraft:spawn_baby
minecraft:spawn_baby_strider_jockey
minecraft:spawn_butcher
minecraft:spawn_cleric
minecraft:spawn_cold
minecraft:spawn_emerging
minecraft:spawn_farmer
minecraft:spawn_for_raid
minecraft:spawn_for_raid_with_evoker_rider
minecraft:spawn_for_raid_with_pillager_rider
minecraft:spawn_from_village
minecraft:spawn_librarian
minecraft:spawn_midnight_cat
minecraft:spawn_skilled_adult
minecraft:spawn_tame
minecraft:spawn_tame_adult
minecraft:spawn_tame_baby
minecraft:spawn_temperate
minecraft:spawn_warm
minecraft:spawn_wild
minecraft:spawn_wild_adult
minecraft:spawn_wild_ashen
minecraft:spawn_wild_baby
minecraft:spawn_wild_baby_or_adult
minecraft:spawn_wild_black
minecraft:spawn_wild_chestnut
minecraft:spawn_wild_pale
minecraft:spawn_wild_rusty
minecraft:spawn_wild_snowy
minecraft:spawn_wild_spotted
minecraft:spawn_wild_striped
minecraft:spawn_wild_woods
minecraft:spawn_with_pillager_captain_rider
minecraft:spawn_with_pillager_rider
minecraft:spawn_with_rider
minecraft:spawn_with_vindicator_captain_rider
minecraft:spawn_with_vindicator_rider
minecraft:spring_trap
minecraft:start_celebrating
minecraft:start_death
minecraft:start_despawn
minecraft:start_exploding
minecraft:start_exploding_forced
minecraft:start_fly
minecraft:start_full_puff
minecraft:start_half_puff
minecraft:start_johnny
minecraft:start_land
minecraft:start_peeking
minecraft:start_playing_idle_ground_sound
minecraft:start_roar
minecraft:start_sitting
minecraft:start_transforming
minecraft:start_twitching
minecraft:start_unrolling
minecraft:started_riding
minecraft:stop_aggro
minecraft:stop_celebrating
minecraft:stop_exploding
minecraft:stop_johnny
minecraft:stop_peeking
minecraft:stop_playing_idle_ground_sound
minecraft:stop_sitting
minecraft:stop_transforming
minecraft:stopped_riding
minecraft:switch_to_ai_controlled
minecraft:switch_to_melee
minecraft:switch_to_player_controlled
minecraft:switch_to_ranged
minecraft:target_far_enough
minecraft:target_too_close
minecraft:temperate_color
minecraft:threat_detected
minecraft:to_full_puff
minecraft:transport_items.start_place_fail
minecraft:transport_items.start_place_succeed
minecraft:transport_items.start_take_fail
minecraft:transport_items.start_take_succeed
minecraft:transport_items.stop_interaction
minecraft:trigger_raid
minecraft:turn_black
minecraft:turn_blue
minecraft:turn_brown
minecraft:turn_cyan
minecraft:turn_gray
minecraft:turn_green
minecraft:turn_light_blue
minecraft:turn_lime
minecraft:turn_magenta
minecraft:turn_orange
minecraft:turn_pink
minecraft:turn_purple
minecraft:turn_red
minecraft:turn_silver
minecraft:turn_white
minecraft:turn_yellow
minecraft:unroll
minecraft:upgrade_to_1_21_100
minecraft:upgrade_to_1_21_130
minecraft:warm_color
minecraft:wax_off
minecraft:wax_on
navigation_off_land
navigation_on_land
on_calm
on_digging_event
on_digging_start
on_egg_spawned
on_fail_during_digging
on_fail_during_searching
on_feeling_happy_end
on_item_found
on_not_riding_parent
on_poison_effect_added
on_pregnant
on_rising_end
on_scenting_success
on_search_and_digging_success
on_wither_effect_added
perish_event
pickup_item_delay
pickup_item_delay_complete
recover_after_dried_out
seek_shelter
spawn_adult
spawn_adult_melee
spawn_adult_melee_no_hunting
spawn_adult_no_hunting
spawn_adult_parent_jockey
spawn_adult_piglin_jockey
spawn_adult_ranged
spawn_adult_ranged_no_hunting
spawn_adult_unhuntable
spawn_baby
spawn_cold
spawn_large
spawn_medium
spawn_small
spawn_temperate
spawn_warm
start_drying_out
start_dryingout
start_event
start_suffocating
start_zombification_event
stop_drying_out
stop_dryingout
stop_panicking_after_fire
stop_suffocating
stop_zombification_event
switch_to_melee
switch_to_ranged
villager_converted
wololo
```

</details>

#### Dynamic Enum: CameraPresets (#8)

Value count now: 6

<details>
<summary>Show values</summary>

```
minecraft:first_person
minecraft:fixed_boom
minecraft:follow_orbit
minecraft:free
minecraft:third_person
minecraft:third_person_front
```

</details>

#### Dynamic Enum: GameTestName (#9)

Value count now: 0

<details>
<summary>Show values</summary>

```
(runtime-provided or currently empty)
```

</details>

#### Dynamic Enum: GameTestTag (#10)

Value count now: 0

<details>
<summary>Show values</summary>

```
(runtime-provided or currently empty)
```

</details>

#### Dynamic Enum: Tool (#11)

Value count now: 1907

<details>
<summary>Show values</summary>

```
mainhand
offhand
minecraft:wooden_spear
minecraft:bow
minecraft:brain_coral_fan
minecraft:waxed_exposed_copper_bulb
minecraft:purpur_block
minecraft:cooked_cod
minecraft:music_disc_ward
minecraft:enderman_spawn_egg
minecraft:air
minecraft:copper_golem_statue
minecraft:charcoal
minecraft:stray_spawn_egg
minecraft:light_block_2
minecraft:stone_spear
minecraft:copper_helmet
minecraft:wooden_slab
minecraft:silver_glazed_terracotta
minecraft:cocoa_beans
minecraft:tropical_fish
minecraft:iron_golem_spawn_egg
minecraft:golden_spear
minecraft:waxed_oxidized_copper_door
minecraft:acacia_log
minecraft:copper_spear
minecraft:wooden_pickaxe
minecraft:beetroot_soup
minecraft:waxed_weathered_copper_door
minecraft:piglin_head
minecraft:magenta_candle_cake
minecraft:item.campfire
minecraft:melon_slice
minecraft:diamond_spear
minecraft:enchanted_book
minecraft:totem_of_undying
minecraft:netherite_spear
minecraft:hard_green_stained_glass_pane
minecraft:light_blue_shulker_box
minecraft:iron_spear
minecraft:white_stained_glass_pane
minecraft:black_bundle
minecraft:item.mangrove_door
minecraft:endermite_spawn_egg
minecraft:pink_bundle
minecraft:orange_tulip
minecraft:weathered_cut_copper_stairs
minecraft:rapid_fertilizer
minecraft:blue_bundle
minecraft:clay
minecraft:tropical_fish_spawn_egg
minecraft:dead_bubble_coral_block
minecraft:green_candle
minecraft:brown_bundle
minecraft:sparkler
minecraft:warped_door
minecraft:cooked_salmon
minecraft:underwater_tnt
minecraft:pufferfish_spawn_egg
minecraft:red_mushroom_block
minecraft:crimson_fungus
minecraft:item.frame
minecraft:bundle
minecraft:cyan_bundle
minecraft:skull_pottery_sherd
minecraft:rabbit
minecraft:sea_lantern
minecraft:creeper_banner_pattern
minecraft:ravager_spawn_egg
minecraft:cooked_porkchop
minecraft:mangrove_leaves
minecraft:polished_blackstone_brick_slab
minecraft:mushroom_stew
minecraft:weathered_copper_door
minecraft:pale_oak_fence
minecraft:iron_horse_armor
minecraft:gray_bundle
minecraft:raw_copper_block
minecraft:green_bundle
minecraft:barrel
minecraft:iron_chestplate
minecraft:waxed_oxidized_cut_copper_stairs
minecraft:torch
minecraft:light_blue_bundle
minecraft:bookshelf
minecraft:golden_horse_armor
minecraft:smooth_quartz_stairs
minecraft:potato
minecraft:element_15
minecraft:nether_star
minecraft:enchanted_golden_apple
minecraft:magenta_terracotta
minecraft:polished_tuff_double_slab
minecraft:tuff
minecraft:light_gray_bundle
minecraft:honeycomb
minecraft:lime_bundle
minecraft:coast_armor_trim_smithing_template
minecraft:compass
minecraft:magenta_bundle
minecraft:netherite_sword
minecraft:music_disc_stal
minecraft:music_disc_wait
minecraft:orange_bundle
minecraft:wooden_door
minecraft:balloon
minecraft:smooth_sandstone_double_slab
minecraft:purple_bundle
minecraft:jungle_sign
minecraft:oak_fence
minecraft:white_candle_cake
minecraft:respawn_anchor
minecraft:red_bundle
minecraft:dead_tube_coral_wall_fan
minecraft:deepslate_lapis_ore
minecraft:white_bundle
minecraft:jungle_door
minecraft:music_disc_cat
minecraft:zoglin_spawn_egg
minecraft:flint_and_steel
minecraft:granite_stairs
minecraft:mourner_pottery_sherd
minecraft:yellow_bundle
minecraft:deepslate_tile_wall
minecraft:golden_carrot
minecraft:spruce_stairs
minecraft:element_13
minecraft:poisonous_potato
minecraft:breeze_rod
minecraft:smooth_quartz_slab
minecraft:raw_gold_block
minecraft:vex_armor_trim_smithing_template
minecraft:black_carpet
minecraft:carrot
minecraft:strider_spawn_egg
minecraft:pale_oak_chest_boat
minecraft:command_block
minecraft:potion
minecraft:chicken
minecraft:ominous_trial_key
minecraft:dead_fire_coral_fan
minecraft:smooth_stone
minecraft:element_43
minecraft:beetroot
minecraft:music_disc_strad
minecraft:iron_sword
minecraft:trial_key
minecraft:red_sandstone_slab
minecraft:lantern
minecraft:torchflower_seeds
minecraft:green_harness
minecraft:resin_brick
minecraft:white_candle
minecraft:sweet_berries
minecraft:clay_ball
minecraft:copper_sword
minecraft:element_68
minecraft:wind_charge
minecraft:diorite_wall
minecraft:bamboo_sign
minecraft:apple
minecraft:stripped_oak_log
minecraft:element_50
minecraft:board
minecraft:angler_pottery_sherd
minecraft:golden_apple
minecraft:cherry_chest_boat
minecraft:bread
minecraft:slime_spawn_egg
minecraft:pink_carpet
minecraft:chipped_anvil
minecraft:porkchop
minecraft:cookie
minecraft:music_disc_chirp
minecraft:prismarine_bricks_stairs
minecraft:cooked_rabbit
minecraft:glow_squid_spawn_egg
minecraft:item.iron_door
minecraft:cod
minecraft:beef
minecraft:gray_stained_glass_pane
minecraft:blaze_spawn_egg
minecraft:deepslate_bricks
minecraft:salmon
minecraft:trapped_chest
minecraft:pufferfish
minecraft:ancient_debris
minecraft:bucket
minecraft:dried_kelp
minecraft:stonecutter_block
minecraft:exposed_copper
minecraft:cooked_beef
minecraft:comparator
minecraft:witch_spawn_egg
minecraft:dirt
minecraft:element_62
minecraft:rotten_flesh
minecraft:campfire
minecraft:lingering_potion
minecraft:rabbit_foot
minecraft:smoker
minecraft:mangrove_wood
minecraft:cooked_chicken
minecraft:spider_eye
minecraft:horse_spawn_egg
minecraft:baked_potato
minecraft:pink_tulip
minecraft:chiseled_copper
minecraft:obsidian
minecraft:prize_pottery_sherd
minecraft:pumpkin_pie
minecraft:spruce_wood
minecraft:rabbit_stew
minecraft:yellow_concrete
minecraft:white_tulip
minecraft:hard_pink_stained_glass
minecraft:wheat_seeds
minecraft:command_block_minecart
minecraft:chest
minecraft:element_2
minecraft:pumpkin_seeds
minecraft:melon_seeds
minecraft:acacia_shelf
minecraft:nether_wart
minecraft:beetroot_seeds
minecraft:powder_snow
minecraft:lime_carpet
minecraft:iron_bars
minecraft:element_80
minecraft:polar_bear_spawn_egg
minecraft:pitcher_pod
minecraft:element_104
minecraft:iron_shovel
minecraft:hard_brown_stained_glass
minecraft:happy_ghast_spawn_egg
minecraft:pillager_spawn_egg
minecraft:iron_pickaxe
minecraft:raw_iron
minecraft:iron_axe
minecraft:melon_block
minecraft:arrow
minecraft:oxeye_daisy
minecraft:coal
minecraft:diamond
minecraft:oak_chest_boat
minecraft:brown_concrete_powder
minecraft:iron_ingot
minecraft:stone_brick_stairs
minecraft:yellow_glazed_terracotta
minecraft:blue_carpet
minecraft:portal
minecraft:gold_ingot
minecraft:oxidized_cut_copper_stairs
minecraft:wooden_sword
minecraft:netherite_boots
minecraft:music_disc_mall
minecraft:camel_husk_spawn_egg
minecraft:hay_block
minecraft:nautilus_shell
minecraft:wooden_shovel
minecraft:music_disc_creator_music_box
minecraft:zombie_pigman_spawn_egg
minecraft:crimson_trapdoor
minecraft:raw_gold
minecraft:waxed_exposed_copper_lantern
minecraft:wooden_axe
minecraft:farmland
minecraft:light_blue_glazed_terracotta
minecraft:stone_sword
minecraft:light_block_15
minecraft:stone_shovel
minecraft:light_gray_stained_glass_pane
minecraft:smooth_stone_slab
minecraft:salmon_bucket
minecraft:planks
minecraft:stone_pickaxe
minecraft:stone_axe
minecraft:stained_glass_pane
minecraft:polished_diorite_slab
minecraft:oxidized_copper_trapdoor
minecraft:end_stone_brick_slab
minecraft:smithing_table
minecraft:colored_torch_purple
minecraft:diamond_sword
minecraft:resin_brick_stairs
minecraft:exposed_copper_trapdoor
minecraft:chainmail_helmet
minecraft:diamond_shovel
minecraft:diamond_pickaxe
minecraft:diamond_axe
minecraft:mangrove_boat
minecraft:hard_glass
minecraft:spyglass
minecraft:deepslate_brick_slab
minecraft:mace
minecraft:dark_prismarine_slab
minecraft:flow_armor_trim_smithing_template
minecraft:stick
minecraft:flowing_water
minecraft:bowl
minecraft:arms_up_pottery_sherd
minecraft:mangrove_hanging_sign
minecraft:azure_bluet
minecraft:warped_wart_block
minecraft:vine
minecraft:spruce_fence
minecraft:petrified_oak_slab
minecraft:golden_sword
minecraft:lit_deepslate_redstone_ore
minecraft:golden_shovel
minecraft:elytra
minecraft:green_wool
minecraft:lit_redstone_lamp
minecraft:golden_pickaxe
minecraft:element_52
minecraft:golden_axe
minecraft:string
minecraft:feather
minecraft:gunpowder
minecraft:skull_banner_pattern
minecraft:birch_sapling
minecraft:acacia_stairs
minecraft:wooden_hoe
minecraft:snow_golem_spawn_egg
minecraft:stone_hoe
minecraft:blue_orchid
minecraft:brick_wall
minecraft:panda_spawn_egg
minecraft:brown_terracotta
minecraft:iron_hoe
minecraft:diamond_hoe
minecraft:stripped_cherry_wood
minecraft:element_86
minecraft:cherry_sign
minecraft:golden_hoe
minecraft:magenta_dye
minecraft:wheat
minecraft:glow_frame
minecraft:silence_armor_trim_smithing_template
minecraft:leather_helmet
minecraft:petrified_oak_double_slab
minecraft:leather_chestplate
minecraft:leather_leggings
minecraft:glistering_melon_slice
minecraft:lodestone
minecraft:leather_boots
minecraft:end_gateway
minecraft:chainmail_chestplate
minecraft:item.beetroot
minecraft:dark_oak_double_slab
minecraft:chainmail_leggings
minecraft:chainmail_boots
minecraft:snowball
minecraft:iron_helmet
minecraft:iron_leggings
minecraft:iron_boots
minecraft:burn_pottery_sherd
minecraft:ender_eye
minecraft:hard_cyan_stained_glass_pane
minecraft:music_disc_pigstep
minecraft:diamond_helmet
minecraft:stone_pressure_plate
minecraft:diamond_chestplate
minecraft:rose_bush
minecraft:sand
minecraft:cut_copper_slab
minecraft:axolotl_spawn_egg
minecraft:diamond_leggings
minecraft:diamond_boots
minecraft:element_51
minecraft:golden_helmet
minecraft:green_stained_glass
minecraft:golden_chestplate
minecraft:glowstone
minecraft:golden_leggings
minecraft:polished_deepslate_stairs
minecraft:golden_boots
minecraft:shield
minecraft:agent_spawn_egg
minecraft:carpet
minecraft:flint
minecraft:cyan_carpet
minecraft:wet_sponge
minecraft:colored_torch_blue
minecraft:heart_of_the_sea
minecraft:painting
minecraft:oak_sign
minecraft:flow_banner_pattern
minecraft:milk_bucket
minecraft:red_dye
minecraft:tadpole_bucket
minecraft:bone
minecraft:cherry_wall_sign
minecraft:element_74
minecraft:water_bucket
minecraft:mossy_stone_bricks
minecraft:tube_coral_block
minecraft:dead_brain_coral_wall_fan
minecraft:shulker_spawn_egg
minecraft:mangrove_fence_gate
minecraft:magenta_glazed_terracotta
minecraft:lava_bucket
minecraft:vindicator_spawn_egg
minecraft:cod_bucket
minecraft:crimson_pressure_plate
minecraft:oxidized_copper_chain
minecraft:spruce_fence_gate
minecraft:exposed_cut_copper_slab
minecraft:tropical_fish_bucket
minecraft:pufferfish_bucket
minecraft:dead_brain_coral_block
minecraft:music_disc_11
minecraft:evoker_spawn_egg
minecraft:item.nether_wart
minecraft:powder_snow_bucket
minecraft:parrot_spawn_egg
minecraft:damaged_anvil
minecraft:axolotl_bucket
minecraft:wolf_spawn_egg
minecraft:minecart
minecraft:cyan_concrete_powder
minecraft:saddle
minecraft:iron_door
minecraft:redstone
minecraft:closed_eyeblossom
minecraft:heavy_core
minecraft:sheep_spawn_egg
minecraft:sniffer_egg
minecraft:elder_guardian_spawn_egg
minecraft:fire_coral_fan
minecraft:red_sandstone_wall
minecraft:crossbow
minecraft:waxed_weathered_copper_bars
minecraft:dead_fire_coral_wall_fan
minecraft:white_shulker_box
minecraft:activator_rail
minecraft:oak_boat
minecraft:element_97
minecraft:birch_boat
minecraft:polished_granite_stairs
minecraft:jungle_boat
minecraft:lime_stained_glass_pane
minecraft:copper_bulb
minecraft:silverfish_spawn_egg
minecraft:spruce_boat
minecraft:light_blue_terracotta
minecraft:decorated_pot
minecraft:acacia_boat
minecraft:dark_oak_boat
minecraft:iron_ore
minecraft:snort_pottery_sherd
minecraft:written_book
minecraft:leather
minecraft:kelp
minecraft:gold_nugget
minecraft:short_dry_grass
minecraft:hard_brown_stained_glass_pane
minecraft:globe_banner_pattern
minecraft:brick
minecraft:netherite_ingot
minecraft:netherite_upgrade_smithing_template
minecraft:lit_pumpkin
minecraft:hard_lime_stained_glass_pane
minecraft:sugar_cane
minecraft:paper
minecraft:granite
minecraft:magenta_shulker_box
minecraft:element_23
minecraft:heartbreak_pottery_sherd
minecraft:yellow_terracotta
minecraft:tadpole_spawn_egg
minecraft:coral
minecraft:dead_tube_coral_fan
minecraft:book
minecraft:gray_concrete_powder
minecraft:trident
minecraft:dead_horn_coral
minecraft:slime_ball
minecraft:chest_minecart
minecraft:cow_spawn_egg
minecraft:egg
minecraft:fishing_rod
minecraft:bogged_spawn_egg
minecraft:clock
minecraft:jungle_sapling
minecraft:andesite_stairs
minecraft:reserved6
minecraft:ocelot_spawn_egg
minecraft:glowstone_dust
minecraft:black_dye
minecraft:miner_pottery_sherd
minecraft:green_dye
minecraft:shulker_box
minecraft:red_candle_cake
minecraft:netherite_nautilus_armor
minecraft:dandelion
minecraft:deny
minecraft:deepslate_brick_wall
minecraft:bee_spawn_egg
minecraft:cyan_shulker_box
minecraft:mud_brick_slab
minecraft:brown_dye
minecraft:pale_oak_wall_sign
minecraft:polished_diorite
minecraft:cut_red_sandstone_slab
minecraft:frame
minecraft:blue_dye
minecraft:item.cake
minecraft:exposed_copper_bars
minecraft:purple_dye
minecraft:snout_armor_trim_smithing_template
minecraft:purpur_slab
minecraft:music_disc_13
minecraft:cyan_dye
minecraft:orange_wool
minecraft:andesite_double_slab
minecraft:blaze_rod
minecraft:oak_planks
minecraft:sticky_piston_arm_collision
minecraft:pale_oak_leaves
minecraft:light_gray_dye
minecraft:gray_dye
minecraft:quartz_double_slab
minecraft:element_41
minecraft:piglin_brute_spawn_egg
minecraft:rabbit_spawn_egg
minecraft:pink_dye
minecraft:lime_dye
minecraft:light_block_0
minecraft:blast_furnace
minecraft:yellow_dye
minecraft:light_blue_dye
minecraft:turtle_egg
minecraft:dirt_with_roots
minecraft:mangrove_door
minecraft:birch_slab
minecraft:stained_glass
minecraft:blue_stained_glass_pane
minecraft:bed
minecraft:waxed_copper_bulb
minecraft:orange_dye
minecraft:birch_leaves
minecraft:cyan_stained_glass
minecraft:yellow_candle
minecraft:camel_spawn_egg
minecraft:white_dye
minecraft:dune_armor_trim_smithing_template
minecraft:item.flower_pot
minecraft:waxed_exposed_chiseled_copper
minecraft:bone_meal
minecraft:turtle_helmet
minecraft:ink_sac
minecraft:compound_creator
minecraft:stripped_crimson_stem
minecraft:camera
minecraft:chorus_fruit
minecraft:pale_moss_carpet
minecraft:medium_amethyst_bud
minecraft:lapis_lazuli
minecraft:waxed_copper_grate
minecraft:suspicious_stew
minecraft:sugar
minecraft:oak_slab
minecraft:purple_stained_glass
minecraft:name_tag
minecraft:creeper_spawn_egg
minecraft:cake
minecraft:netherite_chestplate
minecraft:blue_candle
minecraft:orange_concrete_powder
minecraft:repeater
minecraft:beacon
minecraft:drowned_spawn_egg
minecraft:nether_brick_double_slab
minecraft:polished_andesite_stairs
minecraft:filled_map
minecraft:shears
minecraft:hard_red_stained_glass
minecraft:ender_pearl
minecraft:smooth_stone_double_slab
minecraft:white_carpet
minecraft:ghast_tear
minecraft:element_44
minecraft:glass_bottle
minecraft:cooked_mutton
minecraft:fermented_spider_eye
minecraft:blaze_powder
minecraft:tall_dry_grass
minecraft:magma_cream
minecraft:light_gray_terracotta
minecraft:diamond_nautilus_armor
minecraft:jigsaw
minecraft:brewing_stand
minecraft:copper_nautilus_armor
minecraft:cauldron
minecraft:chicken_spawn_egg
minecraft:pig_spawn_egg
minecraft:mooshroom_spawn_egg
minecraft:brown_stained_glass_pane
minecraft:andesite
minecraft:rib_armor_trim_smithing_template
minecraft:bamboo_hanging_sign
minecraft:fence_gate
minecraft:skeleton_spawn_egg
minecraft:colored_torch_rg
minecraft:bleach
minecraft:spider_spawn_egg
minecraft:hard_red_stained_glass_pane
minecraft:zombie_spawn_egg
minecraft:villager_spawn_egg
minecraft:composter
minecraft:squid_spawn_egg
minecraft:purple_carpet
minecraft:bat_spawn_egg
minecraft:ghast_spawn_egg
minecraft:warped_fungus_on_a_stick
minecraft:chiseled_nether_bricks
minecraft:magma_cube_spawn_egg
minecraft:mob_spawner
minecraft:warped_sign
minecraft:soul_campfire
minecraft:cave_spider_spawn_egg
minecraft:guardian_spawn_egg
minecraft:red_nether_brick_slab
minecraft:husk_spawn_egg
minecraft:lime_concrete_powder
minecraft:chalkboard
minecraft:piglin_spawn_egg
minecraft:white_concrete
minecraft:exposed_copper_door
minecraft:weeping_vines
minecraft:pink_candle_cake
minecraft:wither_skeleton_spawn_egg
minecraft:brewer_pottery_sherd
minecraft:spruce_sign
minecraft:donkey_spawn_egg
minecraft:creaking_spawn_egg
minecraft:stripped_spruce_wood
minecraft:double_plant
minecraft:mule_spawn_egg
minecraft:spruce_slab
minecraft:element_109
minecraft:skeleton_horse_spawn_egg
minecraft:flowering_azalea
minecraft:light_block_14
minecraft:netherite_pickaxe
minecraft:pink_terracotta
minecraft:jukebox
minecraft:zombie_horse_spawn_egg
minecraft:bamboo_door
minecraft:bamboo_slab
minecraft:npc_spawn_egg
minecraft:breeze_spawn_egg
minecraft:pale_oak_hanging_sign
minecraft:end_stone
minecraft:llama_spawn_egg
minecraft:spruce_wall_sign
minecraft:vex_spawn_egg
minecraft:spruce_sapling
minecraft:twisting_vines
minecraft:warped_trapdoor
minecraft:daylight_detector_inverted
minecraft:warden_spawn_egg
minecraft:magenta_concrete
minecraft:zombie_villager_spawn_egg
minecraft:diorite_double_slab
minecraft:cod_spawn_egg
minecraft:red_tulip
minecraft:orange_concrete
minecraft:standing_sign
minecraft:host_armor_trim_smithing_template
minecraft:warped_slab
minecraft:salmon_spawn_egg
minecraft:normal_stone_double_slab
minecraft:dolphin_spawn_egg
minecraft:yellow_carpet
minecraft:turtle_spawn_egg
minecraft:double_cut_copper_slab
minecraft:phantom_spawn_egg
minecraft:element_constructor
minecraft:item.acacia_door
minecraft:oxidized_cut_copper_slab
minecraft:cat_spawn_egg
minecraft:light_gray_wool
minecraft:cherry_fence
minecraft:purpur_double_slab
minecraft:quartz
minecraft:fox_spawn_egg
minecraft:spruce_log
minecraft:cobblestone_wall
minecraft:carrot_on_a_stick
minecraft:acacia_wood
minecraft:wandering_trader_spawn_egg
minecraft:spruce_hanging_sign
minecraft:hoglin_spawn_egg
minecraft:magenta_concrete_powder
minecraft:warped_fence_gate
minecraft:plenty_pottery_sherd
minecraft:infested_cobblestone
minecraft:waxed_weathered_copper_bulb
minecraft:sniffer_spawn_egg
minecraft:oxidized_cut_copper
minecraft:goat_spawn_egg
minecraft:prismarine_slab
minecraft:ender_dragon_spawn_egg
minecraft:wither_spawn_egg
minecraft:magenta_harness
minecraft:blue_stained_glass
minecraft:glow_ink_sac
minecraft:copper_ingot
minecraft:orange_candle_cake
minecraft:copper_block
minecraft:cut_copper
minecraft:dark_oak_pressure_plate
minecraft:seagrass
minecraft:prismarine_shard
minecraft:cut_copper_stairs
minecraft:weathered_cut_copper_slab
minecraft:double_stone_block_slab3
minecraft:mutton
minecraft:red_stained_glass
minecraft:sculk_vein
minecraft:waxed_cut_copper_slab
minecraft:infested_mossy_stone_bricks
minecraft:waxed_exposed_cut_copper_slab
minecraft:jungle_trapdoor
minecraft:fire_charge
minecraft:waxed_weathered_cut_copper_slab
minecraft:infested_cracked_stone_bricks
minecraft:waxed_oxidized_cut_copper_slab
minecraft:polished_andesite
minecraft:raw_copper
minecraft:pale_oak_stairs
minecraft:experience_bottle
minecraft:element_69
minecraft:writable_book
minecraft:bamboo_fence_gate
minecraft:copper_torch
minecraft:deepslate_brick_double_slab
minecraft:emerald
minecraft:dark_prismarine_double_slab
minecraft:copper_chain
minecraft:flower_pot
minecraft:empty_map
minecraft:exposed_chiseled_copper
minecraft:end_stone_brick_wall
minecraft:crimson_nylium
minecraft:firework_rocket
minecraft:element_102
minecraft:colored_torch_bp
minecraft:firework_star
minecraft:netherbrick
minecraft:dead_bubble_coral_wall_fan
minecraft:tnt_minecart
minecraft:polished_granite_slab
minecraft:stripped_acacia_wood
minecraft:hopper_minecart
minecraft:dragon_breath
minecraft:cobblestone
minecraft:hopper
minecraft:light_gray_harness
minecraft:rabbit_hide
minecraft:leather_horse_armor
minecraft:diamond_horse_armor
minecraft:music_disc_blocks
minecraft:music_disc_far
minecraft:music_disc_mellohi
minecraft:acacia_sign
minecraft:blue_terracotta
minecraft:info_update2
minecraft:prismarine_crystals
minecraft:lead
minecraft:chiseled_resin_bricks
minecraft:element_32
minecraft:brush
minecraft:armor_stand
minecraft:phantom_membrane
minecraft:spruce_door
minecraft:birch_hanging_sign
minecraft:birch_door
minecraft:yellow_harness
minecraft:granite_wall
minecraft:element_42
minecraft:acacia_door
minecraft:turtle_scute
minecraft:netherite_leggings
minecraft:dark_oak_door
minecraft:yellow_stained_glass_pane
minecraft:pale_oak_slab
minecraft:popped_chorus_fruit
minecraft:splash_potion
minecraft:shulker_shell
minecraft:mossy_cobblestone_wall
minecraft:light_blue_concrete
minecraft:chiseled_quartz_block
minecraft:pale_oak_wood
minecraft:redstone_block
minecraft:brain_coral
minecraft:banner
minecraft:mangrove_planks
minecraft:iron_nugget
minecraft:birch_sign
minecraft:coral_fan_dead
minecraft:cherry_shelf
minecraft:copper_axe
minecraft:dark_oak_sign
minecraft:flower_banner_pattern
minecraft:magenta_carpet
minecraft:frog_spawn_egg
minecraft:polished_diorite_stairs
minecraft:mojang_banner_pattern
minecraft:monster_egg
minecraft:cherry_button
minecraft:field_masoned_banner_pattern
minecraft:bordure_indented_banner_pattern
minecraft:purple_candle_cake
minecraft:short_grass
minecraft:orange_shulker_box
minecraft:potatoes
minecraft:piglin_banner_pattern
minecraft:purple_wool
minecraft:boat
minecraft:guster_banner_pattern
minecraft:moss_carpet
minecraft:netherite_horse_armor
minecraft:red_nether_brick
minecraft:honey_bottle
minecraft:stripped_warped_hyphae
minecraft:birch_shelf
minecraft:mangrove_sign
minecraft:blue_candle_cake
minecraft:element_22
minecraft:magma
minecraft:ominous_bottle
minecraft:compound
minecraft:stone_brick_slab
minecraft:ice_bomb
minecraft:medicine
minecraft:glow_stick
minecraft:element_83
minecraft:lodestone_compass
minecraft:quartz_ore
minecraft:netherite_shovel
minecraft:netherite_axe
minecraft:mossy_cobblestone_double_slab
minecraft:netherite_hoe
minecraft:mud
minecraft:netherite_helmet
minecraft:netherite_scrap
minecraft:quartz_slab
minecraft:crimson_sign
minecraft:concrete
minecraft:sponge
minecraft:crimson_door
minecraft:acacia_leaves
minecraft:horn_coral
minecraft:cartography_table
minecraft:nether_sprouts
minecraft:blackstone_slab
minecraft:polished_blackstone_slab
minecraft:cobbled_deepslate_slab
minecraft:scrape_pottery_sherd
minecraft:polished_deepslate_slab
minecraft:deepslate_tile_slab
minecraft:amethyst_shard
minecraft:music_disc_otherside
minecraft:element_33
minecraft:howl_pottery_sherd
minecraft:birch_chest_boat
minecraft:smooth_red_sandstone_stairs
minecraft:magenta_candle
minecraft:goat_horn
minecraft:frog_spawn
minecraft:waxed_weathered_double_cut_copper_slab
minecraft:allay_spawn_egg
minecraft:mangrove_slab
minecraft:mangrove_propagule
minecraft:mangrove_roots
minecraft:muddy_mangrove_roots
minecraft:green_glazed_terracotta
minecraft:music_disc_5
minecraft:jungle_standing_sign
minecraft:disc_fragment_5
minecraft:candle_cake
minecraft:pink_glazed_terracotta
minecraft:mossy_stone_brick_slab
minecraft:blue_concrete
minecraft:jungle_chest_boat
minecraft:creaking_heart
minecraft:spruce_chest_boat
minecraft:white_concrete_powder
minecraft:acacia_chest_boat
minecraft:spire_armor_trim_smithing_template
minecraft:dark_oak_chest_boat
minecraft:info_update
minecraft:mangrove_chest_boat
minecraft:pale_oak_trapdoor
minecraft:sculk_shrieker
minecraft:recovery_compass
minecraft:tripwire_hook
minecraft:chest_boat
minecraft:echo_shard
minecraft:smooth_quartz
minecraft:birch_trapdoor
minecraft:trader_llama_spawn_egg
minecraft:sculk
minecraft:waxed_exposed_copper_chest
minecraft:cherry_boat
minecraft:lit_furnace
minecraft:cherry_door
minecraft:cherry_sapling
minecraft:cherry_hanging_sign
minecraft:cherry_slab
minecraft:bamboo_mosaic_slab
minecraft:bamboo_raft
minecraft:bamboo_chest_raft
minecraft:element_89
minecraft:oak_hanging_sign
minecraft:crimson_shelf
minecraft:quartz_stairs
minecraft:explorer_pottery_sherd
minecraft:jungle_hanging_sign
minecraft:acacia_hanging_sign
minecraft:dark_oak_hanging_sign
minecraft:polished_tuff
minecraft:crimson_hanging_sign
minecraft:brown_candle
minecraft:warped_hanging_sign
minecraft:waxed_oxidized_copper
minecraft:double_stone_block_slab
minecraft:archer_pottery_sherd
minecraft:stone_brick_double_slab
minecraft:blade_pottery_sherd
minecraft:danger_pottery_sherd
minecraft:flow_pottery_sherd
minecraft:friend_pottery_sherd
minecraft:guster_pottery_sherd
minecraft:pink_shulker_box
minecraft:heart_pottery_sherd
minecraft:sheaf_pottery_sherd
minecraft:fire_coral_block
minecraft:brick_double_slab
minecraft:ladder
minecraft:unlit_redstone_torch
minecraft:shelter_pottery_sherd
minecraft:sentry_armor_trim_smithing_template
minecraft:spruce_planks
minecraft:element_27
minecraft:wild_armor_trim_smithing_template
minecraft:ward_armor_trim_smithing_template
minecraft:waxed_copper_golem_statue
minecraft:chain_command_block
minecraft:gray_wool
minecraft:light_blue_stained_glass
minecraft:loom
minecraft:polished_deepslate_double_slab
minecraft:eye_armor_trim_smithing_template
minecraft:red_stained_glass_pane
minecraft:bamboo_block
minecraft:tide_armor_trim_smithing_template
minecraft:wayfinder_armor_trim_smithing_template
minecraft:red_carpet
minecraft:raiser_armor_trim_smithing_template
minecraft:bamboo_button
minecraft:element_118
minecraft:shaper_armor_trim_smithing_template
minecraft:element_4
minecraft:bolt_armor_trim_smithing_template
minecraft:wither_skeleton_skull
minecraft:music_disc_relic
minecraft:weathered_copper_golem_statue
minecraft:wool
minecraft:red_nether_brick_wall
minecraft:stone
minecraft:polished_granite
minecraft:green_stained_glass_pane
minecraft:light_block_10
minecraft:diorite
minecraft:element_11
minecraft:coarse_dirt
minecraft:cobblestone_double_slab
minecraft:skeleton_skull
minecraft:zombie_head
minecraft:yellow_shulker_box
minecraft:player_head
minecraft:cut_sandstone
minecraft:creeper_head
minecraft:dragon_head
minecraft:orange_stained_glass
minecraft:skull
minecraft:dark_oak_planks
minecraft:red_sand
minecraft:cracked_deepslate_tiles
minecraft:white_terracotta
minecraft:copper_nugget
minecraft:cracked_polished_blackstone_bricks
minecraft:orange_terracotta
minecraft:waxed_oxidized_copper_lantern
minecraft:lime_terracotta
minecraft:copper_horse_armor
minecraft:gray_terracotta
minecraft:smooth_red_sandstone_double_slab
minecraft:cyan_terracotta
minecraft:purple_terracotta
minecraft:green_terracotta
minecraft:red_terracotta
minecraft:black_terracotta
minecraft:fletching_table
minecraft:brown_carpet
minecraft:stained_hardened_clay
minecraft:armadillo_scute
minecraft:armadillo_spawn_egg
minecraft:wolf_armor
minecraft:deepslate_coal_ore
minecraft:element_9
minecraft:tuff_slab
minecraft:waxed_oxidized_cut_copper
minecraft:polished_tuff_slab
minecraft:light_blue_wool
minecraft:oxidized_chiseled_copper
minecraft:birch_planks
minecraft:mossy_stone_brick_wall
minecraft:tuff_brick_slab
minecraft:copper_door
minecraft:oxidized_copper_door
minecraft:warped_nylium
minecraft:waxed_copper_door
minecraft:stone_block_slab4
minecraft:waterlily
minecraft:waxed_exposed_copper_door
minecraft:pale_oak_boat
minecraft:smooth_basalt
minecraft:pale_oak_sign
minecraft:pale_oak_door
minecraft:green_carpet
minecraft:normal_stone_stairs
minecraft:resin_brick_slab
minecraft:double_stone_block_slab2
minecraft:resin_clump
minecraft:blue_egg
minecraft:conduit
minecraft:brown_egg
minecraft:black_harness
minecraft:blue_harness
minecraft:brown_harness
minecraft:enchanting_table
minecraft:cyan_harness
minecraft:gray_harness
minecraft:cut_red_sandstone
minecraft:acacia_fence
minecraft:light_blue_harness
minecraft:bubble_coral_block
minecraft:light_gray_stained_glass
minecraft:lime_harness
minecraft:orange_harness
minecraft:light_blue_candle
minecraft:pink_harness
minecraft:basalt
minecraft:purple_harness
minecraft:red_harness
minecraft:dark_oak_fence_gate
minecraft:white_harness
minecraft:shroomlight
minecraft:copper_golem_spawn_egg
minecraft:copper_shovel
minecraft:trip_wire
minecraft:copper_pickaxe
minecraft:brick_slab
minecraft:dead_horn_coral_fan
minecraft:cave_vines_body_with_berries
minecraft:sandstone_stairs
minecraft:copper_hoe
minecraft:spruce_standing_sign
minecraft:copper_chestplate
minecraft:sticky_piston
minecraft:black_wool
minecraft:brown_shulker_box
minecraft:double_stone_block_slab4
minecraft:waxed_oxidized_copper_grate
minecraft:tnt
minecraft:copper_leggings
minecraft:copper_boots
minecraft:prismarine_brick_double_slab
minecraft:element_24
minecraft:nautilus_spawn_egg
minecraft:zombie_nautilus_spawn_egg
minecraft:barrier
minecraft:frosted_ice
minecraft:parched_spawn_egg
minecraft:iron_nautilus_armor
minecraft:acacia_double_slab
minecraft:golden_nautilus_armor
minecraft:nether_brick_stairs
minecraft:white_wool
minecraft:magenta_wool
minecraft:yellow_wool
minecraft:lime_wool
minecraft:infested_chiseled_stone_bricks
minecraft:pink_wool
minecraft:stripped_warped_stem
minecraft:infested_stone_bricks
minecraft:cyan_wool
minecraft:element_18
minecraft:blue_wool
minecraft:cherry_double_slab
minecraft:brown_stained_glass
minecraft:element_29
minecraft:brown_wool
minecraft:red_wool
minecraft:dark_prismarine_stairs
minecraft:deepslate_brick_stairs
minecraft:orange_carpet
minecraft:bamboo_pressure_plate
minecraft:hard_black_stained_glass
minecraft:light_blue_carpet
minecraft:gray_carpet
minecraft:light_gray_carpet
minecraft:oak_log
minecraft:birch_log
minecraft:jungle_log
minecraft:log
minecraft:birch_fence
minecraft:structure_block
minecraft:jungle_fence
minecraft:dark_oak_fence
minecraft:element_53
minecraft:fence
minecraft:waxed_oxidized_double_cut_copper_slab
minecraft:oxidized_copper_golem_statue
minecraft:stone_bricks
minecraft:cracked_stone_bricks
minecraft:poppy
minecraft:chiseled_stone_bricks
minecraft:pink_concrete
minecraft:stonebrick
minecraft:tall_grass
minecraft:brain_coral_block
minecraft:horn_coral_block
minecraft:dead_tube_coral_block
minecraft:oxidized_copper_lantern
minecraft:dead_fire_coral_block
minecraft:suspicious_sand
minecraft:dead_horn_coral_block
minecraft:lit_blast_furnace
minecraft:bamboo_stairs
minecraft:coral_block
minecraft:sandstone_slab
minecraft:cobblestone_slab
minecraft:nether_brick_slab
minecraft:stone_block_slab
minecraft:leaves
minecraft:andesite_wall
minecraft:prismarine_brick_slab
minecraft:mossy_cobblestone_slab
minecraft:smooth_sandstone_slab
minecraft:stone_block_slab2
minecraft:leaves2
minecraft:smooth_red_sandstone_slab
minecraft:lectern
minecraft:dead_brain_coral
minecraft:polished_andesite_slab
minecraft:andesite_slab
minecraft:bubble_coral
minecraft:diorite_slab
minecraft:prismarine_bricks
minecraft:granite_slab
minecraft:spruce_leaves
minecraft:birch_standing_sign
minecraft:prismarine_wall
minecraft:chiseled_polished_blackstone
minecraft:stone_block_slab3
minecraft:normal_stone_slab
minecraft:cut_sandstone_slab
minecraft:element_16
minecraft:cyan_stained_glass_pane
minecraft:sandstone_double_slab
minecraft:red_sandstone_double_slab
minecraft:dark_oak_sapling
minecraft:prismarine_double_slab
minecraft:waxed_cut_copper_stairs
minecraft:red_nether_brick_double_slab
minecraft:fern
minecraft:end_stone_brick_double_slab
minecraft:polished_andesite_double_slab
minecraft:border_block
minecraft:polished_diorite_double_slab
minecraft:granite_double_slab
minecraft:element_10
minecraft:polished_granite_double_slab
minecraft:mossy_stone_brick_double_slab
minecraft:dead_fire_coral
minecraft:purple_stained_glass_pane
minecraft:smooth_quartz_double_slab
minecraft:cut_sandstone_double_slab
minecraft:dragon_egg
minecraft:cut_red_sandstone_double_slab
minecraft:sweet_berry_bush
minecraft:tube_coral_fan
minecraft:bubble_coral_fan
minecraft:nether_brick_wall
minecraft:horn_coral_fan
minecraft:tinted_glass
minecraft:large_amethyst_bud
minecraft:coral_fan
minecraft:dead_brain_coral_fan
minecraft:dead_bubble_coral_fan
minecraft:lily_of_the_valley
minecraft:polished_blackstone_button
minecraft:sea_pickle
minecraft:oak_sapling
minecraft:acacia_sapling
minecraft:sapling
minecraft:oak_leaves
minecraft:jungle_leaves
minecraft:dark_oak_leaves
minecraft:azalea_leaves
minecraft:soul_fire
minecraft:azalea_leaves_flowered
minecraft:sandstone
minecraft:chiseled_sandstone
minecraft:smooth_sandstone
minecraft:spruce_button
minecraft:red_sandstone
minecraft:chiseled_red_sandstone
minecraft:stripped_pale_oak_wood
minecraft:smooth_red_sandstone
minecraft:jungle_slab
minecraft:acacia_slab
minecraft:redstone_lamp
minecraft:dark_oak_slab
minecraft:crimson_roots
minecraft:warped_roots
minecraft:allium
minecraft:cornflower
minecraft:lime_concrete
minecraft:large_fern
minecraft:red_flower
minecraft:sunflower
minecraft:exposed_cut_copper
minecraft:lilac
minecraft:peony
minecraft:daylight_detector
minecraft:snow_layer
minecraft:red_nether_brick_stairs
minecraft:jungle_planks
minecraft:gray_stained_glass
minecraft:light_gray_shulker_box
minecraft:light_blue_concrete_powder
minecraft:acacia_planks
minecraft:quartz_block
minecraft:quartz_pillar
minecraft:deprecated_purpur_block_1
minecraft:element_77
minecraft:purpur_pillar
minecraft:deprecated_purpur_block_2
minecraft:sandstone_wall
minecraft:stone_brick_wall
minecraft:tube_coral
minecraft:fire_coral
minecraft:diamond_ore
minecraft:dead_tube_coral
minecraft:small_amethyst_bud
minecraft:dead_bubble_coral
minecraft:soul_soil
minecraft:acacia_pressure_plate
minecraft:tallgrass
minecraft:element_103
minecraft:brown_mushroom_block
minecraft:mushroom_stem
minecraft:dark_oak_log
minecraft:log2
minecraft:warped_fungus
minecraft:end_portal_frame
minecraft:pale_hanging_moss
minecraft:anvil
minecraft:big_dripleaf
minecraft:deprecated_anvil
minecraft:infested_stone
minecraft:prismarine
minecraft:leaf_litter
minecraft:dark_prismarine
minecraft:gray_concrete
minecraft:light_gray_concrete
minecraft:cyan_concrete
minecraft:purple_concrete
minecraft:element_56
minecraft:brown_concrete
minecraft:lime_candle
minecraft:green_concrete
minecraft:red_concrete
minecraft:jungle_wood
minecraft:black_concrete
minecraft:yellow_concrete_powder
minecraft:pink_concrete_powder
minecraft:music_disc_lava_chicken
minecraft:spruce_trapdoor
minecraft:firefly_bush
minecraft:light_gray_concrete_powder
minecraft:purple_concrete_powder
minecraft:blue_concrete_powder
minecraft:green_concrete_powder
minecraft:red_concrete_powder
minecraft:black_concrete_powder
minecraft:concrete_powder
minecraft:element_75
minecraft:white_stained_glass
minecraft:element_64
minecraft:magenta_stained_glass
minecraft:stripped_jungle_wood
minecraft:yellow_stained_glass
minecraft:item.hopper
minecraft:hard_magenta_stained_glass
minecraft:wood
minecraft:mud_brick_double_slab
minecraft:lime_stained_glass
minecraft:pink_stained_glass
minecraft:birch_button
minecraft:deepslate_redstone_ore
minecraft:reinforced_deepslate
minecraft:black_stained_glass
minecraft:orange_stained_glass_pane
minecraft:item.dark_oak_door
minecraft:light_block
minecraft:magenta_stained_glass_pane
minecraft:end_crystal
minecraft:light_blue_stained_glass_pane
minecraft:pink_stained_glass_pane
minecraft:black_stained_glass_pane
minecraft:undyed_shulker_box
minecraft:lime_shulker_box
minecraft:gray_shulker_box
minecraft:deepslate_diamond_ore
minecraft:purple_shulker_box
minecraft:blue_shulker_box
minecraft:green_shulker_box
minecraft:red_shulker_box
minecraft:red_sandstone_stairs
minecraft:carved_pumpkin
minecraft:black_shulker_box
minecraft:piston
minecraft:torchflower_crop
minecraft:bamboo
minecraft:observer
minecraft:scaffolding
minecraft:grindstone
minecraft:bell
minecraft:oak_wood
minecraft:birch_wood
minecraft:dark_oak_wood
minecraft:stripped_oak_wood
minecraft:stripped_birch_wood
minecraft:stripped_dark_oak_wood
minecraft:music_disc_creator
minecraft:music_disc_precipice
minecraft:music_disc_tears
minecraft:material_reducer
minecraft:lab_table
minecraft:chemistry_table
minecraft:hard_white_stained_glass
minecraft:packed_ice
minecraft:hard_orange_stained_glass
minecraft:cobbled_deepslate
minecraft:hard_light_blue_stained_glass
minecraft:hard_yellow_stained_glass
minecraft:hard_lime_stained_glass
minecraft:hard_gray_stained_glass
minecraft:hard_light_gray_stained_glass
minecraft:hard_cyan_stained_glass
minecraft:crimson_double_slab
minecraft:hard_purple_stained_glass
minecraft:hard_blue_stained_glass
minecraft:hard_green_stained_glass
minecraft:element_84
minecraft:hard_stained_glass
minecraft:hard_white_stained_glass_pane
minecraft:hard_orange_stained_glass_pane
minecraft:hard_magenta_stained_glass_pane
minecraft:hard_light_blue_stained_glass_pane
minecraft:hard_yellow_stained_glass_pane
minecraft:hard_pink_stained_glass_pane
minecraft:carrots
minecraft:hard_gray_stained_glass_pane
minecraft:hard_light_gray_stained_glass_pane
minecraft:hard_purple_stained_glass_pane
minecraft:hard_blue_stained_glass_pane
minecraft:hard_black_stained_glass_pane
minecraft:hard_stained_glass_pane
minecraft:gravel
minecraft:colored_torch_red
minecraft:chiseled_tuff
minecraft:colored_torch_green
minecraft:light_block_1
minecraft:mangrove_shelf
minecraft:light_block_3
minecraft:light_block_4
minecraft:gray_candle_cake
minecraft:light_block_5
minecraft:light_block_6
minecraft:moss_block
minecraft:lightning_rod
minecraft:light_block_7
minecraft:deepslate_tile_double_slab
minecraft:light_block_8
minecraft:light_block_9
minecraft:waxed_oxidized_copper_bars
minecraft:light_block_11
minecraft:gold_block
minecraft:light_block_12
minecraft:light_block_13
minecraft:slime
minecraft:pumpkin
minecraft:crimson_slab
minecraft:candle
minecraft:orange_candle
minecraft:fire
minecraft:pink_candle
minecraft:gray_candle
minecraft:black_candle_cake
minecraft:light_gray_candle
minecraft:cyan_candle
minecraft:purple_candle
minecraft:red_candle
minecraft:polished_deepslate_wall
minecraft:black_candle
minecraft:element_0
minecraft:element_1
minecraft:element_3
minecraft:element_5
minecraft:element_6
minecraft:diamond_block
minecraft:element_7
minecraft:element_8
minecraft:element_12
minecraft:element_14
minecraft:pale_oak_standing_sign
minecraft:client_request_placeholder_block
minecraft:element_17
minecraft:element_19
minecraft:pearlescent_froglight
minecraft:element_20
minecraft:element_21
minecraft:element_25
minecraft:element_26
minecraft:element_28
minecraft:element_30
minecraft:element_31
minecraft:element_34
minecraft:bamboo_double_slab
minecraft:element_35
minecraft:element_36
minecraft:element_37
minecraft:element_38
minecraft:element_39
minecraft:element_40
minecraft:element_45
minecraft:element_46
minecraft:element_47
minecraft:element_48
minecraft:soul_sand
minecraft:element_49
minecraft:element_54
minecraft:element_55
minecraft:crafting_table
minecraft:element_57
minecraft:element_58
minecraft:element_59
minecraft:element_60
minecraft:element_61
minecraft:element_63
minecraft:element_65
minecraft:element_66
minecraft:element_67
minecraft:element_70
minecraft:element_71
minecraft:element_72
minecraft:element_73
minecraft:cobbled_deepslate_wall
minecraft:element_76
minecraft:element_78
minecraft:crafter
minecraft:redstone_torch
minecraft:element_79
minecraft:weathered_copper_bars
minecraft:element_81
minecraft:exposed_lightning_rod
minecraft:element_82
minecraft:tuff_bricks
minecraft:element_85
minecraft:element_87
minecraft:element_88
minecraft:element_90
minecraft:element_91
minecraft:element_92
minecraft:element_93
minecraft:element_94
minecraft:element_95
minecraft:waxed_exposed_cut_copper_stairs
minecraft:element_96
minecraft:element_98
minecraft:cactus
minecraft:element_99
minecraft:polished_blackstone_bricks
minecraft:element_100
minecraft:element_101
minecraft:element_105
minecraft:element_106
minecraft:element_107
minecraft:element_108
minecraft:element_110
minecraft:element_111
minecraft:element_112
minecraft:warped_button
minecraft:element_113
minecraft:birch_stairs
minecraft:element_114
minecraft:element_115
minecraft:nether_wart_block
minecraft:element_116
minecraft:element_117
minecraft:netherite_block
minecraft:crying_obsidian
minecraft:dye
minecraft:banner_pattern
minecraft:spawn_egg
minecraft:glow_berries
minecraft:polished_basalt
minecraft:nether_gold_ore
minecraft:waxed_weathered_copper_chain
minecraft:waxed_weathered_copper_chest
minecraft:item.warped_door
minecraft:mangrove_trapdoor
minecraft:piston_arm_collision
minecraft:waxed_oxidized_chiseled_copper
minecraft:dark_oak_button
minecraft:deepslate_copper_ore
minecraft:target
minecraft:blackstone_double_slab
minecraft:jungle_button
minecraft:pale_oak_fence_gate
minecraft:cherry_pressure_plate
minecraft:crimson_wall_sign
minecraft:cobbled_deepslate_stairs
minecraft:item.glow_frame
minecraft:hanging_roots
minecraft:waxed_exposed_copper_chain
minecraft:calcite
minecraft:pale_oak_pressure_plate
minecraft:stripped_dark_oak_log
minecraft:lime_glazed_terracotta
minecraft:trapdoor
minecraft:cactus_flower
minecraft:bamboo_planks
minecraft:mossy_cobblestone
minecraft:deepslate
minecraft:warped_standing_sign
minecraft:polished_blackstone_brick_wall
minecraft:pitcher_crop
minecraft:warped_pressure_plate
minecraft:oak_stairs
minecraft:end_bricks
minecraft:smooth_sandstone_stairs
minecraft:packed_mud
minecraft:light_blue_candle_cake
minecraft:oxidized_lightning_rod
minecraft:amethyst_block
minecraft:chiseled_bookshelf
minecraft:weathered_chiseled_copper
minecraft:iron_trapdoor
minecraft:waxed_weathered_chiseled_copper
minecraft:noteblock
minecraft:mangrove_log
minecraft:torchflower
minecraft:copper_grate
minecraft:powered_comparator
minecraft:warped_wall_sign
minecraft:open_eyeblossom
minecraft:pale_oak_sapling
minecraft:mangrove_double_slab
minecraft:waxed_exposed_copper_grate
minecraft:oxidized_double_cut_copper_slab
minecraft:waxed_copper_bars
minecraft:stone_button
minecraft:jungle_shelf
minecraft:exposed_double_cut_copper_slab
minecraft:blue_glazed_terracotta
minecraft:bamboo_fence
minecraft:hardened_clay
minecraft:stripped_jungle_log
minecraft:polished_blackstone_double_slab
minecraft:hard_glass_pane
minecraft:tuff_brick_wall
minecraft:polished_blackstone_brick_double_slab
minecraft:waxed_exposed_copper
minecraft:waxed_weathered_copper
minecraft:resin_brick_double_slab
minecraft:cyan_candle_cake
minecraft:polished_tuff_wall
minecraft:mud_brick_wall
minecraft:honey_block
minecraft:dripstone_block
minecraft:cherry_trapdoor
minecraft:gold_ore
minecraft:stonecutter
minecraft:dried_ghast
minecraft:warped_planks
minecraft:golden_rail
minecraft:invisible_bedrock
minecraft:oxidized_copper_bulb
minecraft:deepslate_tile_stairs
minecraft:oxidized_copper_bars
minecraft:orange_glazed_terracotta
minecraft:emerald_block
minecraft:heavy_weighted_pressure_plate
minecraft:underwater_torch
minecraft:wall_banner
minecraft:spruce_double_slab
minecraft:ochre_froglight
minecraft:cherry_stairs
minecraft:tuff_wall
minecraft:glowingobsidian
minecraft:brown_mushroom
minecraft:brown_glazed_terracotta
minecraft:exposed_copper_lantern
minecraft:waxed_copper_trapdoor
minecraft:copper_trapdoor
minecraft:waxed_exposed_copper_bars
minecraft:spruce_shelf
minecraft:moving_block
minecraft:oxidized_copper
minecraft:copper_ore
minecraft:birch_pressure_plate
minecraft:polished_blackstone_brick_stairs
minecraft:jungle_pressure_plate
minecraft:green_candle_cake
minecraft:stripped_bamboo_block
minecraft:sculk_catalyst
minecraft:waxed_lightning_rod
minecraft:warped_shelf
minecraft:copper_bars
minecraft:oak_double_slab
minecraft:brown_candle_cake
minecraft:purpur_stairs
minecraft:acacia_wall_sign
minecraft:light_weighted_pressure_plate
minecraft:polished_blackstone
minecraft:mycelium
minecraft:pale_oak_planks
minecraft:stone_stairs
minecraft:warped_stairs
minecraft:weathered_copper_grate
minecraft:copper_chest
minecraft:item.wooden_door
minecraft:wooden_button
minecraft:pitcher_plant
minecraft:spruce_pressure_plate
minecraft:birch_fence_gate
minecraft:redstone_wire
minecraft:waxed_exposed_cut_copper
minecraft:lava
minecraft:waxed_weathered_copper_lantern
minecraft:item.crimson_door
minecraft:mangrove_pressure_plate
minecraft:small_dripleaf_block
minecraft:waxed_exposed_lightning_rod
minecraft:rail
minecraft:blackstone_wall
minecraft:mossy_cobblestone_stairs
minecraft:stripped_pale_oak_log
minecraft:detector_rail
minecraft:brain_coral_wall_fan
minecraft:darkoak_standing_sign
minecraft:waxed_exposed_copper_golem_statue
minecraft:red_glazed_terracotta
minecraft:waxed_oxidized_copper_chest
minecraft:waxed_oxidized_copper_chain
minecraft:bamboo_mosaic_double_slab
minecraft:structure_void
minecraft:acacia_button
minecraft:snow
minecraft:mangrove_standing_sign
minecraft:black_glazed_terracotta
minecraft:dark_oak_shelf
minecraft:lit_redstone_ore
minecraft:stripped_mangrove_wood
minecraft:bone_block
minecraft:lapis_block
minecraft:coal_ore
minecraft:bamboo_shelf
minecraft:redstone_ore
minecraft:waxed_copper_chest
minecraft:waxed_copper_chain
minecraft:nether_brick_fence
minecraft:pale_oak_button
minecraft:crimson_hyphae
minecraft:wildflowers
minecraft:polished_blackstone_stairs
minecraft:waxed_weathered_copper_grate
minecraft:ender_chest
minecraft:warped_double_slab
minecraft:jungle_wall_sign
minecraft:sculk_sensor
minecraft:oak_shelf
minecraft:diorite_stairs
minecraft:stripped_cherry_log
minecraft:crimson_button
minecraft:honeycomb_block
minecraft:blackstone
minecraft:chorus_flower
minecraft:cracked_nether_bricks
minecraft:powered_repeater
minecraft:deepslate_tiles
minecraft:red_mushroom
minecraft:gilded_blackstone
minecraft:exposed_cut_copper_stairs
minecraft:mangrove_stairs
minecraft:unknown
minecraft:yellow_candle_cake
minecraft:dropper
minecraft:jungle_stairs
minecraft:pink_petals
minecraft:infested_deepslate
minecraft:soul_torch
minecraft:podzol
minecraft:crimson_fence_gate
minecraft:deadbush
minecraft:waxed_weathered_copper_golem_statue
minecraft:item.wheat
minecraft:item.spruce_door
minecraft:suspicious_gravel
minecraft:brick_block
minecraft:waxed_weathered_copper_trapdoor
minecraft:stripped_birch_log
minecraft:cave_vines
minecraft:melon_stem
minecraft:crimson_planks
minecraft:waxed_weathered_cut_copper
minecraft:horn_coral_wall_fan
minecraft:waxed_oxidized_copper_trapdoor
minecraft:brick_stairs
minecraft:wall_sign
minecraft:waxed_oxidized_copper_golem_statue
minecraft:dark_oak_stairs
minecraft:birch_double_slab
minecraft:glass_pane
minecraft:chiseled_deepslate
minecraft:weathered_lightning_rod
minecraft:bamboo_trapdoor
minecraft:mangrove_wall_sign
minecraft:light_gray_candle_cake
minecraft:cherry_leaves
minecraft:darkoak_wall_sign
minecraft:cyan_glazed_terracotta
minecraft:chiseled_tuff_bricks
minecraft:cracked_deepslate_bricks
minecraft:fire_coral_wall_fan
minecraft:flowing_lava
minecraft:jungle_fence_gate
minecraft:resin_brick_wall
minecraft:exposed_copper_grate
minecraft:coal_block
minecraft:exposed_copper_chest
minecraft:exposed_copper_chain
minecraft:waxed_double_cut_copper_slab
minecraft:item.kelp
minecraft:chorus_plant
minecraft:water
minecraft:chemical_heat
minecraft:mud_brick_stairs
minecraft:unpowered_repeater
minecraft:white_glazed_terracotta
minecraft:acacia_trapdoor
minecraft:weathered_copper_chest
minecraft:weathered_copper_chain
minecraft:glow_lichen
minecraft:pale_moss_block
minecraft:soul_lantern
minecraft:bee_nest
minecraft:bubble_column
minecraft:calibrated_sculk_sensor
minecraft:stripped_acacia_log
minecraft:cobbled_deepslate_double_slab
minecraft:warped_fence
minecraft:cherry_standing_sign
minecraft:pale_oak_shelf
minecraft:waxed_exposed_copper_trapdoor
minecraft:mossy_stone_brick_stairs
minecraft:waxed_copper
minecraft:end_rod
minecraft:crimson_stem
minecraft:tuff_brick_double_slab
minecraft:warped_hyphae
minecraft:resin_bricks
minecraft:tuff_stairs
minecraft:grass_block
minecraft:item.reeds
minecraft:pale_oak_log
minecraft:deepslate_gold_ore
minecraft:item.camera
minecraft:vault
minecraft:beehive
minecraft:item.jungle_door
minecraft:glass
minecraft:wither_rose
minecraft:waxed_weathered_cut_copper_stairs
minecraft:bamboo_mosaic_stairs
minecraft:polished_blackstone_pressure_plate
minecraft:acacia_standing_sign
minecraft:tuff_brick_stairs
minecraft:exposed_copper_bulb
minecraft:crimson_stairs
minecraft:stripped_spruce_log
minecraft:waxed_oxidized_copper_bulb
minecraft:pumpkin_stem
minecraft:deepslate_emerald_ore
minecraft:quartz_bricks
minecraft:unpowered_comparator
minecraft:end_brick_stairs
minecraft:weathered_copper_lantern
minecraft:item.nether_sprouts
minecraft:verdant_froglight
minecraft:resin_block
minecraft:warped_stem
minecraft:stripped_crimson_hyphae
minecraft:cocoa
minecraft:lever
minecraft:weathered_copper_trapdoor
minecraft:mangrove_fence
minecraft:oxidized_copper_grate
minecraft:ice
minecraft:item.bed
minecraft:web
minecraft:oxidized_copper_chest
minecraft:polished_blackstone_wall
minecraft:waxed_exposed_double_cut_copper_slab
minecraft:bubble_coral_wall_fan
minecraft:azalea
minecraft:mud_bricks
minecraft:birch_wall_sign
minecraft:bamboo_wall_sign
minecraft:bush
minecraft:bamboo_sapling
minecraft:standing_banner
minecraft:budding_amethyst
minecraft:jungle_double_slab
minecraft:purple_glazed_terracotta
minecraft:weathered_cut_copper
minecraft:bedrock
minecraft:dried_kelp_block
minecraft:blackstone_stairs
minecraft:blue_ice
minecraft:dead_horn_coral_wall_fan
minecraft:weathered_double_cut_copper_slab
minecraft:netherrack
minecraft:mangrove_button
minecraft:waxed_oxidized_lightning_rod
minecraft:allow
minecraft:item.birch_door
minecraft:cherry_wood
minecraft:bamboo_standing_sign
minecraft:cherry_log
minecraft:prismarine_stairs
minecraft:polished_tuff_stairs
minecraft:nether_brick
minecraft:deepslate_iron_ore
minecraft:waxed_cut_copper
minecraft:iron_chain
minecraft:spore_blossom
minecraft:crimson_standing_sign
minecraft:emerald_ore
minecraft:pointed_dripstone
minecraft:netherreactor
minecraft:exposed_copper_golem_statue
minecraft:item.cauldron
minecraft:cave_vines_head_with_berries
minecraft:dark_oak_trapdoor
minecraft:item.brewing_stand
minecraft:weathered_copper_bulb
minecraft:end_portal
minecraft:acacia_fence_gate
minecraft:lit_smoker
minecraft:lapis_ore
minecraft:waxed_copper_lantern
minecraft:repeating_command_block
minecraft:cherry_planks
minecraft:polished_deepslate
minecraft:tuff_double_slab
minecraft:furnace
minecraft:amethyst_cluster
minecraft:waxed_chiseled_copper
minecraft:crimson_fence
minecraft:dispenser
minecraft:item.soul_campfire
minecraft:wooden_pressure_plate
minecraft:lime_candle_cake
minecraft:trial_spawner
minecraft:grass_path
minecraft:waxed_weathered_lightning_rod
minecraft:weathered_copper
minecraft:pale_oak_double_slab
minecraft:cherry_fence_gate
minecraft:gray_glazed_terracotta
minecraft:bamboo_mosaic
minecraft:raw_iron_block
minecraft:iron_block
minecraft:stripped_mangrove_log
minecraft:copper_lantern
minecraft:tube_coral_wall_fan
```

</details>

## Notes

- Permission labels are mapped from numeric levels (0-4).
- Flags are shown as raw numeric values from command metadata.
- Dynamic enum lists may be empty in static data because some values are runtime-provided.
