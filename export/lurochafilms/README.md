# LU ROCHA FILMS — Portfolio

Static site. Single HTML entry: `index.html`. Assets live under `assets/`.

## Deploy to Vercel

### Option A — Drag and drop (no CLI)
1. Go to https://vercel.com/new
2. Click **"Browse all templates"** → scroll down, or use the import area
3. Drag this entire folder (or its zip) into the upload zone
4. Pick a project name (e.g. `lurochafilms`)
5. Hit **Deploy** — Vercel auto-detects a static site, no build step needed
6. Your site will be live at `https://<project-name>.vercel.app`

### Option B — Vercel CLI
```bash
npm i -g vercel
cd lurochafilms
vercel        # follow prompts
vercel --prod # to publish to production
```

## Custom domain (later)
After deploy, in the Vercel dashboard:
- Project → Settings → Domains → Add → `lurochafilms.com` (or whichever)
- Update your DNS records as Vercel instructs

## Files
- `index.html` — the portfolio
- `assets/lucas-1.jpg`, `assets/lucas-2.jpg` — your photos used in the contact section
- `vercel.json` — clean URLs + long-cache headers for assets

## Videos
Video thumbnails are pulled live from YouTube (`img.youtube.com`). Clicking a video opens it in a new tab at `youtube.com/watch`. No embed/iframe issues this way.

If you ever want to switch to inline playback, replace `openVideo(id)` (in the `<script>` near the bottom) with a modal that loads `https://www.youtube-nocookie.com/embed/<id>?autoplay=1`. It will work fine on your own domain.

---
© 2026 Lu Rocha Films
