# 030 · Sleep Curve

**AppADay — Day 030**
Category: Data Visualization · Built: 2026-06-06

Log your bedtime and wake time each night and watch your sleep curve take shape. Color-coded durations, a 7-hour target line, nightly stats, and iOS Shortcuts support for one-tap automatic logging.

---

## Features

- Log bedtime and wake time for any night; duration calculated automatically across midnight boundaries.
- Smooth Bezier line chart rendering up to 7 most recent nights via HTML Canvas.
- 7-hour target shown as a dashed reference line on the chart.
- Duration dots color-coded green (7h+), amber (6–7h), red (under 6h).
- Stats bar showing average sleep, best night, and count of 7+ hour nights.
- Duplicate-safe: logging the same date twice updates the existing entry.
- Date field auto-advances by one day after each log entry for fast week-entry.
- URL parameter support: `?bed=HH:MM&wake=HH:MM&date=YYYY-MM-DD&log=1` pre-fills and optionally auto-submits an entry.
- ⚡ Shortcuts modal with step-by-step iOS Shortcuts setup instructions and live URL examples pre-populated with the app's deployed URL.
- Toast confirmation on auto-log via URL params.
- All data persisted in localStorage; no account, no backend.
- Back link to AppADay portfolio on every page load.

## Stack

Single-file vanilla HTML/CSS/JS. No frameworks, no dependencies, no build step. Canvas 2D API for chart rendering. Cormorant Garamond + DM Mono typography. Deep navy editorial aesthetic with starfield background.

## iOS Shortcuts Integration

Create two Shortcuts in the iOS Shortcuts app:

**Bedtime shortcut** — Action: Open URLs → `https://[your-url]/?bed=[Current Time]`

**Wake shortcut** — Action: Open URLs → `https://[your-url]/?bed=[stored bedtime]&wake=[Current Time]&log=1`

The wake shortcut auto-submits the entry. Tap the ⚡ Shortcuts button inside the app for full instructions with your live URL pre-filled.

## Definition of Complete

- [x] Functional — logs entries, calculates duration, renders chart without errors
- [x] Single purpose — one clear job: track nightly sleep duration over time
- [x] Mobile friendly — usable at 375px, 16px inputs, tap targets correctly sized
- [x] Visually polished — dark editorial palette, intentional typography, smooth chart
- [x] Published — live GitHub Pages URL, numbered and named

## Links

- Live app: https://augustineiacopelli.github.io/appaday-030-sleep-curve/
- Portfolio: https://augustineiacopelli.github.io/appaday/
