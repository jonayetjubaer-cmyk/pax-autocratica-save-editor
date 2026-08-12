# Pax Autocratica Save Editor

Unofficial, binary-only Windows save editor for **Pax Autocratica**.

> This is a public distribution repository. The application is proprietary and
> closed source. Source code is not included or licensed.

## Download

Download the current validation build from the
[GitHub Releases page](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/tag/v0.3.0-beta.1).

Direct beta download:
[PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/download/v0.3.0-beta.1/PaxSaveEditor.exe)

> **Validation status:** v0.2.0 wrote valid database records but targeted the
> wrong resource/health layers and allowed an unsafe credit amount. Use the
> v0.3 beta validation build for build `0.195.x`; verify changes in-game and keep
> the automatic backup.

## Features

- Edit credits / Starbucks within the game's safe integer range.
- Edit the three live home-base storage resources: civil components, plant
  material, and metal.
- Edit persisted current health; derived shield is shown read-only.
- Edit stackable crafting materials, components, trade goods, seeds, and
  capture ammunition.
- Add missing stackable resources from identifiers verified against the
  installed game metadata.
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
