# Arena Mod 1.1

Welcome to the Arena of Life and Death.

Arena Mod adds 30 configurable combat challenges to Heroes of Might and Magic III ERA: 15 Standard Arenas and 15 unique Boss Arenas inspired by the Might and Magic series.

## Main features

- ![Attack](Assets/attr_attack.webp) Fight through 15 Standard Arenas ranging from early-game skirmishes to major army battles.
- ![Heroes III](Assets/logo_homm3_sod.webp) Challenge 15 Boss Arenas with individual combat mechanics and rewards.
- ![Grail](Assets/art_holy_grail.webp) Keep your army: creatures, Commander and Henchman are restored after every Arena battle.
- ![Spellbook](Assets/art_spellbinders_hat.webp) Configure Standard and Boss difficulty separately.
- ![ERA](Assets/logo_homm3_era.webp) Inspect requirements, rewards, scaling and a color-coded danger estimate directly in the Arena menu.

## Requirements and compatibility

- Heroes of Might and Magic III ERA 3.9.31 or newer is recommended.
- Game Enhancement Mod (GEM) supplies the shared interface functions used by Arena Mod.
- Advanced Classes Mod (ACM) is required only for Boss Arenas 16-30 and their ACM rewards.
- Difficulty Mod is optional and provides convenient access to the Arena configuration window.

## Entering the Arena

- Use the Arena button in the GEM town menu.
- Right-click the Marketplace while a hero is visiting the town.
- Visit an Arena object on the adventure map.

Choose a challenge and press **Fight**. Right-click an Arena entry to inspect its rules and current values. Right-click a Boss during combat to inspect its statistics.

## Difficulty settings

Standard Arenas and Boss Arenas store separate difficulty ranks.

Editable defaults are stored in `Lang/configuration.json`. Confirmed in-game settings are stored in `Runtime/arena config.ini` and take precedence. Delete the INI to apply changed JSON defaults again.

| Rank | Standard enemies | Standard growth | Boss HP | Boss damage | Boss Attack/Defense | Boss Speed |
|---|---:|---:|---:|---:|---:|---:|
| Peasant | 50% | 2 weeks later | 50% | 50% | -10 | -2 |
| Warrior | 100% | unchanged | 100% | 100% | unchanged | unchanged |
| Berserk | 150% | 1 week earlier | 150% | 150% | +10 | +2 |
| Chieftain | 200% | 2 weeks earlier | 200% | 200% | +20 | +3 |

Gold and experience rewards scale with the selected rank. Configured Boss effects such as summon amounts, spell damage and resurrection values scale from 50% to 200%.

The danger indicator compares the selected encounter with the current hero and army. It considers army Fight Value, Attack, Defense, hero level and learned secondary skills. It is an estimate rather than a guaranteed combat prediction.

## Arena rules

- Arena battles do not permanently consume the hero's army.
- Creatures, Commander and Henchman are restored after victory or defeat.
- Each Arena has its own costs, visit restrictions and hero-level requirements.
- Some Standard Arenas grow with game time when growth is enabled in their template.
- A battle is lost when its configured maximum duration is exceeded.
- Some encounters enrage after a configured number of combat rounds.
- Completed Boss Arenas are marked with a golden check mark for the current player.

## Boss Arenas

Boss Arenas 16-30 use individual scripts for mechanics such as additional attacks, regeneration, resurrection, summoning, damage limits, resistances, auras and phase changes. Arenas 26-30 enter a second phase at 50% health and announce it through the battle log, animation and sound.

Boss rewards improve ACM systems such as Commander attributes, combat and magic bonuses, class points and other long-term character progression.

## Creating a custom Arena

The files `Data/s/New_Arena_001.erm` through `New_Arena_030.erm` contain the encounter definitions. `Data/s/New_Arena_Template_001.off` is the reusable starting template.

1. Copy the template and rename it to the next Arena number.
2. Replace the Arena number consistently inside the copied file.
3. Configure the opposing army, requirements, rewards and battle settings.
4. Set the corresponding `Arena_X_Fight` value.
5. Add a menu slot if the new Arena extends the existing selection.

Visible interface text is stored in `Lang/arena_mod.json`. Dialogue layouts are packed in `Data/Arena.pac`, while interface graphics are stored in `Data/arena_mod.zip`.

## Changelog

### 2026-09-17 — Version 1.1

- Added separate, persistent difficulty settings for Standard and Boss Arenas.
- Improved Boss mechanics, stack handling and restoration after Arena combat.
- Added stack-specific Boss appearances with collision-free Arena DEF names.
- Set Peasant Boss health and damage scaling to 50% and corrected the displayed values.
- Restored Arena requirement and cost checks and reduced the battlefield package to the 16 backgrounds in use.

### 2026-08-23 — Version 1.0

- Added a Might and Magic VII-inspired configuration window with separately saved difficulty ranks for Standard Arenas 1-15 and Boss Arenas 16-30.
- Added `Lang/configuration.json` for editable Arena difficulty defaults.
- Standard Arena difficulty now changes enemy numbers and the week in which configured growth begins.
- Boss Arena difficulty now changes Boss health, damage, Attack, Defense and Speed.
- Fixed Boss effect values and Gold/experience rewards now scale with the selected difficulty.
- Reduced the base Gold and experience rewards of Boss Arenas 16-30 by 50%.
- Added a color-coded danger assessment based on army Fight Value and hero development.
- Added player-specific golden completion marks to the Boss selection page.
- Standardized Arena descriptions, hints, right-click information and difficulty overviews.
- Improved restoration of creatures, Commander, Henchman stack experience and equipped banner.
- Ensured summoned creatures and clones do not inherit mechanics intended only for original Boss stacks.
- Added reusable Boss mechanics for phase changes, resistances and round auras.
- Added stack-specific Boss battle DEF replacement during battle initialization without changing the underlying creature type or statistics.
- Added second phases to Boss Arenas 26-30.
- Reworked several encounters, including the Elite Archer, Robert the Wise, the Mountain Troll, Sir Charles Quixote, the Lich King and Xenofex.
- Arena 24 now contains the intended pair of Manticores; both share the full Boss mechanics and can inflict Paralysis.
- The Mountain Troll now gains +5 Speed after every resurrection and acts twice after its first resurrection.
- Corrected reward, speed, action-count, resurrection and combat-script inconsistencies.
- Removed calibration popups and obsolete dialogue resources; active dialogue text files are now packed in `Arena.pac`.

### 2025-12-01 — Version 0.8 Beta

- Added 15 Standard Arena challenges and 15 ACM Boss Battles.
- Added the Arena menu, detailed right-click information and custom-Arena template files.

## Feedback

For feedback, balance suggestions and bug reports, join the [HoMM 3.5 ERA Mods Discord server](https://discord.gg/hCTMfVq6w5).

Arena Mod by PerryR.
