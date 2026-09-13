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
| `--color-paper`    | `#F5F0E8` | Write-room panel    |

---

## Email capture

The homepage has one Formspree form (`https://formspree.io/f/xeepeaja`) in the launch section. Nav “Get notified at launch” jumps there.

---

## Screenshots

Native captures live in `images/`:

| File | Screen |
|------|--------|
| `practice.png` | Practice tab (hero) |
| `recording.png` | Recording a session |
| `write.png` | Write tab |
| `session.png` | Session review |
| `library.png` | Library |
| `piece.png` | Piece detail |

Recapture from the native Simulator when the app UI changes. Demo library on these shots: modern jazz standards and well-known classical pieces.

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
