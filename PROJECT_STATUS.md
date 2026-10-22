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

## Hosting

| Item | Value |
|------|-------|
| Provider | **FatCow** (shared Linux host, Debian) |
| Origin IP | `65.254.248.180` |
| CDN | **Cloudflare** in front of the domain (DNS resolves to Cloudflare) |
| Deploy method | **SFTP** → origin IP `65.254.248.180` port **2222** |
| SFTP user | `hragent` (password supplied by Barry at deploy time) |
| Web root (SFTP view) | `/` — the account is **chrooted** to the daltonthompson.com web root |
| Server doc-root path | `/home/users/web/b2682/moo.barrythompson` (internal; not visible over SFTP) |
| PHP / MySQL / Perl | 8.4.7 / 5.7 / 5.8.8 — unused, the site is static |

### Deploy gotchas (IMPORTANT)

1. Connect to the **origin IP** `65.254.248.180`, *not* `ftp.daltonthompson.com` —
   that hostname is Cloudflare-proxied and silently drops SFTP.
2. The host only offers **`ssh-rsa` (SHA-1) host keys** → use `paramiko<4`
   (paramiko 5.x removed `ssh-rsa` support entirely and cannot connect).
3. The SFTP account is **chrooted**, so the web root is `/`, not the `/home/users/...` path.
4. `.htaccess` sets `DirectoryIndex index.html`; the old `home.html` is now a redirect to `index.html`.
5. The web root also holds **other projects** (a `vault` app, zenphoto photo albums,
   webalizer `stats/`, a WordPress DB dump) — **back up and never delete them**.

## Done ✅

- [x] Created the GitHub repo (public)
- [x] Scaffolded the site: `index.html`, `games.html`, `blog.html`, `about.html` + `assets/css/style.css`
- [x] Copied Fret Quest into the repo and linked it
- [x] Deployed to `daltonthompson.com` via SFTP — **verified live** (origin + Cloudflare)
- [x] Backed up the existing web root (742 files) before touching anything

## Pending ⏳

- [ ] Fill in Dalton's real bio on `about.html` (marked with a `TODO`)
- [ ] Add first blog post
- [ ] Build more games (scales, chords, rhythm, theory)

## How to redeploy

Deploy/backup script: `/tmp/deploy_dalton.py` (requires `paramiko<4`; holds the SFTP password, chmod 600).
Re-run `python3 /tmp/deploy_dalton.py deploy` after updating files in the repo checkout at `/tmp/daltonthompson.com`.
Pre-deploy backup: `/tmp/dalton_backup_1792634476/`.

## How to pick this back up

Point Hermes (or anyone) at this file / repo — everything needed to continue is
here and in the commit history.
