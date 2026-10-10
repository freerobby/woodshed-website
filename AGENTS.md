# Agent notes

This is the marketing site for the native iOS app in
[`freerobby/woodshed`](https://github.com/freerobby/woodshed). Plain HTML/CSS.
GitHub Pages from `main`.

The **app** repo owns when this site must change. Agents working on Woodshed
follow `.cursor/rules/marketing-site.mdc` there. Do not wait for a separate
“please update the website” prompt.

When you *are* in this repo:

- Keep Practice and Write as two rooms, one library. Do not split the
  product into two apps or two homepages.
- Recapture Simulator PNGs in `images/` using the map in `README.md`. Keep
 filenames. Only screens shown on the homepage live here. That step is
 **woodshed-mac only**. Linux app agents list stale files in the app repo
 (`marketing/screenshots-stale.md`); they do not capture. `recording.png`
 is a quiet Practice mid-recording. Weekly-goal chips are opt-in; reset the
 Simulator and pass `-WoodshedSkipOnboarding`.
- The homepage is one layout: a headline, a sentence or two, one phone per
 beat. Add a new idea as another `.beat`, not a new layout system.
- Privacy copy lives in `privacy/index.html`. If the data story changes,
  update it in the same website PR as the homepage if both are affected.
- Do not invent launch dates or platforms.

## Cursor Cloud specific instructions

Plain HTML and CSS. There is no package install, lint, test suite, or build.

The environment start script serves the repo root on port 8000. If `http://127.0.0.1:8000/` already responds, leave that server running. Otherwise start it from the repo root:

```bash
python3 -m http.server 8000 --bind 0.0.0.0
```

Homepage: `http://127.0.0.1:8000/`. Privacy policy: `http://127.0.0.1:8000/privacy/`.
