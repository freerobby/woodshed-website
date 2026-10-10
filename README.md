# Woodshed Website

Marketing site for the [Woodshed](https://getwoodshed.com) iOS app.

**Live:** https://getwoodshed.com

---

## Stack

Plain HTML5 + CSS. No build step, no framework. Google Fonts loads Instrument Serif and Instrument Sans. Open `index.html` directly in a browser to preview locally.

```
woodshed-website/
├── index.html        ← marketing homepage
├── privacy/
│   └── index.html    ← Privacy Policy (https://getwoodshed.com/privacy)
├── css/
│   └── style.css     ← all styles, CSS variables for color palette
├── images/           ← app icon + native screenshots
└── README.md
```

---

## Color palette

Defined as CSS variables at the top of `style.css`:

| Variable            | Value     | Usage                      |
|---------------------|-----------|----------------------------|
| `--color-bg`        | `#090909` | Page background            |
| `--color-accent`    | `#C9883A` | Primary / brass            |
| `--color-gold`      | `#E8A84C` | Hover / highlight          |
| `--color-text`      | `#F5F0E8` | Headlines                  |
| `--color-text-soft` | `#B3ADA3` | Homepage body copy         |
| `--color-text-sec`  | `#8A8A8A` | Secondary copy, legal body |
| `--color-paper`     | `#F5F0E8` | Write band                 |

## Homepage layout

One idea per screen. Every section after the hero uses the same `.beat`
layout: copy on one side, a single phone screenshot on the other, stacked
on mobile. There are no icons, cards, timelines, or section borders;
whitespace separates ideas. The Write section is the only tonal break (the
`--color-paper` band). Add new content as another `.beat`, not a new
layout system.

---

## App Store

Download links use `https://apps.apple.com/app/id6760981537` (Woodshed, bundle id `com.woodshed`). The nav “Get the app” button, the closing section, and the footer all use that URL. Badge artwork is the official Apple file at `images/app-store-badge.svg` — do not redraw it.

---

## Screenshots

Native captures live in `images/`. The app repo maps which UI change
recaptures which file (`marketing/screenshot-map.md` in
`freerobby/woodshed`); its UI test writes captures straight into this
folder. Keep these filenames. Only screens shown on the homepage are kept
here; if you add a screen back, restore its bullet in the app repo map and
its `writeScreenshot` call in `TabSmokeTests.testCaptureMarketingScreenshots`.

| File | Screen | On homepage | Recapture when |
|------|--------|-------------|----------------|
| `room.jpg` | Practice-room photograph (hero) | Hero | Never from the Simulator; this is artwork |
| `recording.png` | Practice while recording | Practice, beat 1 | Recording UI, Practice chrome, tab bar |
| `session.png` | Session review | Practice, beat 2 | Segments, match chips, ratings |
| `piece.png` | Piece detail | Practice, beat 3 | Piece stats, progress, session history |
| `idea.png` | Idea detail, opened from Write | Write | Idea detail, takes, tags |
| `library.png` | Library | Library, beat 1 | Library rows, filters, pieces vs ideas |
| `library-listen.png` | Library listen sheet with matches | Library, beat 2 | Search by playing, Piece and Idea rows |
| `og.png` | Open Graph card (1200×630) | Social previews | App icon or homepage tagline only |

`recording.png` should be a quiet Practice mid-recording. Weekly-goal chips
are opt-in and off by default — reset the Simulator so they stay hidden.
On Simulator: `-WoodshedSkipOnboarding`. Demo library: jazz standards,
well-known classical pieces, a few named song ideas.

Linux cloud agents do not recapture. They list owed files in the app repo
(`marketing/screenshots-stale.md`). Recapture on woodshed-mac (iPhone 17
Simulator) when that session already exists (usually TestFlight).

---

## Deploying

The site is hosted on **GitHub Pages** from the `main` branch root (`getwoodshed.com`).

```bash
cd /path/to/woodshed-website
git add -A
git commit -m "describe your change"
git push origin main
```

GitHub Pages rebuilds within about a minute.
