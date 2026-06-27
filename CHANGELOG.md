# Changelog

All notable changes to the Sabil Stoppage Tracker are documented in this file.

---

## [2.0.0] — 2026-06-27

### Summary

Major feature update with new PDF report design, operational dashboard, shift management, and Transfer Completed status. All existing functionality preserved.

### Added

- **PDF Report Redesign**: Dashboard-style report with KPI cards (Availability gauge, Running Time, Downtime, Total Stops, Status), dual party tables with category badges, downtime breakdown bars, key highlights, availability result, and improved signature area.
- **Shift Time Settings**: Configurable shift start/end times per day, stored in Firestore. PDF report pulls data across day boundaries when shift crosses midnight.
- **General Notes**: Text field for daily operational notes, synced via Firestore, displayed in PDF report.
- **Transfer Completed Status**: Operational event for monthly target completion. Accessed via Log Stoppage flow. Does not count as downtime or affect KPI calculations.
- **Operational Dashboard Cards**: Summary cards showing Sabil stops, Mills stops, current status, and last update — with company logos.
- **Stoppage Category Classification**: Automatic categorization of stoppage reasons (Technical, Mechanical, Electrical, Maintenance, Operational) displayed in PDF tables.
- **PIN Protection**: Admin PIN required for changing shift times and clearing daily data.
- **Animated Status Indicators**: Rotating gears icon for Running state, checkered flag for Transfer Completed.
- **White Sabil Logo**: Header uses white logo on dark green background.

### Not Changed

- Firebase configuration and initialization.
- 10-second refresh interval for synchronization.
- Firestore real-time listener (`onSnapshot`).
- Stoppage logging, editing, and deletion.
- Duration calculations.
- Midnight rollover logic.
- All existing UI elements preserved.

---

## [1.1.0] — 2026-06-27

### Summary

Reorganized the project from a single monolithic HTML file into a structured multi-file layout.

### Changed

- Extracted CSS into `css/styles.css`.
- Extracted JavaScript into `js/app.js`.
- Updated HTML to reference external files.

---

## [1.0.0] — Original Release

### Summary

Initial version. Single file (`stoppage_tracker.html`).

### Features

- Log transfer stoppages with party assignment (Modern Mills / Sabil).
- Real-time synchronization via Firebase Firestore.
- Live clock and elapsed timer.
- Date picker for historical logs.
- Edit and delete stoppages.
- Midnight rollover.
- Text summary and PDF report export.
