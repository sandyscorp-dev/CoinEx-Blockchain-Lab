# CoinEx Blockchain Lab Inauguration — Report Site

This folder is a ready-to-deploy static site: `index.html` plus a `videos/` folder
with the 4 event clips as real .mp4 files (no base64 embedding). Total size ~35MB.

## Deploy with GitHub Pages (no coding required)

1. Go to https://github.com/new and create a new repository
   (e.g. `coinex-blockchain-lab-report`). Public repo, no README/template needed.
2. On the new repo's page, click **"uploading an existing file"**
   (or use "Add file" → "Upload files").
3. Drag in everything from this folder — `index.html`, the `videos/` folder,
   and this `README.md` — and commit.
4. Go to the repo's **Settings → Pages**.
5. Under "Build and deployment" → "Source", choose **Deploy from a branch**.
6. Branch: `main`, folder: `/ (root)`. Click **Save**.
7. GitHub will give you a URL like:
   `https://<your-username>.github.io/coinex-blockchain-lab-report/`
   It usually goes live within 1-2 minutes.

## Alternative: git command line

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then enable Pages the same way (step 4-6 above).

## Why this version is better than the downloaded HTML file

The version you've been testing on your phone has all 4 videos embedded
directly as base64 text inside the HTML (~55MB file, no real video
streaming). This site version instead links to real .mp4 files sitting
next to the page — this is exactly how normal websites serve video, so
it loads faster, plays instantly, and Safari/Chrome will handle seeking
and buffering properly instead of trying to decode one giant embedded blob.
