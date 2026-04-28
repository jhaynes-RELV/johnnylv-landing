# Johnny Haynes — Las Vegas Realtor® Landing Page

A single-file static landing page that links each property card to its full listing on JohnnyLV.com.

## What's in the box
- `index.html` — the entire site (HTML, CSS, JS in one file)
- `vercel.json` — a tiny Vercel config (clean URLs, no trailing slash)
- `README.md` — this file

## Easiest way to deploy on Vercel (no Git required)

1. Go to https://vercel.com/new
2. Sign in (free Hobby plan is fine)
3. Click **"Deploy without Git" / "Other"** → upload this whole folder (or its zip)
4. Vercel auto-detects it as a static site and gives you a live URL in ~30 seconds
5. Click **"Domains"** to point your custom domain (e.g., a subdomain of johnnylv.com) at it

## Deploy via GitHub (recommended if you want easy edits)

1. Create a new repo on GitHub and upload these files
2. Go to https://vercel.com/new and import the repo
3. Click **Deploy** — done. Future commits auto-deploy.

## Deploy via Vercel CLI (for power users)

```bash
npm i -g vercel
cd johnnylv-landing
vercel        # follow prompts, choose "static"
vercel --prod # promote to production
```

## How to update content
Open `index.html` in any text editor. Each property is a `<a class="card">` block — easy to find.

To add a real photo, replace the `<div class="card-img alt-N">` block with:

```html
<div class="card-img" style="background-image:url('YOUR_PHOTO_URL'); background-size:cover; background-position:center;">
  <span class="pill sale">For Sale</span>
</div>
```

To swap the contact info, search for `(702) 600-0288` or `johnny@johnnylv.com` and replace.

## Notes
- The page uses Google Fonts (Inter + Fraunces) loaded from a CDN. No build step needed.
- The colored gradient "photo" placeholders are intentional — they look polished even before you drop in real photos.
- All listing links open in a new tab (`target="_blank"`).
