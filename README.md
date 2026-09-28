# Dan's Glasses Web Apps

Simple web apps for Meta Ray-Ban Display glasses (developer mode).
Built 2026-09-28. All pages are 600x600, dark UI, D-pad / arrow-key navigation.

## Files

- `index.html` — app launcher (YouTube / Maps / Facebook)
- `youtube.html` — YouTube search + in-lens video player (needs a free YouTube Data API v3 key, entered once in the app's ⚙ API key panel)
- `maps.html` — map with phone GPS location, place search, D-pad pan/zoom (OpenStreetMap data via CARTO dark tiles — Google doesn't offer a keyless embed that works on glasses)
- `facebook.html` — quick links to the mobile Facebook site (login required in the glasses browser)

## Hosting (pick one, then paste the URL into the Meta AI app)

**Option A — Netlify Drop (no account needed):**
1. On your phone or computer, go to https://app.netlify.com/drop
2. Drag this whole folder onto the page
3. You get a public URL like `https://your-site-name.netlify.app`

**Option B — GitHub Pages (needs a GitHub account):**
1. Create a repo, upload these files
2. Settings → Pages → Deploy from branch → main → Save
3. Your URL: `https://YOUR-USERNAME.github.io/REPO-NAME/`

## Adding to the glasses

1. Meta AI app → Devices → your Display glasses → settings
2. App connections → Web apps → **Add a web app**
3. Name: "Dan's Apps", URL: your hosted `index.html` URL (e.g. `https://your-site-name.netlify.app/index.html`)
4. Open it from the glasses app list

(Developer mode must be on: Meta AI app → Settings → App Info → tap App version 5 times → Enable. Already done on Dan's pair.)

## Notes

- YouTube search uses the YouTube Data API (free tier: ~100 searches/day). Get a key: console.cloud.google.com → new project → enable "YouTube Data API v3" → Credentials → API key.
- Facebook links open Facebook's real mobile pages — usable, but not redesigned for the lens.
- Tesla: not included — Tesla requires official OAuth login through a Tesla developer app, which can't be a simple static page. Possible as a later project.
- Driving directions are not supported on the Display glasses (Meta's own nav is walking-only); the Maps app shows your location and places.
