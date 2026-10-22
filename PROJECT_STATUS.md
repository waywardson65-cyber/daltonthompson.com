# Project Status — Dalton's Website

> Last updated: 2026-10-22 · Keep this file current as the project moves.

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

## Hosting (confirmed 2026-10-22)

| Item | Value |
|------|-------|
| Type | Shared Linux host (Debian) |
| Origin IP | `65.254.248.180` |
| CDN / proxy | **Cloudflare** in front of the domain (DNS resolves to Cloudflare, not the origin IP) |
| Deploy method | **SFTP** → `ftp.daltonthompson.com` port **2222** |
| FTP (plain) | port 21 open — prefer SFTP |
| Document root | `/home/users/web/b2682/moo.barrythompson` |
| CGI | Active |
| PHP | 8.4.7 (not needed for static site) |
| MySQL | 5.7 (could power a real blog later) |
| Perl | 5.8.8 (not needed) |

> The site is **static** — no PHP/MySQL/Perl required today.

## Done ✅

- [x] Created the GitHub repo (public)
- [x] Scaffolded the site: `index.html`, `games.html`, `blog.html`, `about.html`
- [x] Shared stylesheet (`assets/css/style.css`)
- [x] Copied Fret Quest into the repo and linked it via relative path (`fret-quest.html`)
- [x] Added `CNAME` → `daltonthompson.com` (GitHub Pages only — irrelevant for SFTP deploy, harmless to keep)
- [x] Confirmed SFTP port 2222 reachable and domain proxied via Cloudflare

## Blocked / pending ⏳

- [ ] **SFTP credentials** — need username + password (or SSH key) to deploy.
- [ ] Deploy the repo files to the document root (overwrite the current `index.html`).
- [ ] Fill in Dalton's real bio on `about.html` (marked with a `TODO`).
- [ ] Add first blog post.
- [ ] Build more games (scales, chords, rhythm, theory).

## Next steps (to resume)

1. Get the SFTP username + password/SSH key for the hosting account.
2. Back up the current document root (safety) before overwriting.
3. Upload via SFTP to `ftp.daltonthompson.com:2222` → document root:
   - `index.html`, `games.html`, `blog.html`, `about.html`, `fret-quest.html`, `assets/`
   - (`CNAME` is not needed on this host.)
4. **Purge Cloudflare cache** after upload — HTML is cached up to ~1h (`cache-control: max-age=3600`), so changes may not appear immediately otherwise.
5. Verify the new home page renders at `https://daltonthompson.com/` and Fret Quest still works.

## How to pick this back up

Point Hermes (or anyone) at this file / repo — everything needed to continue is
here and in the commit history.
