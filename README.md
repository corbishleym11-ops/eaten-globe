# Everywhere I've Eaten — 3D globe

A single static page (`index.html`) with all place data embedded. No build step, no API keys.
`places.json` / `extras.json` are the same data as plain files (no dollar amounts) in case you want to reuse them.

## Deploy (pick one)

**GitHub Pages (recommended, permanent free URL)**
1. Create a new public repo on github.com (e.g. `eaten-globe`).
2. Upload the files in this folder (drag & drop on the repo page → "Add file" → "Upload files" → Commit).
3. Repo → Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder: `/ (root)` → Save.
4. After ~1 minute the site is live at `https://<your-username>.github.io/eaten-globe/`.

**Vercel**
- With a GitHub repo: vercel.com → Add New → Project → Import the repo → Deploy (framework preset "Other", no build command). Done.
- Without GitHub: `npx vercel --prod` from inside this folder (logs you in, then gives you a URL).

**Fastest possible (no account needed to test)**
- Drag this folder onto https://app.netlify.com/drop

## Notes
- Pins are at city level (statements don't include street addresses). Pins marked ◌ are best-guess locations
  (merchant matched from an earlier statement, or defaulted to Raleigh when the 2025–26 spending reports gave no city).
- Map tiles come from OpenFreeMap (free, no key) with a fallback to MapLibre demo tiles.
