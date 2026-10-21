# daltonthompson.com

Personal website for **Dalton Thompson** — educational games for learning guitar and music theory, plus a blog.

## What's here

- **Home** (`index.html`) — intro and featured content
- **Games** (`games.html`) — educational music/guitar games
- **Fret Quest** (`fret-quest.html`) — learn the notes of the guitar fretboard
- **Blog** (`blog.html`) — posts (coming soon)
- **About** (`about.html`) — about Dalton

## Structure

```
.
├── index.html
├── games.html
├── blog.html
├── about.html
├── fret-quest.html      # the fretboard game
├── CNAME                # custom domain
├── assets/
│   └── css/
│       └── style.css
└── README.md
```

## Local development

This is a plain static site — no build step. Just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Custom domain

The site is served at **daltonthompson.com**. The `CNAME` file tells GitHub Pages (or another static host) which domain to use.

---

© 2026 Dalton Thompson
