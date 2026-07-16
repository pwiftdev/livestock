# 🐄 LIVESTOCK — Genuinely Tokenized

The world's first real world asset with a heartbeat and a tail. A single-page, dependency-free
scroll experience: raise the sun, reveal the farm, meet the herd.

Built as one static `index.html` — no build step, no framework, no bundler. GSAP is loaded from a CDN.

## Local preview

Just open `index.html` in a browser. Or serve it:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Deploy to Vercel

This is a static site, so Vercel needs **zero configuration**.

**Option A — dashboard (easiest):**
1. Push this repo to GitHub (see below).
2. Go to vercel.com → **Add New… → Project** → import the GitHub repo.
3. Framework Preset: **Other**. Build Command: *(leave empty)*. Output Directory: `./`.
4. **Deploy.**

**Option B — Vercel CLI:**
```bash
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

## Structure

```
livestock/
├── index.html      # the whole site
├── vercel.json     # minimal static config
├── .gitignore
└── README.md
```

## Notes

- Falls back gracefully with reduced-motion enabled or if the GSAP CDN fails to load
  (renders the fully-assembled daytime farm).
- Drop your Solana contract address into the `#addr` element in `index.html` before launch.
