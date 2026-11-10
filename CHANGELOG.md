# Changelog

All notable changes to the Genesys Experience Unit Calculator are listed here.
The project uses [Semantic Versioning](https://semver.org/):

- **MAJOR** for changes to calculation logic or results
- **MINOR** for new features, inputs or capabilities
- **PATCH** for fixes, wording and styling

The current version is set in `APP_VERSION` in `index.html` and shown in the app header and footer. Bump it and add an entry here with every release.

## [2.0.0] - 2026-11-10

Calculation logic and results are unchanged from 1.0.0.

### Changed
- Renamed the tool from "Genesys AI Token Calculator" to **Genesys Experience Unit Calculator**, and relabeled tokens as Experience Units throughout the UI.
- Redesigned the interface: sticky header, summary tiles, card layout, cleaner tables and charts, empty states and a mobile-friendly layout.
- Pinned Chart.js (4.4.1) and the Tailwind CDN (3.4.16) to fixed versions.

### Added
- Light and dark themes with a header toggle.
- Version number shown in the app.
- README and this changelog.

## [1.0.0] - 2025-09-27

- Initial release as "Genesys AI Token Calculator" (build 202509271101).
