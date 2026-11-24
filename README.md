# Ambucore Ambulance Services: website redesign

Single-page static site for Ambucore Ambulance Services (Quezon City, PH).
Replaces the current GoDaddy Website Builder site at ambucoreambulance.com.

## Files
- `index.html`: the whole site (HTML, CSS and JS in one file)
- `_headers`: Cloudflare Pages headers (currently blocks search indexing for the preview)
- `robots.txt`: currently disallows all crawlers (preview stage)

## Deploy (Cloudflare Pages)
1. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git → pick this repo.
2. Framework preset: **None**. Build command: *(leave empty)*. Output directory: `/`.
3. Deploy. Every push to `main` redeploys automatically.
4. Optional: add a custom domain, e.g. `ambucore.preview.<yourdomain>`.

## Before going live
- [ ] Download the photos (currently loaded from img1.wsimg.com) into `/images` and update the `src` paths. They'll break once the GoDaddy site is cancelled.
- [ ] Replace the example training courses (marked `EDIT` in index.html) with Ambucore's real courses.
- [ ] Remove the `X-Robots-Tag` line from `_headers` and change `robots.txt` to allow crawlers.
- [ ] Point ambucoreambulance.com DNS to Cloudflare Pages.
- [ ] Hook the quote form to a real form handler (currently opens the visitor's email app).
