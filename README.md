# MusicBrainz Picard Scripts

Custom **MusicBrainz Picard** tagging and file naming scripts designed for music collectors and music hoarders.

These scripts are intended for **MusicBrainz Picard 2.13.x** and are designed to keep album titles, original release years, reissue years, edition information, and multi-disc albums organized consistently.

## Tagger Scripts

The Tagger Scripts modify the **Album** tag and related year fields.

They use MusicBrainz Picard's original release date and specific release date to distinguish the original album from later reissues or editions.

### Album Edition Year First

Places the release year **before** the edition information.

Examples:

- `Slipknot [2009 10th Anniversary Edition]`
- `Killswitch Engage [2005 Remastered]`
- `Jesu [2022 Remastered Deluxe Edition]`
- `Isn't Anything [2012 Remastered]`
- `Born To Die [The Paradise Edition]`

### Album Edition Year Last

Places the release year **after** the edition information.

Examples:

- `Slipknot [10th Anniversary Edition 2009]`
- `Killswitch Engage [Remastered 2005]`
- `Jesu [Remastered Deluxe Edition 2022]`
- `Isn't Anything [Remastered 2012]`
- `Born To Die [The Paradise Edition]`

**Use only one of these Tagger Scripts at a time.** They provide two different formatting choices for the Album tag.

## File Naming Scripts

The File Naming Scripts determine how Picard organizes music files and folders.

The File Naming Scripts determine how Picard organizes music files and folders.

Artist - Album [Year]

Standard organization:

Artist/[Year] Album/01 - Title

For multi-disc releases, the disc number is included in the filename:

Artist/[Year] Album/1-01 - Title

Artist - Album [Year] - Multi-Disc Folders

Creates a separate folder for each disc:

Artist/[Year] Album/Disc 1/01 - Title

Artist/[Year] Album/Disc 2/01 - Title

This keeps each disc's tracks together in its own folder.

Artist - Album [Year] - No Multi-Disc Folders

Keeps all discs in the same album folder while including the disc number in the filename:

Artist - Album [Year]/1-01 - Title

Artist - Album [Year]/2-01 - Title

This version also provides more advanced handling of original release years, reissue years, and edition information in album folder names.

## Design Goals

These scripts were developed with a few simple goals:

- Preserve the **original release year** when available.
- Preserve the **specific release year** when it differs from the original.
- Keep edition information together and consistently formatted.
- Avoid duplicated edition information.
- Convert album edition parentheses to brackets where appropriate.
- Handle multi-disc releases in a predictable way.
- Keep file and folder names clean and easy to read.
- Provide different organization options so collectors can choose what works best for their libraries.

## Installation

### Tagger Scripts

On macOS:

1. Open **MusicBrainz Picard**.
2. Go to **MusicBrainz Picard → Preferences…**
3. Select **Scripting**.
4. Add a new tagging script.
5. Give it the same name as the script you're installing.
6. Copy the contents of the desired Tagger Script from this repository into the script editor.
7. Save the changes.
8. Enable the script.

**Use only one of the two Tagger Scripts at a time.**

### File Naming Scripts

On macOS:

1. Open **MusicBrainz Picard**.
2. Go to **MusicBrainz Picard → Preferences…**
3. Select **File Naming**.
4. Open the **File Naming Script Editor**.
5. Create a new script, or import the script as a plain-text file.
6. Give the script the same name as the file in this repository.
7. Save the changes.
8. Select the desired script as the **Active File Naming Script**.

Only one File Naming Script can be active at a time.

### Choosing a File Naming Script

- **Artist - Album [Year]** — standard organization with multi-disc numbers included in filenames.
- **Artist - Album [Year] - Multi-Disc Folders** — puts each disc in its own folder.
- **Artist - Album [Year] - No Multi-Disc Folders** — keeps multiple discs together in the album folder and includes the disc number in the filename.

## Version

**Version 1.0**

These scripts are a work in progress and may be updated as additional edge cases are discovered or improvements are suggested.

## Suggestions & Improvements

If you find an issue, encounter an unusual release that the scripts do not handle correctly, or have an idea for an improvement, feel free to open an **Issue** or suggest a change.

The goal is to make these scripts useful to as many MusicBrainz Picard users and music collectors as possible.

## Credits

Built and tested using **MusicBrainz Picard 2.13.x**.

MusicBrainz Picard: https://picard.musicbrainz.org/
