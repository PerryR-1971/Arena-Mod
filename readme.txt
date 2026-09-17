ARENA MOD 1.1

Welcome to the Arena of Life and Death.

Arena Mod adds 30 configurable combat challenges to Heroes of Might and Magic III ERA: 15 Standard Arenas and 15 unique Boss Arenas inspired by the Might and Magic series.

----------------------------------------------------------------------------------------------------------------------
MAIN FEATURES
----------------------------------------------------------------------------------------------------------------------

- 15 Standard Arenas ranging from early-game skirmishes to major army battles.
- 15 Boss Arenas with individual combat mechanics and ACM rewards.
- Separate difficulty settings for Standard and Boss Arenas.
- Detailed right-click information and a color-coded danger estimate.
- Player-specific golden completion marks for defeated Boss Arenas.
- Full restoration of creatures, Commander and Henchman after Arena combat.
- A reusable ERM template for additional Arena encounters.

----------------------------------------------------------------------------------------------------------------------
REQUIREMENTS AND COMPATIBILITY
----------------------------------------------------------------------------------------------------------------------

- Heroes of Might and Magic III ERA 3.9.31 or newer is recommended.
- Game Enhancement Mod (GEM) supplies the shared interface functions used by Arena Mod.
- Advanced Classes Mod (ACM) is required only for Boss Arenas 16-30 and their rewards.
- Difficulty Mod is optional and provides convenient access to the Arena configuration window.

Editable Arena difficulty defaults are stored in Lang/configuration.json. Confirmed in-game settings are stored in Runtime/arena config.ini and take precedence. Delete the INI to apply changed JSON defaults again.

----------------------------------------------------------------------------------------------------------------------
HOW TO ENTER THE ARENA
----------------------------------------------------------------------------------------------------------------------

- Use the Arena button in the GEM town menu.
- Right-click the Marketplace while a hero is visiting the town.
- Visit an Arena object on the adventure map.

Choose a challenge and press Fight. Right-click an Arena entry to inspect its rules and current values. Right-click a Boss during combat to inspect its statistics.

----------------------------------------------------------------------------------------------------------------------
DIFFICULTY SETTINGS
----------------------------------------------------------------------------------------------------------------------

Standard Arenas and Boss Arenas store separate difficulty ranks.

Peasant:
- 50% Standard enemies and growth starts two weeks later.
- 50% Boss HP and damage, -10 Attack/Defense and -2 Speed.

Warrior:
- 100% Standard enemies and unchanged growth timing.
- 100% Boss HP and damage with unchanged combat statistics.

Berserk:
- 150% Standard enemies and growth starts one week earlier.
- 150% Boss HP and damage, +10 Attack/Defense and +2 Speed.

Chieftain:
- 200% Standard enemies and growth starts two weeks earlier.
- 200% Boss HP and damage, +20 Attack/Defense and +3 Speed.

Gold and experience rewards scale with the selected rank. Configured Boss effects such as summon amounts, spell damage and resurrection values scale from 50% to 200%.

The danger indicator considers army Fight Value, Attack, Defense, hero level and learned secondary skills. It is an estimate rather than a guaranteed combat prediction.

----------------------------------------------------------------------------------------------------------------------
ARENA RULES
----------------------------------------------------------------------------------------------------------------------

- Arena battles do not permanently consume the hero's army.
- Creatures, Commander and Henchman are restored after victory or defeat.
- Each Arena has its own costs, visit restrictions and hero-level requirements.
- Some Standard Arenas grow with game time when growth is enabled in their template.
- A battle is lost when its configured maximum duration is exceeded.
- Some encounters enrage after a configured number of combat rounds.

----------------------------------------------------------------------------------------------------------------------
BOSS ARENAS
----------------------------------------------------------------------------------------------------------------------

Boss Arenas 16-30 use individual scripts for mechanics such as additional attacks, regeneration, resurrection, summoning, damage limits, resistances, auras and phase changes. Arenas 26-30 enter a second phase at 50% health and announce it through the battle log, animation and sound.

Boss rewards improve ACM systems such as Commander attributes, combat and magic bonuses, class points and other long-term character progression.

----------------------------------------------------------------------------------------------------------------------
CREATING A CUSTOM ARENA
----------------------------------------------------------------------------------------------------------------------

Data\s\New_Arena_001.erm through New_Arena_030.erm contain the encounter definitions. Data\s\New_Arena_Template_001.off is the reusable starting template.

1. Copy the template and rename it to the next Arena number.
2. Replace the Arena number consistently inside the copied file.
3. Configure the opposing army, requirements, rewards and battle settings.
4. Set the corresponding Arena_X_Fight value.
5. Add a menu slot if the new Arena extends the existing selection.

Visible interface text is stored in Lang\arena_mod.json. Dialogue layouts are packed in Data\Arena.pac, while interface graphics are stored in Data\arena_mod.zip.

----------------------------------------------------------------------------------------------------------------------
LATEST CHANGELOG
----------------------------------------------------------------------------------------------------------------------

2026-09-17 - Version 1.1

- Added separate, persistent difficulty settings for Standard and Boss Arenas.
- Improved Boss mechanics, stack handling and restoration after Arena combat.
- Added stack-specific Boss appearances with collision-free Arena DEF names.
- Set Peasant Boss health and damage scaling to 50% and corrected the displayed values.
- Restored Arena requirement and cost checks and reduced the battlefield package to the 16 backgrounds in use.


2026-08-23 - Version 1.0

- Added separately saved difficulty ranks for Standard Arenas 1-15 and Boss Arenas 16-30.
- Added Lang/configuration.json for editable Arena difficulty defaults.
- Added difficulty scaling for enemies, growth timing, Boss statistics, Boss effects and rewards.
- Reduced the base Gold and experience rewards of Boss Arenas 16-30 by 50%.
- Added a color-coded danger assessment and player-specific Boss completion marks.
- Standardized Arena descriptions, hints and right-click information.
- Improved restoration of creatures, Commander, Henchman experience and equipped banner.
- Added reusable Boss phase, resistance and aura mechanics.
- Added stack-specific Boss battle DEF replacement during battle initialization without changing the underlying creature type or statistics.
- Added second phases to Boss Arenas 26-30.
- Reworked several Boss encounters and corrected combat-script inconsistencies.
- Arena 24 now contains two Manticores with the full Boss mechanics and Paralysis attacks.
- Moved additional visible text to the language file.


2025-12-01 - Version 0.8 Beta

- Added 15 Standard Arena challenges and 15 ACM Boss Battles.
- Added the Arena menu, detailed right-click information and custom-Arena template files.

----------------------------------------------------------------------------------------------------------------------
FEEDBACK
----------------------------------------------------------------------------------------------------------------------

For feedback, balance suggestions and bug reports, join the HoMM 3.5 ERA Mods Discord server:
https://discord.gg/hCTMfVq6w5

Arena Mod by PerryR.
