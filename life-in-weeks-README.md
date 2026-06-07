# Life in Weeks ⏳

A single-page **memento mori** web app that visualises an entire human lifespan as a grid of weeks, with a live reverse countdown of the time remaining. Built with zero dependencies and deployed free on GitHub Pages.

> *"How we spend our days is how we spend our lives."*

**🔗 Live demo:** `https://<your-username>.github.io/life-in-weeks/`

<!-- Add a screenshot here: drag an image into the GitHub editor, or commit one as screenshot.png -->
<!-- ![Screenshot](screenshot.png) -->

---

## Overview

Inspired by the "Life in Weeks" idea, the app turns an abstract lifespan into something you can *see*: every week of a chosen life expectancy is a single cell, split into the weeks already lived and the weeks remaining. A large counter and a live ticker count **down** in real time, reframing time as a finite, visible resource.

## Features

- **Live reverse countdown** — weeks remaining, plus a ticking `days : hours : minutes : seconds` display updated every second.
- **Full life grid** — one cell per week (52 per row); lived weeks, the current week, and remaining weeks are colour-coded.
- **Editable lifespan** — change the expected lifespan inline; the counter, grid, and projected end-date all recalculate instantly.
- **Expected end-date** — derived from birth date + lifespan, leap years included.
- **Reflections panel** — a curated collection of quotes on time and life.
- **Responsive & self-contained** — works on mobile and desktop; settings persist locally between visits.

## Tech Stack

- **HTML5, CSS3, vanilla JavaScript** — no frameworks, no build step, no dependencies.
- **Web Storage API** (`localStorage`) for persisting user settings.
- **GitHub Pages** for hosting.

## How It Works

- All date arithmetic (weeks lived / remaining / total, percentage, end-date) is computed at runtime from the birth date and lifespan, so the figures are always exact and current.
- The grid is rendered dynamically from the computed week count; only the cell representing the current week is recomputed as time passes, keeping updates cheap.
- A 1-second interval drives the live ticker; user settings are saved to `localStorage` so they survive refreshes.

## Run Locally

No build tools required — it's a single static file.

```bash
git clone https://github.com/<your-username>/life-in-weeks.git
cd life-in-weeks
# open index.html in any browser
```

## Deploy to GitHub Pages

1. Push the repo to GitHub (file named `index.html` at the root).
2. **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.**
3. The site goes live at `https://<your-username>.github.io/life-in-weeks/`.

## Customisation

Open the in-app settings to change the **birth date** and **expected lifespan**; everything recalculates live. Colours are defined as CSS variables at the top of `index.html` for easy theming.

## Possible Enhancements

- A shareable "card" view for social media.
- Milestone markers on the grid (e.g. graduations, retirement).
- A "productive hours remaining" mode based on waking hours.

## License

Released under the [MIT License](LICENSE). Free to use and adapt.
