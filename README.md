# Android 4.0.4 Ice Cream Sandwich — in the browser

A single-version deployment of **Android Time Machine** by Levente Szabó:
Android 4.0.4 (Ice Cream Sandwich, 2012) on the Galaxy Nexus, rebuilt in
HTML/CSS/JavaScript from the phone's own factory image. No build step, no
server, no network calls at runtime — open the page and the phone starts.

- Live: https://lastmessage-games.github.io/android-4-0-4/
- Original project: https://github.com/szabolevi98/android-time-machine
- Original live demo (all 8 versions): https://android.levente.net/

## What's in this repo

- The complete `versions/4.0.4/` folder from the upstream project, moved to
  the repo root so it serves as the site.
- The shared files that version loads (`boot-ready.js`, `earth-app.js`,
  `earth-globe.js`, `i18n.js`, `mms-prefs.js`, `movie-studio.js`,
  `plus-messenger.js`, `plus-post.js`, `state.js`, `strings.js`,
  `favicon.svg`), plus the shared sound files (`assets/audio/`, the image's
  own ringtones/alarms) and the Earth globe texture (`assets/earth/`).
- `og-cover.jpg` for link previews.

Small, deliberate changes vs upstream (nothing else touched):

- All `../../` paths were rewritten to `./` so the version works at the site
  root instead of under `versions/4.0.4/`.
- The header "← VERSIONS" back-link now points to the upstream repository
  (there is no version picker on this single-version site).
- Open Graph tags point at this deployment's URL.

## License

This work is licensed under the **GNU Affero General Public License v3.0
(AGPL-3.0-only)** — see `LICENSE`. The Android system artwork, sounds and
texts reproduced here come from the Galaxy Nexus factory image (AOSP,
Apache-2.0) — see `THIRD_PARTY_NOTICES.md`.

Per AGPL §13, using a modified version over a network requires offering the
complete corresponding source: this public repository is that offer.

## Run it locally

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
