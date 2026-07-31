## SnackTrack


A daily nutrition log (Norwegian language) styled as a running grocery receipt. Type what you ate in plain language — Gemini estimates the calories, protein, fat, and carbs for you.

Built as a lightweight, installable PWA. No backend, no accounts, no tracking. Everything runs in your own browser.

**Live app:** https://joachim911.github.io/snacktrack/

## Features

-  **Receipt-style daily log** — each day gets its own running "receipt," browsable with the arrows at the top
-  **Free-text logging** — write things like `400g yoghurt naturell` or `2 kyllingfileter`, no manual macro lookup needed
-  **AI-powered estimates** — uses your own free Google Gemini API key to estimate nutrition per entry
-  **Live totals** — calories, protein, fat, and carbs update automatically as you log
-  **Installable PWA** — add it to your home screen and it behaves like a native app, works offline for viewing past logs
-  **100% local data** — everything is stored in your browser's `localStorage`; nothing is ever sent to a server except the nutrition-estimate request (which goes straight to Google, not through this repo)
-  **Export / Import** — back up your full log as a CSV file, and restore it later on any device

## Getting started

### 1. Get a free Gemini API key
Go to [aistudio.google.com/apikey](https://aistudio.google.com/apikey), sign in, and click **Create API key**. No credit card required for the free tier.

### 2. Open the app
Visit the live link above (or your own fork's GitHub Pages URL), tap **API-nøkkel** at the top, and paste in your key. It's saved only on your device.

### 3. Install it (optional, recommended)
In Chrome (Android) or Safari (iOS), open the site and choose **Add to Home Screen**. SnackTrack now launches like a regular app, with its own icon and no browser bar.

### 4. Log something
Type what you ate and hit **+**. Each entry gets parsed into name, quantity, and macros automatically.

## Data & privacy

- All log entries live in your browser's local storage only — not in this repository, not on any server
- The only network request the app makes (besides loading the page itself) is directly to Google's Gemini API, using your own key
- Clearing your browser data, switching browsers, or switching devices will erase your local log — use **Eksport** regularly to keep a CSV backup, and **Import** to restore it

## Tech stack

Plain HTML, CSS, and JavaScript — no build step, no framework, no dependencies. A service worker caches the app shell for offline use. Deployed via GitHub Pages.

## Deploying your own copy

1. Fork this repository
2. In **Settings → Pages**, set the source to deploy from the `main` branch, root folder
3. Your app will be live at `https://<your-username>.github.io/<repo-name>/`

## License

Personal project, shared as-is for anyone who wants to fork or adapt it.
