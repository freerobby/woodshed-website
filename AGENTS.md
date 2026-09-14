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
  filenames. That step is **woodshed-mac only**. Linux app agents list stale
  files in the app repo (`marketing/screenshots-stale.md`); they do not
  capture. Hero/recording: empty Practice. Weekly-goal chips are opt-in;
  reset the Simulator and pass `-WoodshedSkipOnboarding`.
- Privacy copy lives in `privacy/index.html`. If the data story changes,
  update it in the same website PR as the homepage if both are affected.
- Do not invent launch dates or platforms.
