# Project Status — Dalton's Website

> Last updated: 2026-10-21 · Keep this file current as the project moves.

## What this is

Personal website for **Dalton Thompson**, hosted at **daltonthompson.com**.
Focus: educational games for learning guitar and music theory, plus a blog.

## Key facts

| Item | Value |
|------|-------|
| Domain | `daltonthompson.com` |
| GitHub repo | `waywardson65-cyber/daltonthompson.com` (public) |
| Default branch | `main` |
| Existing game | **Fret Quest** — learn guitar fretboard notes |
| Game file | `fret-quest.html` (self-contained; in-repo copy) |
| Game live URL | `https://daltonthompson.com/fret-quest.html` |

## Done ✅

- [x] Created the GitHub repo (public)
- [x] Scaffolded the site: `index.html`, `games.html`, `blog.html`, `about.html`
- [x] Shared stylesheet (`assets/css/style.css`)
- [x] Copied Fret Quest into the repo and linked it via relative path (`fret-quest.html`)
- [x] Added `CNAME` → `daltonthompson.com` (ready for GitHub Pages)

## Not done / blocked ⏳

- [ ] **Deploy the new site to `daltonthompson.com`** — the domain is already
      pointed at an existing host (that's how `fret-quest.html` is live), but the
      hosting provider is **unknown** and the credentials aren't available yet.
- [ ] Confirm which host is serving the domain (GitHub Pages? Netlify? Vercel? other?)
- [ ] Fill in Dalton's real bio on `about.html` (marked with a `TODO`)
- [ ] Add first blog post
- [ ] Build more games (scales, chords, rhythm, theory)

## Next steps (to resume)

1. Identify the current host for `daltonthompson.com` (check DNS records, or find the credentials).
2. Decide deployment path:
   - **GitHub Pages** — enable Pages on this repo (Settings → Pages → `main` branch),
     then point DNS `A`/`CNAME` records at GitHub. Free, keeps everything in one place.
   - **Existing host** — connect this repo to that host (Netlify/Vercel/etc.) instead.
3. Confirm the new `index.html` renders at the domain root, with Fret Quest still reachable.

## How to pick this back up

Point Hermes (or anyone) at this file / repo — everything needed to continue is
here and in the commit history.
