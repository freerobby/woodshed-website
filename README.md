# Woodshed Website

Marketing site for the [Woodshed](https://woodshedapp.com) iOS app.

**Live:** https://freerobby.github.io/woodshed-website/

---

## Stack

Plain HTML5 + CSS. No build step, no framework, no dependencies other than Google Fonts. Open `index.html` directly in a browser to preview locally.

```
woodshed-website/
├── index.html        ← single-page site
├── css/
│   └── style.css     ← all styles, CSS variables for color palette
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

## Wiring up Mailchimp

There are **two** email forms in `index.html` — one in the hero and one in the mid-page email capture section. The capture section form has an `id="mc-embedded-subscribe-form"` comment block explaining where to drop the Mailchimp action URL.

1. In Mailchimp, go to **Audience → Signup forms → Embedded forms** and copy the form `action` URL (looks like `https://yourlist.us1.list-manage.com/subscribe/post?u=XXX&id=YYY`).
2. Replace `action="#"` on the form with `id="mc-embedded-subscribe-form"` with that URL.
3. Also replace the anti-bot hidden input's `name` attribute with the value Mailchimp provides.
4. If you want the hero form to also subscribe, repeat for `id="hero-form"`.

---

## Adding a real app screenshot

Replace the CSS phone mockup in `index.html` with an actual screenshot:

1. Export a screenshot at 2× (e.g. `assets/screenshot.png`).
2. In `index.html`, replace the `.phone-mock` `<div>` block with:
   ```html
   <img src="assets/screenshot.png" class="app-screenshot" alt="Woodshed app screenshot" width="260" />
   ```
3. Add to `style.css`:
   ```css
   .app-screenshot { border-radius: 36px; box-shadow: 0 40px 100px rgba(0,0,0,0.7); }
   ```

---

## Deploying

The site is hosted on **GitHub Pages** from the `main` branch root.

To deploy an update:

```bash
cd /path/to/woodshed-website
# make your edits
git add -A
git commit -m "describe your change"
git push origin main
```

GitHub Pages automatically rebuilds within ~60 seconds.

To check Pages status:

```bash
gh api repos/freerobby/woodshed-website/pages
```
