# Sexy Dice Game — standalone GitHub Pages bundle

A dice game for two consenting adults. This folder is the complete standalone
site (no Muse wrapper): `index.html` + `manifest.webmanifest` + `sw.js` +
SVG icons, so Chrome on Android can install it as its own app
("Sexy Dice", own icon, full-screen standalone).

## Remaining step for a full WebAPK install (PNG icons)

Chrome's full Android install (WebAPK) wants PNG icons at 192px and 512px.
The live manifest currently references the SVG icons (text files, pushed via
the Muse GitHub connector — that connector corrupts binary uploads, which is
why the PNGs are not in this repo yet).

Ready-made PNGs are in `png-for-manual-upload/` in the local bundle
(genuine 192px + 180px icons extracted from the game, plus generated
512px / maskable-512px icons):

1. In this repo on github.com, use **Add file → Upload files** and upload
   `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, and
   `apple-touch-icon.png` to the repo root.
2. Replace `manifest.webmanifest` with the contents of
   `png-for-manual-upload/manifest-with-png.webmanifest` (same filename,
   `manifest.webmanifest`) — it adds the PNG icons alongside the SVGs.
3. Reopen the site in Chrome, then ⋮ → **Install app**.

Until then the site still loads and plays identically, and Chrome offers
at minimum "Add to Home screen".
