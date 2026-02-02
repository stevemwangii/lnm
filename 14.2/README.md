# Lnm (Latifah) — Vercel Deployment Instructions

This is a single-file static site. To deploy on Vercel, include the background image `lnm.jpeg` in the same folder as `Lnm.html` and follow one of the methods below.

Pre-steps (Windows):

1. Copy your image into the project folder:

```bash
copy "E:\\lnm.jpeg" "E:\\14.2\\lnm.jpeg"
```

2. Open a terminal in the project folder:

```bash
cd /d E:\\14.2
```

Option A — Deploy with Vercel CLI (fast):

```bash
npm install -g vercel
vercel login
vercel
```

Follow the interactive prompts. When asked for the project root, accept `.`. Vercel will deploy the static files and serve `Lnm.html`.

Option B — Deploy via Git provider (GitHub/GitLab/Bitbucket):

```bash
git init
git add .
git commit -m "Initial site"
# push to a remote (create repo on GitHub first)
git remote add origin <your-repo-url>
git push -u origin main
```

Then connect the repository in the Vercel dashboard (https://vercel.com/new) and import the project — Vercel will detect a static site and deploy.

Notes and tips:
- Keep `lnm.jpeg` in the same folder as `Lnm.html` so the CSS `url('lnm.jpeg')` works.
- If your browser blocks local audio or file URLs while testing, verify the file paths or host audio in the project folder and update the `<source>` to a local filename (e.g. `love.mp3`).
- The included `vercel.json` ensures the root routes to `Lnm.html`.

If you want, I can add the image and audio files to the project (you'll need to upload them or grant file access). Tell me which option you prefer.

Hosting & sharing (quick guide)

1) Ensure static assets are in the folder:

- Place `lnm.jpeg` in `e:\14.2` (same folder as `Lnm.html`).
- If you want the audio local, copy your MP3 as `love.mp3` into the same folder and update the `<source>` in `Lnm.html` to `love.mp3`.

2) Deploy with Vercel CLI (recommended — gives an immediate shareable link):

```bash
npm install -g vercel
cd /d E:\14.2
vercel login
vercel --prod
```

The `vercel` command will return a deployment URL (example: `https://your-project.vercel.app`). Use that URL to share the page.

3) Deploy via Git provider (GitHub) if you prefer continuous deploys:

```bash
cd /d E:\14.2
git init
git add .
git commit -m "Initial site"
# create a GitHub repo, then:
git remote add origin <your-repo-url>
git push -u origin main
```

Then import the repo in the Vercel dashboard at https://vercel.com/new — Vercel will deploy and give you a shareable URL.

4) Notes & troubleshooting
- If the background image doesn't load, confirm `lnm.jpeg` is present and named exactly `lnm.jpeg`.
- If your browser blocks autoplay for audio, the track may not start until user interaction; consider removing `autoplay` if that behavior is undesirable.
- Attribution: the page includes a visible footer credit for Bensound. If you change the audio source, keep proper attribution as required by the license.

If you want, I can run the exact `vercel` commands for you here (I cannot push to your Vercel account without your login). Tell me when you're ready and I'll guide you interactively through the CLI steps.
