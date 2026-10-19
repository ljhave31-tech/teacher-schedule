# Teacher Schedule [PH - VN]

A single-page schedule app that can be installed on a phone's home screen.

## Put it online with GitHub Pages
1. Create a new repository on GitHub and upload everything in this folder (keep the `icons` folder).
2. Open **Settings → Pages**, set **Source** to *Deploy from a branch*, choose `main` and `/ (root)`, then Save.
3. After a minute your app is live at `https://YOUR-NAME.github.io/YOUR-REPO/`.

## Add it to the home screen
- **iPhone / iPad (Safari):** open the link, tap **Share → Add to Home Screen**.
- **Android (Chrome):** open the link, tap **⋮ → Install app** (or *Add to Home screen*).

## Updating
Upload the changed files to GitHub. If devices keep showing the old version, change `CACHE = 'teacher-schedule-v1'` in `sw.js` to `v2`.

Note: schedules are saved in each device's own browser storage, so they are not shared between phones.
