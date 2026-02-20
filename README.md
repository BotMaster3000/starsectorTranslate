# Starsector Translation Pack Workspace

This repository contains Starsector `data` files and language-specific translation deltas.

## Structure

- `data/`
  - Original/source game data files (reference base).
- `ger/data/`
  - German translation files.
  - This folder intentionally contains only files that differ from the base `data/`.

## How to Install a Language in the Game

The game reads files from the game `data` directory.  
To apply a translation, copy the language folder's `data` contents into the game's `data` folder and replace existing files.

### Example (German)

1. Locate your Starsector game directory (the one that contains `data/`).
2. Copy all files from this repository's `ger/data/` into the game's `data/`.
3. Overwrite/replace files when prompted.

## Important Notes

- Always keep a backup of your game `data/` folder before replacing files.
- The base `data/` folder in this repo is kept as reference and should not be overwritten here.
- Language folders are designed as patch/delta overlays; unchanged files are inherited from the game's original `data/`.

## Maintainer Notes

- `ger/data/` is intentionally delta-only (changed files only).
- `data/strings/descriptions.csv` requires cp1252-safe handling in tooling.
- Machine translation should preserve placeholders (`$...`, `%...`, `\\n`) and locked proper nouns.
- Avoid global `ae/oe/ue -> ä/ö/ü` replacements; apply targeted fixes to prevent false positives (e.g. `feuert`/`Abfeuern`).
