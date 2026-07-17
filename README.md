# Arup "Abhi" Datta — Portfolio Site

A static, single-page portfolio site. No build step, no dependencies — just HTML/CSS/JS.

## Files

- `index.html` — the site
- `profile.jpg` — profile photo / favicon
- `Arup_Datta_Resume.pdf` — downloadable résumé (linked from the site)
- `vercel.json` — deployment config (clean URLs + asset caching)

Keep all four files together in the same folder — the page references the image and PDF by relative path.

## Deploy to Vercel

### Option A — Vercel dashboard (no install required)
1. Go to https://vercel.com/new
2. Choose **"Deploy without Git"** and drag this whole folder onto the upload area
   (or click "Browse" and select all files in this folder)
3. Framework preset: **Other** (Vercel should auto-detect this)
4. Click **Deploy**

### Option B — Vercel CLI
```bash
npm i -g vercel      # if you don't already have it
cd portfolio-vercel  # this folder
vercel                # first deploy (follow the prompts)
vercel --prod          # promote to production
```

### Option C — GitHub + Vercel (recommended for future edits)
1. Create a new GitHub repo and push this folder's contents to it:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. Go to https://vercel.com/new, click **"Import Git Repository"**, and select the repo
3. Framework preset: **Other** — no build command, no output directory needed
4. Click **Deploy**

Once deployed, Vercel gives you a `*.vercel.app` URL immediately, and you can attach a custom domain from the project's **Settings → Domains** tab.

## Making edits later
This is plain HTML/CSS/JS in a single `index.html` file — open it in any text editor, make changes, and redeploy (`vercel --prod`, or just push to GitHub if you used Option C for automatic redeploys).
