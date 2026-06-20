# Run & Play Adventure 🏃🐶

A side-scrolling runner starring the girl and her Cavalier King Charles Spaniel. Swipe up to jump over rolling balls, swipe down to duck under flying balls, and keep up as they run faster and faster. Single lightweight, offline-capable web app — no build step, no dependencies.

This is a **separate app from Match & Play** — give it its own GitHub repo, following the same steps you already know.

## Files

- `index.html` — the entire game (HTML/CSS/JS, artwork embedded inline)
- `manifest.json` — Web App Manifest, so it can install as a standalone app
- `sw.js` — service worker that caches the app so it works fully offline
- `icon-192.png`, `icon-512.png` — app icons (Android/Chrome)
- `apple-touch-icon.png` — app icon (iOS/Safari)

## Put it on GitHub (new repo)

1. Create a **new** repository (e.g. `run-and-play`) — don't reuse the Match & Play one.
2. Upload all 7 files above to it. On your phone:
   - Extract this zip first if you downloaded it as one
   - In the repo: **Add file → Upload files** → select all 7 files
   - If `sw.js` doesn't show up in your file picker, create it manually instead: **Add file → Create new file**, name it `sw.js`, and paste its contents in (same trick that worked last time)

## Turn on GitHub Pages

1. **Settings → Pages**
2. Source: **Deploy from a branch** → branch `main` → folder `/ (root)` → **Save**
3. Live in a minute or two at `https://<your-username>.github.io/run-and-play/`

## Install it as an app

1. Open that URL in Chrome on your phone
2. **Clear browsing data → Cached images and files** if you're testing right after setup (avoids stale cache issues)
3. Open the ⋮ menu and look for **Install app**
4. Open it once while online so the service worker can cache everything — after that it works fully offline

## How to play

- **Swipe up** to jump over rolling balls (a small tap works too)
- **Swipe down** to duck under flying balls (auto-stands after a moment)
- You can interrupt one action with the other — swipe down mid-jump to drop into a duck, or swipe up to leap straight out of a duck
- Starts at a brisk pace and speeds up the longer you survive
- Three hearts — lose all three and you'll get a friendly "try again" screen with your score
- Tap the girl or dog on the start screen for a woof!

## Editing later

Same structure as Match & Play: open `index.html` in any text editor. Artwork is embedded as base64 near the top of `<body>`, game logic is plain JavaScript at the bottom (look for the `<script>` tag).
