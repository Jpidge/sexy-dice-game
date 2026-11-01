# Sexy Dice Game

A two-dice game for two consenting adult partners. Roll two 12-face dice —
one picks the action, the other picks where. Per-player anatomy toggles
(Dick/Pussy) make the roll wording body-specific for each partner. Includes
read-aloud with voice personalities, a turn timer, Skip & Reroll, and bonus
cards on matching faces.

**Play it:** https://jpidge.github.io/sexy-dice-game/ — GitHub Pages,
published from the `main` branch of this repo.

## Heat levels

- **Sweet** — gentle.
- **Spicy** — kinkier sensory play.
- **Wild** — explicit oral/fucking content, plus experimental-position
  bonus cards.
- **BDSM** — the dirtiest level: kink scenes, a safeword check-in card,
  and the whole site flips to a red theme.

The Spicy and Wild contents were swapped on 2026-11-01 so the ladder
matches the labels (Spicy used to hold the explicit deck).

## Theme

Purple backgrounds with softened dusty-rose / pastel-orchid pink accents
(#a95284, #d99ac0). Selecting BDSM switches the site to deep red.

## Install as a web app

Full PWA: a manifest with PNG icons (192/512, plus a maskable 512)
alongside the SVGs, and a service worker whose cache version bumps with
each content sync (currently v4). Open the site in Chrome on Android and
choose **Install app**. The in-page “Install it as an app” card hides
itself automatically when the page is running inside the Android app.

## Android APK

A signed APK also exists: a Trusted Web Activity (built with Bubblewrap),
package `app.github.jpidge.sexydice`, app name “Sexy Dice”. It runs
fullscreen, verified via Digital Asset Links served at
https://jpidge.github.io/.well-known/assetlinks.json (hosted in the
separate Jpidge/jpidge.github.io repo). The APK project lives outside
this repo, in a local workspace folder (`sexy-dice-apk/`), and any update
APK must be signed with the same keystore.

## Files in this repo

- `index.html` — the whole game, a single file
- `manifest.webmanifest` — PWA manifest
- `sw.js` — service worker
- `icon.svg`, `icon-maskable.svg` — SVG icons
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`,
  `apple-touch-icon.png`, `favicon-32.png` — PNG icons
- `.nojekyll` — keeps GitHub Pages from running Jekyll

## Maintenance

The game is authored as a Muse web artifact (“Sexy Dice Game”) and
synced to this repo. Each export is adapted in exactly three ways: the
manifest link is pointed at `manifest.webmanifest`, an SVG favicon link
is added, and the service-worker registration is added. Each content
sync bumps the cache version in `sw.js`.
