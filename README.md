# Pax Autocratica Save Editor

Unofficial, binary-only Windows save editor for **Pax Autocratica**.

> This is a public distribution repository. The application is proprietary and
> closed source. Source code is not included or licensed.

## Download

### Latest beta: v0.5.0-beta.10

[Download PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/download/v0.5.0-beta.10/PaxSaveEditor.exe)

Also available on [Nexus Mods](https://www.nexusmods.com/paxautocratica/mods/18).

This beta adds owned weapon and armor editing, soldier rarity promotion and
bulk roster edits, and clearer upgrade-material descriptions with a Blue+
ingredient quick set. It also includes the persistent base-storage fix.

### Stable: v0.3.0

Download the current stable build from the
[latest stable release](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest).

Direct stable download:
[PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest/download/PaxSaveEditor.exe)

> **Compatibility:** v0.3.0 was confirmed in-game with Pax Autocratica build
> `0.195.x`. The existing beta.10 integration harness passes against a local
> save copy, including equipment, soldier rarity, bulk edits, and pre-transfer
> and post-transfer storage checks. This does not establish compatibility with
> every newer Early Access build. v0.2.0 must not be used.

## Features

- Edit credits / Starbucks within the game's safe integer range.
- Edit persistent civil components, plant material, and metal before or after
  the game consumes its one-time transfer queue.
- Edit persisted current health; derived shield is shown read-only.
- Edit stackable crafting materials, components, trade goods, seeds, and
  capture ammunition.
- Add missing stackable resources from identifiers verified against the
  installed game metadata.
- Add verified weapons and consumables as valid inventory instances.
- Edit owned weapons and armor: rarity, equipment level, and verified
  slot-compatible bonus stats and their levels.
- Edit persistent soldier name, level, XP, needs, morale, wage, personal gold,
  and ten work stats. Combat HP, shield, and damage remain game-derived.
- Promote soldier rarity from White through Orange using the game's normal,
  elite, and boss thresholds while preserving existing affixes.
- Apply selected progression, needs/morale, economy, and work-stat groups to
  the complete roster, or bulk-promote its rarity, in one backup-first edit.
- Choose upgrade materials by verified family, rank/grade, and purpose, or
  stage the Blue+ upgrade-ingredient set before saving.
- Heal soldiers and clear persistent injury, disability, illness, fatigue, and
  breakdown conditions while preserving game sentinel states.
- Duplicate persistent soldiers with unique names and matching inventory
  identities.
- Edit common character values such as name, level, XP, current health, and
  difficulty.
- Inspect and edit advanced LiteDB documents as extended JSON.
- Create a timestamped backup before every write or restore.
- Refuse to write while Pax Autocratica is running.

## Usage

1. Close Pax Autocratica completely.
2. Download `PaxSaveEditor.exe` from Releases.
3. Run the executable. It automatically locates the newest save.
4. Open **Resources** to edit credits, skill points, and inventory quantities.
5. Select **Save resources & skill points**. A backup is created automatically.
6. Open **Soldiers** to edit, promote, heal, bulk-update, or duplicate home-station soldiers.
7. Open **Add items** to add verified weapons or consumables.
8. Open **Equipment** to edit owned weapon and armor rarity, level, and bonus stats.

Backups are stored under:

```text
%LOCALAPPDATA%\PaxSaveEditor\Backups
```

## Requirements and warnings

- Windows 10 or Windows 11, x64.
- The executable is self-contained; no separate .NET installation is required.
- The executable is currently unsigned. Windows SmartScreen may display an
  unrecognized-app warning. Verify its SHA-256 checksum against
  the `SHA256SUMS.txt` attached to your selected release before running it.
- Editing a save can affect progression or achievements. Keep backups.
- Steam Cloud may synchronize the edited file when the game starts again.

## License

The application is proprietary freeware. You may download, install, and run the
official unmodified executable for personal, non-commercial use. You may not
redistribute, modify, decompile, reverse engineer, sublicense, or sell it.
See [LICENSE.txt](LICENSE.txt) for the complete terms.

Pax Autocratica and its assets are trademarks of their respective owners. This
project is not affiliated with or endorsed by the game's developer or publisher.
