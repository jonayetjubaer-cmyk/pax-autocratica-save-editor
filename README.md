# Pax Autocratica Save Editor

Unofficial, binary-only Windows save editor for **Pax Autocratica**.

> This is a public distribution repository. The application is proprietary and
> closed source. Source code is not included or licensed.

## Download

### Latest beta: v0.5.0-beta.5

[Download PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/download/v0.5.0-beta.5/PaxSaveEditor.exe)

This beta fixes civil components, plant material, and metal disappearing from
the editor after Pax consumes its one-time resource transfer queue. The editor
now reads and writes the persistent inventory records used by the game.

### Stable: v0.3.0

Download the current stable build from the
[latest stable release](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest).

Direct stable download:
[PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest/download/PaxSaveEditor.exe)

> **Compatibility:** v0.3.0 was confirmed in-game with Pax Autocratica build
> `0.195.x`. v0.5.0-beta.5 has been tested against both pre-transfer and
> post-transfer saves, including the current player save that exposed the
> missing-storage problem. v0.2.0 must not be used.

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
- Edit persistent soldier combat and work stats, level, health, needs, morale,
  hunger, fatigue, and recovery values.
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
6. Open **Soldiers** to edit, heal, or duplicate home-station soldiers.
7. Open **Add items** to add verified weapons or consumables.

Backups are stored under:

```text
%LOCALAPPDATA%\PaxSaveEditor\Backups
```

## Requirements and warnings

- Windows 10 or Windows 11, x64.
- The executable is self-contained; no separate .NET installation is required.
- The executable is currently unsigned. Windows SmartScreen may display an
  unrecognized-app warning. Verify its SHA-256 checksum against
  [SHA256SUMS.txt](SHA256SUMS.txt) before running it.
- Editing a save can affect progression or achievements. Keep backups.
- Steam Cloud may synchronize the edited file when the game starts again.

## License

The application is proprietary freeware. You may download, install, and run the
official unmodified executable for personal, non-commercial use. You may not
redistribute, modify, decompile, reverse engineer, sublicense, or sell it.
See [LICENSE.txt](LICENSE.txt) for the complete terms.

Pax Autocratica and its assets are trademarks of their respective owners. This
project is not affiliated with or endorsed by the game's developer or publisher.
