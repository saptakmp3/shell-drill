# Shell Drill PWA

## Included
- `index.html` — the Shell Drill app
- `manifest.webmanifest` — install metadata and app icons
- `sw.js` — offline app-shell caching
- `icons/` — 192px, 512px, and maskable icons

## Run locally
A PWA must be served from **HTTPS** or `localhost`; opening `index.html` directly as a `file://` URL will not enable installation or the service worker.

For local testing, from this folder run:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Deploy
Upload the contents of this folder to the root of an HTTPS static host (GitHub Pages, Cloudflare Pages, Netlify, etc.). Open the deployed URL in Chrome and choose **Install app** / **Add to Home screen**.

The app's existing localStorage settings and best scores remain stored by the browser on that device. The service worker caches the app shell for offline launches after the first successful visit.
