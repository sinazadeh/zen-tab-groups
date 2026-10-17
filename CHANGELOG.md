# Changelog

Notable changes to Tab Groups. Versions match `version` in `theme.json`;
bump `updatedAt` along with it (to the current UTC time), as that's what
tells Sine an update is available. Once a version reaches `main`, it's
published as a GitHub release with its notes below (see
`.github/workflows/release.yml`).

## [Unreleased]

### Changed

- Every version has a GitHub release with its notes and a zip of
  `tab-groups.uc.js` and `tab-groups/` for fx-autoconfig, and new versions
  are released automatically once the version bump reaches `main`.

## [1.2.0] - 2026-10-17

### Added

- **Items in the tab menu** (`zen.sitegroups.tab-menu-items`, on by
  default), on the settings page and in Sine's options. Switched off, none
  of Tab Groups' items show when you right-click a tab, settings included;
  the header menu and Sine's settings button still open the settings page.

### Changed

- Tab Groups' items in the tab menu have ids (`context_zsg-*`), so other
  mods can recognize them: Zen Calmer Context Menu lists and hides them by
  id, since their labels change with the tab's site. They also have generic
  labels until the menu first opens, for anything that lists them before
  that.

## [1.1.0] - 2026-10-15

### Added

- **Backups.** The settings page gets a Backup card: **Save backup…**
  writes the sections and options to a `.json` file through Zen's save
  dialog, and **Restore from backup…** loads one back after asking,
  replacing the current sections and options. Files that aren't Tab Groups
  backups, and option values the page can't show, are ignored. Opened
  outside Zen, the page uses a normal download and file picker instead.
- A **Banking** collection idea: 100 US banks, card issuers, money apps and
  credit unions, each with its icon.

### Changed

- Idea cards show their first 6 sites, with "+N more" to see the rest, and
  collections with more than 12 sites fold to 10 chips plus "+N more".
- If a collection with an idea's name already exists, the idea offers to
  add only the sites it's missing instead of showing "Added".

## [1.0.3] - 2026-10-14

### Changed

- Marked as Zen-only (tested on Zen 1.23.2b) and AI-assisted, in the
  README and in `theme.json`, which Sine reads.

## [1.0.2] - 2026-10-14

### Fixed

- Sine now offers updates. It compares `updatedAt`, not the version, and
  1.0.1 kept 1.0.0's date, so copies of 1.0.0 were never offered it;
  `updatedAt` is now a full timestamp.

## [1.0.1] - 2026-10-13

### Changed

- The settings button on Tab Groups' card in Sine Mods opens the full
  settings page (sections, colors, collections, options) instead of Sine's
  options box, which only fits simple checkboxes and dropdowns.

## [1.0.0] - 2026-10-13

First release: tabs from the sites you choose move to the top of Zen's
sidebar, under colored, collapsible headers, with a settings page and Sine
support.
