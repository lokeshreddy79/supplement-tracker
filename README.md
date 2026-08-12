# The Daily Dose — Supplement Tracker

A single-page, local-first web app for tracking daily supplement/vitamin intake.
No backend, no build step — all data is stored in your browser's `localStorage`.

## Features

- Add, edit, and remove supplements (name, dosage, time of day)
- Daily checklist grouped by Morning / Afternoon / Evening / Anytime
- Streak tracking (consecutive days with everything checked off)
- Today's progress gauge
- 14-day history heatmap

## Project structure

```
supplement-tracker/
├── index.html      # entire app: markup, styles, and logic
├── package.json     # optional scripts for running a local dev server
└── README.md
```

Everything lives in `index.html` on purpose — it's a single file you can
open directly in a browser with no tooling at all.

## Running it

**Option A — just open the file**
Double-click `index.html`, or drag it into a browser window. Nothing to install.

**Option B — run a local dev server (recommended in VS Code)**
A local server avoids any browser quirks around opening files directly via `file://`.

```bash
npm install --no-save serve   # only needed once, or rely on npx as below
npm start                     # serves the folder at http://localhost:5173
```

or, for auto-reload on save while you develop:

```bash
npm run dev
```

In VS Code, the **Live Server** extension also works great — right-click
`index.html` → "Open with Live Server".

## Data & privacy

All data is stored locally in your browser via `localStorage` under the key
`daily-dose-tracker-v1`. Nothing is sent anywhere. Clearing your browser's
site data for this page will erase your history — there's no cloud backup
in this version.

## Ideas for future development

- Export/import data as JSON (for backup or moving between devices)
- Reminders/notifications at each time-of-day slot
- Multiple profiles
- Cloud sync (e.g. a small backend + auth) if you want cross-device access
- Notes field per dose (how you felt, side effects, etc.)
- Weekly/monthly summary view beyond the 14-day heatmap

## Tech

Vanilla HTML/CSS/JS. Fonts: Fraunces (display), IBM Plex Sans (body),
IBM Plex Mono (data/labels), loaded from Google Fonts.
