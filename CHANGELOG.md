# Changelog

All notable changes to the Genesys Experience Unit Calculator are listed here.
The project uses [Semantic Versioning](https://semver.org/):

- **MAJOR** for changes to calculation logic or results
- **MINOR** for new features, inputs or capabilities
- **PATCH** for fixes, wording and styling

The current version is set in `APP_VERSION` in `index.html` and shown in the app header and footer. Bump it and add an entry here with every release.

## [3.2.0] - 2026-11-10

### Added
- **Scenarios** button in the header to keep several estimates side by side:
  - **Save current** stores every input (prices, Voice Mix, Digital Mix, capabilities and the Distribution choice) under a name. Saving with an existing name asks before replacing it.
  - The saved list shows when each scenario was saved, its Total Experience Units and how many voice and digital interactions it has, with **Load**, **Rename**, **Export** and **Delete** for each one.
  - Saved scenarios are kept in this browser on this computer (no server or sign-in).
  - **Export** downloads a scenario as a small `.json` file to keep with customer notes or send to a colleague, and **Import from file** loads it back and adds it to the saved list.
- The header shows the name of the scenario that is loaded.

### Fixed
- Interaction names and call lengths that contain quotes or `<` now display correctly in the Voice and Digital Mix tables.

Calculations are unchanged.

## [3.1.0] - 2026-11-10

### Added
- **Download Summary** button in the header with two formats for the current estimate:
  - **PDF report**: a one-page printable summary opened in the print dialog (choose *Save as PDF*). It shows Total Experience Units, Estimated Cost, the totals for the other distribution, Experience Units, price and cost for each AI type, the Voice and Digital Mix, enabled capabilities and Unused Capacity.
  - **CSV spreadsheet**: the same information as a file for Excel or Google Sheets.
- The summary follows the Distribution currently chosen (Selected or Lowest Cost). Calculations are unchanged.

## [3.0.0] - 2026-11-10

Estimated Cost and the Lowest Cost results can change, because each AI type now has its own price.

### Removed
- The **AI Guide Creation** input. Its Experience Units no longer count toward Total Experience Units, Estimated Cost or the breakdown chart.

### Changed
- Replaced the single "Price per Experience Unit" with preset price fields, each defaulting to $1.00:
  - **Bot**: Voice Bot and Digital Bot
  - **VA**: Virtual Agent
  - **AVA**: Agentic AI
- Estimated Cost now multiplies each AI type's Experience Units by its own price. Experience Units from Copilot, Predictive Engagement, Predictive Routing, Supervisor Copilot and Virtual Supervisor Copilot still count toward Total Experience Units but no longer add to Estimated Cost.
- The Voice and Digital AI Cost Comparison charts use each AI type's price.
- The Lowest Cost view now picks the cheapest AI type for each row by cost at these prices. Digital rows previously compared Experience Units only. With all prices equal, Lowest Cost picks match 2.0.1.
- The Estimated Cost tile shows the prices in use.
- Updated the User Guide, README and screenshots for the new pricing fields.

## [2.0.1] - 2026-11-10

### Changed
- Rewrote the User Guide for the new name and interface, with current screenshots, and renamed it to `Genesys Experience Unit Calculator User Guide.pdf`. The User Guide button opens the new file.
- Removed stray chat text and a duplicated copy of the guide that were in the old PDF.
- Removed "(tokens)" from the subtitle under the title.
- Documented that the Lowest Cost view always counts voice calls of 8:30 or longer as Virtual Agent.

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
