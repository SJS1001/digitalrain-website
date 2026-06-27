# Digitalrain ONE — website

Scroll-driven product website for **Digitalrain ONE**, the real-time digital-twin platform for mining operations. Built as a single Design Component with a WebGL "digital rain" hero, Apple-style scroll motion, and live-animating telemetry (sparklines, dashboard charts, digital-twin stats).

## Files

| File | Purpose |
|---|---|
| `standalone.html` | **Self-contained build.** Everything (markup, images, fonts, scripts) inlined into one file. Open directly in any browser or serve as-is. Use this for GitHub Pages. |
| `Digitalrain ONE.dc.html` | Editable source (Design Component). References `support.js` and `assets/`. |
| `support.js` | Design Component runtime. |
| `assets/digital-twin.png` | Engebø aerial digital-twin image (full-bleed panel). |
| `assets/fjord.png` | Engebø fjord parallax image (Industries section). |

## Run locally

Just open `standalone.html` in a browser — no build step, no server required.

To edit, work in `Digitalrain ONE.dc.html` and serve the folder over a local web server (so `support.js` and `assets/` resolve), e.g.:

```bash
python3 -m http.server
# then open http://localhost:8000/Digitalrain%20ONE.dc.html
```

## Deploy to GitHub Pages

1. Commit this folder to a repo.
2. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**.
3. Pick your branch and the folder, then save.
4. Rename `standalone.html` to `index.html` (or set it as the entry) so the site loads at the Pages root.

## Design

Dark charcoal canvas, teal accent (`#3DDC97`), Inter + JetBrains Mono — aligned to the OPUS Aurora 2.0 design language. All telemetry animates at data-representative speeds; scroll reveals use a one-way IntersectionObserver so content can never get stuck hidden.
