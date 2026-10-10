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

| Variable           | Value     | Usage               |
|--------------------|-----------|---------------------|
| `--color-bg`       | `#090909` | Page background     |
| `--color-accent`   | `#C9883A` | Primary / brass     |
| `--color-gold`     | `#E8A84C` | Hover / highlight   |
| `--color-text`     | `#F5F0E8` | Body copy           |
| `--color-text-sec` | `#8A8A8A` | Secondary copy      |

---

## App Store

Download links use `https://apps.apple.com/app/id6760981537` (Woodshed, bundle id `com.woodshed`). The nav “Get the app” button, the closing section, and the footer all use that URL. Badge artwork is the official Apple file at `images/app-store-badge.svg` — do not redraw it.

---

## Screenshots

Native captures live in `images/`. The app repo maps which UI change
recaptures which file (`.cursor/skills/marketing-site/SKILL.md` in
`freerobby/woodshed`). Keep these filenames. The Homepage column is what `index.html` shows; the other files stay in `images/` for the app repo’s recapture map.

| File | Screen | Homepage | Recapture when |
|------|--------|----------|----------------|
| `practice.png` | Practice tab, idle record | Yes — Practice chapter | Practice chrome, record button, tab bar, empty state |
| `recording.png` | Practice while recording | No — same screen as `practice.png`, while recording | Recording UI |
| `write.png` | Write tab | Yes — Write chapter | Write list, best-take badges |
| `write-list.png` | Write tab ideas list | No — same screen as `write.png` | Write list, before an idea is opened |
| `idea.png` | Idea detail, opened from Write | Yes — Write chapter | Idea detail, takes, tags |
| `session.png` | Session review | Yes — Practice chapter | Segments, match chips, ratings |
| `piece.png` | Piece detail | Yes — Practice chapter | Piece stats, progress, session history |
| `library.png` | Library | No | Library rows, filters, pieces vs ideas |
| `library-listen.png` | Library listen sheet with matches | Yes — Library | Search by playing, Piece and Idea rows |
| `og.png` | Open Graph card (1200×630) | Social card, not the page | App icon or homepage tagline only |

Hero and recording should be a quiet empty Practice. Weekly-goal chips
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
