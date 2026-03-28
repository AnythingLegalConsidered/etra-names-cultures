# Changelog

All notable changes to **Etra: Names & Cultures** are documented here.

---

## v0.3.0 — Armonorican Language & Bug Fixes

### Added
- Full Armonorican language support (2 dialects: Armonorican, Ebiam)
- 134 unique Armonorican names (male, female, dynasty)
- Armonorican ruler titles for all government types
- Armonorican polity name translations

### Fixed
- **Snowball duplication bug** in ruler titles: file bloated from 8K to 31K lines due to cascading duplicates in the generation pipeline — reduced back to 8K
- **Armonorican trigger scope**: ruler-scope `?=` triggers didn't work for Armonorican; switched all to country-scope triggers (same pattern as other working languages)
- **Armonorican dialect detection**: switched from `culture.language` to `culture.dialect` for dialect-level checks
- **Armonorican fallback**: added `armonorican_language` as parent key so dialects fall back correctly
- **Gov type titles**: merged all government type titles into a single `country_flavor` block to avoid override conflicts
- **Ruler title loc**: separated ruler title localization into its own file to prevent cross-contamination with name localization

---

## v0.2.2 — Fantasy Ruler Titles

### Added
- **Ruler titles for all 7 languages** across 34 dialects
- 4 government types supported: Monarchy, Theocracy, Republic, Military Order
- 4 ranks per type: Empire, Kingdom, Duchy, County
- Per-language "Order of" naming for military orders (e.g., "Skarlakenorden", "L'Ordren Escarlain", "Ordo Scarlatinus")
- Translated polity names: 7+ countries translated into all 7 languages
- Game rule `etra_names_fantasy` to toggle the system

### Changed
- Polity names shortened across all languages for cleaner display
- Military order titles display `$NAME$` only (no rank prefix)

---

## v0.2.1 — Title Names System

### Added
- Title names system for dynamic country name display
- Country name construction rules per language
- Initial CHANGELOG and documentation

---

## v0.2.0 — Repository Restructure & Foundation

### Added
- **7 complete language files** with dialect definitions:
  - Torrent (17 dialects, 371 names)
  - Ardrainic (11 dialects, 215 names)
  - Armonorican (2 dialects, 134 names)
  - Hravevi (standalone, 129 names)
  - Moran (5 dialects, 121 names)
  - Sordrenic (4 dialects, 122 names)
  - Vulgar Moran (8 dialects, 131 names)
- **Character overrides** for Pantagrin and Rattolini dialects
- **Dynasty name additions** across all languages
- Culture definition files for Ardrainic, Moran, Sordrenic, Torrent, Vulgar Moran
- Mod metadata (`.metadata/metadata.json`)

### Changed
- Full repo restructure into `in_game/` and `main_menu/` Paradox mod layout
