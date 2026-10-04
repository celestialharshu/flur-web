# Flur website

Static site (no build step). Files:

- `index.html` — the whole site
- `logo.svg` — app icon / favicon
- `vercel.json` — Vercel config
- `downloads/` — put your installer here as `Flur-Setup.msi`

## Add your installer

Copy your `.msi` into `downloads/` and name it `Flur-Setup.msi`.
If your file has a different name, search `index.html` for `/downloads/Flur-Setup.msi` (2 places) and change it.

**Large file?** Vercel allows files up to 100 MB per deployment file. If your .msi is bigger, upload it to a
GitHub Release and replace both links with the release URL.

## Deploy on Vercel

Option A — drag and drop / CLI:
1. `npm i -g vercel`
2. In this folder run `vercel` then `vercel --prod`

Option B — GitHub:
1. Push this folder to a GitHub repo
2. Vercel → Add New → Project → import the repo
3. Framework Preset: **Other**, no build command, output directory blank → Deploy
