# Pomodoro GP

A race-inspired pomodoro flip-clock timer. One self-contained HTML file — no build step, no backend, no dependencies — plus a small PWA shell so it installs as an app and works offline.

**Focus stints** run a glowing car around a pseudo-3D Monaco street circuit at realistic race pace, with tyre degradation, live lap times and a lap counter. **Breaks** are a single slow cooldown lap. Complete your race and you get the chequered flag, a finish fanfare and confetti. Five livery color themes (or Random for a new one each stint), a five-light start sequence, adjustable stint/break lengths (editable mid-run), and a split-flap clock in the classic style.

## Run it

Open `index.html` in any modern browser. That's it. The layout adapts from desktop down to phones.

## Install it as an app

Once hosted (see below), the site is a PWA: it works offline and installs like a native app. On iPhone/iPad: Share → **Add to Home Screen** — it then opens full-screen with no browser toolbar (which also gives the layout the whole display, and stops Safari evicting a loaded custom font). On Android or desktop Chrome: use the **Install** prompt in the address bar. For this to work, `manifest.webmanifest`, `sw.js` and the `icon-*.png` files must sit next to `index.html`. Updates you push still reach installed users normally — page loads go network-first, the cache is only a fallback for offline.

## Before you publish

`index.html` references the social preview image at `https://YOUR-USERNAME.github.io/pomodoro-gp/social-card.png` (two places in the `<head>`). Replace `YOUR-USERNAME` with your GitHub username — and the repo name if you called it something other than `pomodoro-gp` — so shared links on Reddit, X and Discord show the preview card. Upload everything in this folder next to `index.html`: `social-card.png`, `manifest.webmanifest`, `sw.js`, `icon-180.png`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `LICENSE`, `OFL.txt`.

## Host it (free)

1. Put this folder in a public GitHub repository.
2. Repository → Settings → Pages → deploy from branch → root.
3. Your timer is live at `https://<you>.github.io/<repo>/`.

Cloudflare Pages and Netlify work identically (drag-and-drop the folder). All three serve over HTTPS automatically.

## Privacy

No accounts, no cookies, no analytics, no tracking. Preferences (durations, theme, sound) are stored in the visitor's own browser via `localStorage` and never leave it. The service worker caches the app in the visitor's browser for offline use; it talks only to this site's own files.

## Fonts

The bundled display face, "PW Display", is a modified build of [Titillium Web](https://fonts.google.com/specimen/Titillium+Web) Black (a slashed zero was added for the timing-screen look); labels use Titillium Web SemiBold. Both are used and redistributed under the SIL Open Font License 1.1 — see `OFL.txt`; the derivative keeps the OFL and drops the reserved "Titillium" name as the license requires. No proprietary fonts are distributed with this site. Two ways to see a different display face:

- If a visitor has a display font **installed on their own computer** under the name "Formula1 Display Black", the page uses it automatically (via CSS `local()` — nothing is downloaded or distributed).
- Race Setup → **Display font → Load file** lets a visitor load any font file they own; it is stored only in their own browser and never uploaded anywhere.

## Licenses & credits

- **Code**: MIT — see `LICENSE`.
- **Typeface**: Titillium Web by the Accademia di Belle Arti di Urbino, embedded (subset) under the SIL Open Font License 1.1 — see `OFL.txt`.
- **Circuit outline**: derived from [F1-Track-Layouts-SVG](https://github.com/MasterPlay007/F1-Track-Layouts-SVG), released under CC0 1.0 (public domain). Credit given with thanks.
- Sounds and all other artwork are generated in-project.

## Disclaimer

Pomodoro GP is an unofficial fan project. It is not affiliated with, endorsed by, or connected to Formula 1, Formula One Licensing B.V., the FIA, the Automobile Club de Monaco, or any racing team. Team names appear only to identify which team's colors a theme refers to; no logos or other marks are used, and no sponsorship or endorsement is implied.
