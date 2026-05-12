# Highlands & Islands — Road Trip Guide

A personal interactive travel guide for a 10-day road trip through the Scottish Highlands and Islands (April 2019). Built as a single self-contained HTML file with no build step required.

---

## What It Is

This is not a generic Scotland travel site. It's a curated record of one specific trip — Edinburgh → Inverness → Loch Ness → Isle of Skye → Glencoe → Oban → Mull → Treshnish Isles → St Andrews — with real photos, real costs, real opinions, and things I wish I'd known before going.

**Nine tabs:**
- **Map** — interactive Leaflet.js map with every stop pinned and described
- **Itinerary** — day-by-day timeline with times, driving notes, and embedded photos
- **Driving Tips** — left-side driving, single-track roads, roundabouts, the A82
- **Puffins** — deep dive on booking Staffa Tours from Oban, what to wear on Lunga, biology, and a full photo gallery from the May 2019 boat trip
- **Locale** — place-specific notes, history and terminology (what "loch" means, Munros, Gaelic prefixes, clan castle types), whisky country context
- **Packing** — interactive checklist (Scotland-specific, click-to-check)
- **Budget** — editable live budget tracker — real numbers from the trip
- **Plan Yours** — customisable trip planner with date picker and cost calculator
- **Gallery** — 55 photos from the trip, organised by place

---

## Tech Stack

| Layer | What |
|---|---|
| HTML/CSS/JS | Single file, no frameworks, no build step |
| Fonts | [Fraunces](https://fonts.google.com/specimen/Fraunces) (serif) + [Inter](https://fonts.google.com/specimen/Inter) (sans) via Google Fonts |
| Map | [Leaflet.js](https://leafletjs.com/) 1.9.4 via CDN |
| Icons | [Lucide](https://lucide.dev/) via CDN |
| Images | [Cloudinary](https://cloudinary.com/) — auto-format, auto-width, lazy-loaded |
| Hosting | GitHub Pages (see below) |

Everything runs client-side. No server, no database, no API keys in the browser.

---

## Viewing Locally

Clone or download the repo, then open the HTML file directly in a browser:

```bash
git clone https://github.com/YOUR_USERNAME/scotland-travel-guide.git
cd scotland-travel-guide
open Scotland-Travel-Guide.html   # macOS
# or: start Scotland-Travel-Guide.html  (Windows)
# or: xdg-open Scotland-Travel-Guide.html  (Linux)
```

No local server needed — everything loads from CDN and Cloudinary.

---

## Deploying to GitHub Pages

### First-time setup

1. **Create a new GitHub repository**
   - Go to [github.com](https://github.com) → click **+** → **New repository**
   - Name it `scotland-travel-guide` (or anything you like)
   - Set to **Public** (required for free GitHub Pages)
   - Do **not** initialise with README (you already have one)
   - Click **Create repository**

2. **Upload the files**
   - On the repository page, click **uploading an existing file** (or drag and drop)
   - Upload both files: `Scotland-Travel-Guide.html` and `README.md`
   - Write a commit message: `Initial upload`
   - Click **Commit changes**

3. **Enable GitHub Pages**
   - Go to **Settings** → **Pages** (left sidebar)
   - Under **Source**, select **Deploy from a branch**
   - Branch: `main` — Folder: `/ (root)`
   - Click **Save**
   - Wait ~60 seconds, then refresh the page
   - Your URL will appear: `https://YOUR_USERNAME.github.io/scotland-travel-guide/Scotland-Travel-Guide.html`

### Making updates later

**Option A — via the GitHub website:**
- Go to the repository
- Click `Scotland-Travel-Guide.html` → click the **pencil icon** to edit
- Paste in the updated content → **Commit changes**

**Option B — via Git CLI (faster for big changes):**
```bash
git add Scotland-Travel-Guide.html
git commit -m "describe what changed"
git push
```
Changes go live within ~30 seconds of pushing.

---

## Project Structure

```
scotland-travel-guide/
├── Scotland-Travel-Guide.html   # The entire guide — everything is here
└── README.md                    # This file
```

All images are hosted on Cloudinary (free tier). All map tiles are from OpenStreetMap via Leaflet.js. No assets need to be committed to this repo.

---

## Photos

All photos are my own, taken on the April–May 2019 trip. They are hosted on Cloudinary and referenced via URL — nothing is bundled in the HTML file itself. If you fork this project, the images will continue to load from my Cloudinary account unless you re-host them yourself.

---

## Credits

- Tile layer: [OpenStreetMap contributors](https://www.openstreetmap.org/copyright)
- Boat trips: [Staffa Tours](https://www.staffatours.com/) (Oban) — genuinely worth the early booking
- Ferry: [CalMac Ferries](https://www.calmac.co.uk/) — Oban to Mull

---

## Licence

Personal project. Code is MIT-licensed if you want to use the structure for your own travel guide. Photos are not included in this licence.
