# Gridiron Tracker

A private, offline macro/calorie tracker built for football season (target: **Aug 12, 2026**).
No accounts, no cost, no internet needed. Your data stays in your browser.

## How to open it
1. Go to the `health/tracker` folder on your PC.
2. Double-click **`index.html`**. It opens in your browser. That's it.
3. Fill in **Your Profile** → tap **Save & calculate targets**. Your daily calorie + macro
   goals appear at the top.
4. Log food throughout the day. Watch the progress bars fill.

## Files (what each one is)
- `index.html` — the whole app (screen + logic). This is the one you open.
- `manifest.webmanifest` + `icon.svg` — make it installable as a phone app.
- `sw.js` — lets it work offline once it's hosted.
- `README.md` — this file.

## Publish it free with GitHub (auto-updates, phone install, barcode scanning)
Barcode scanning uses your camera, and browsers only allow the camera on a real web
address (`https://`). Hosting on GitHub means that whenever the app files change, you
push the update and it goes live automatically — no re-uploading. All free.

### One-time setup (~10 minutes, no coding)
1. **Make a GitHub account** (free): github.com → Sign up.
2. **Install GitHub Desktop** (free app): desktop.github.com → install → sign in.
3. **Add this folder as a repository:**
   - GitHub Desktop → **File → Add local repository**
   - Choose this folder: `…/Disce aut discede/health/tracker`
   - It says "this isn't a repository yet — create one." Click **Create a repository**.
   - Name it e.g. `gridiron-tracker`. Click **Create repository**.
4. **Publish it:** click **Publish repository** (top bar).
   - **Uncheck "Keep this code private"** (free GitHub Pages needs a public repo — the app
     has no secrets, it's fine). Click **Publish repository**.
5. **Turn on the website (GitHub Pages):**
   - On github.com, open your `gridiron-tracker` repo → **Settings** → **Pages** (left menu)
   - Under **Source**, pick **Deploy from a branch** → Branch: **main**, folder: **/ (root)** → **Save**
   - Wait ~1 minute, refresh. It shows: *"Your site is live at
     `https://YOURNAME.github.io/gridiron-tracker/`"* — that's your app URL.
6. **Put it on your iPhone:** open that URL in **Safari** → **Share** → **Add to Home Screen**.
   Open it from the icon → **📷 Scan a barcode** → **Allow** camera → scan.

### Pushing updates later (when the app improves)
The app files live in OneDrive, so Claude's changes sync to your PC automatically. Then:
1. Open **GitHub Desktop** — you'll see the changed files listed.
2. Type a short note (e.g. "add lifting program"), click **Commit to main**.
3. Click **Push origin**. ~1 minute later the live site updates itself. Done.

> Keep OneDrive running so file changes sync before you commit. Data is stored per web
> address — use the GitHub URL as your real tracker. Move data between versions with the
> **Export / Import backup** buttons.

### Quick alternative (no GitHub)
Prefer zero setup? Go to **app.netlify.com/drop** and drag the `tracker` folder on — instant
link. Downside: you must re-drag the folder each time the app changes. GitHub avoids that.

## Barcode scanning — how it works
- Tap **📷 Scan a barcode** in the Log Food card, point at a packaged food's barcode.
- It looks the product up in **Open Food Facts** (a free, open database) and fills in the
  calories and macros. Adjust **Servings** to match how much you ate.
- Whole foods (chicken, rice, banana) don't have barcodes — use the **search library** for those.
- Scanning needs internet; the rest of the app works offline.

## Backup
Your data lives in this browser only. Use **Export backup** now and then to save a `.json`
file (drop it in this folder). **Import backup** restores it on any device.

## Roadmap
- **Phase 1 (done):** macro & calorie tracker, body-weight trend, backup.
- **Phase 2:** 5-day skill-position lifting program, checkable workouts, weight logging.
- **Phase 3:** history charts, saved meals, phone install.
