# Sabil Stoppage Tracker

Real-time web application for tracking transfer stoppages during wheat transfer operations at silos.

## Features

- Log stoppages by party (Modern Mills / Sabil) with categorized reasons
- Real-time sync across devices via Firebase Firestore
- Configurable shift times with PIN protection
- Transfer Completed status for monthly target achievement
- Operational dashboard with live KPI cards
- Professional PDF report with availability gauge, dual party tables, and performance summary
- General notes field synced across devices
- Edit/delete stoppages, date picker for historical data
- Automatic midnight rollover for cross-day stoppages

## Project Structure

```
sabil-tracker/
├── stoppage_tracker.html   # Main HTML (entry point)
├── css/
│   └── styles.css          # All styles
├── js/
│   └── app.js              # All application logic
├── assets/
│   └── sabil-logo-white.png # White header logo
├── README.md
└── CHANGELOG.md
```

## Running Locally

Requires a web server (JavaScript modules don't load from `file://`):

```bash
python3 -m http.server 8080
```

Open: `http://localhost:8080/stoppage_tracker.html`

## Deployment

Upload these files to any static hosting (GitHub Pages, etc.):
- `stoppage_tracker.html`
- `css/styles.css`
- `js/app.js`
- `assets/sabil-logo-white.png`

Firebase connects automatically — no server setup needed.

## Backup

Original v1.0 backup: `/Users/mohammedkofayh/Downloads/sabil-tracker-backup/`

## Important Notes

- **10-second refresh** ensures reliable team sync — do not remove
- **PIN code** (`1234`) protects shift times and Clear Day
- **Shift-based PDF**: report pulls data across day boundaries based on configured shift times
- **Transfer Completed** is an operational event, not a stoppage — excluded from all KPI calculations

---

Sabil Stoppage Tracker v2.0 — Developed by Eng. Mohammed Kufiyyah
