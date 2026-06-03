# Diet Plan Tracker — PWA

A private, offline, installable app that tracks your exact 90-day diet
routine (meals, workouts, water, steps, sleep, supplements, wellbeing ratings, cheat days).
All data stays on your device — no login, no servers, nothing uploaded.

## Files
- `index.html` — the whole app (plan data + Chart.js are inlined, so it works offline)
- `manifest.json` — makes it installable to your home screen
- `sw.js` — service worker for offline use
- `icon-192.png`, `icon-512.png` — app icons

## How to run it

A PWA must be served over **https** (or `localhost`) for install + offline to work.
You can't just double-click `index.html` and get the install prompt — it needs a host.

### Easiest free options (no coding)
1. **Netlify Drop** — go to app.netlify.com/drop and drag this whole folder in.
   You get a live https link in seconds. Open it on your phone and install.
2. **GitHub Pages** — push this folder to a repo, enable Pages. (You already have a
   GitHub account, so this fits your setup.)
3. **Vercel** — import the folder, deploy.

### Quick local test on a computer
```
cd glow-plan-pwa
python3 -m http.server 8000
```
Then open http://localhost:8000 in Chrome.

## Install on your phone
- **Android (Chrome):** open the link → menu (⋮) → **Add to Home screen**.
- **iPhone (Safari):** open the link → Share → **Add to Home Screen**.

After installing, it runs full-screen and works with no internet.

## First-time setup
1. Open **More** tab → set your **Start date (Day 1)**. Everything (which day's meals,
   the weight target line, cheat days) is calculated from this.
2. Optionally turn on **Reminders** and tap **Enable notifications**.
   (Note: in-app reminders fire while the app has been opened that day; full background
   push is limited by the browser, especially on iPhone.)

## Using it day to day
- **Today** tab: tap ✓ Done / ✎ Modified / ✕ Skip on each meal, the workout, and
  supplements. Tap water drops, type steps + sleep, rate skin/energy/mood. The ring
  shows your adherence %; an 80%+ day keeps your streak alive.
- **History** tab: month calendar, colored dot per day. Tap any day to open it.
- **Progress** tab: weight vs. target line, 14-day adherence bars, glow trend, and a
  weekly weigh-in box.
- **More** tab: reminders, start date, CSV export, JSON backup/restore, reset.

## Back up your data
Because data lives only on the device, use **More → Back up all data (JSON)** now and
then, and restore it if you change phones.

---
General wellness tool, not medical advice. Given hypothyroidism, confirm anything
significant with your doctor or a registered dietitian.
