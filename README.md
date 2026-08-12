# Pax Autocratica Save Editor

Unofficial, binary-only Windows save editor for **Pax Autocratica**.

> This is a public distribution repository. The application is proprietary and
> closed source. Source code is not included or licensed.

## Download

Download the latest `PaxSaveEditor.exe` from the
[GitHub Releases page](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest).

Direct latest download:
[PaxSaveEditor.exe](https://github.com/jonayetjubaer-cmyk/pax-autocratica-save-editor/releases/latest/download/PaxSaveEditor.exe)

## Features

- Edit credits, skill points, galaxy fuel, and galaxy food.
- Edit stackable crafting materials, components, trade goods, seeds, and
  capture ammunition.
- Add missing stackable resources from identifiers verified against the
  installed game metadata.
- Edit common character values such as name, level, XP, health, shield, and
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
