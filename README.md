# Aurevia Estates: fictional portfolio website

A static website (HTML, CSS, JavaScript). No build step, no server and no database. Every company, listing, person, price and contact detail is fictional.

## Files

| File | Purpose |
|---|---|
| `index.html` | The site's single entry page (all pages render inside it) |
| `styles.css`, `script.js` | Design system, data, pages and interactions |
| `images/` | All photography (31 JPEGs) |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` | Browser tab and home-screen icons |
| `og-image.jpg` | Social sharing preview (1200x630) |
| `404.html` | Not-found page used by Netlify, Vercel, GitHub Pages, Cloudflare Pages |
| `robots.txt`, `sitemap.xml` | Search engine files |
| `_headers`, `vercel.json` | Optional security and caching headers (Netlify / Cloudflare Pages, Vercel) |
| `.nojekyll` | Tells GitHub Pages to serve files as they are |

Keep the folder structure exactly as it is. `index.html` loads `styles.css`, `script.js` and `images/` by relative path.

## Before you publish: replace the placeholder

Search for `YOUR-DOMAIN.com` in `index.html`, `robots.txt` and `sitemap.xml`, and replace it with your real address (for example `https://aurevia-demo.netlify.app`). Social previews need the full address in `og:image`.

## Deploy

**Netlify (easiest):** go to app.netlify.com/drop and drag the whole folder onto the page.

**Cloudflare Pages:** Create a project, choose "Upload assets", and upload the folder. No build command.

**Vercel:** `npx vercel` inside the folder, or import the folder from a Git repository. Framework preset: Other, no build command, output directory `.`.

**GitHub Pages:** push the folder contents to a repository, then Settings > Pages > Deploy from branch > `main` / root.

**Traditional hosting (cPanel / FTP):** upload everything into `public_html` (or your site's root folder). `_headers`, `vercel.json` and `.nojekyll` are ignored there and can be left out.

## Things to know

- **Navigation** uses `#/page` links (for example `/#/properties`), so the site works on any host without server settings. Search engines treat it as one page. For full per-page SEO, the site would need separate HTML files.
- **Forms** (inquiry, contact, newsletter) validate and show a success message, but send nothing. Connect a service such as Formspree or Netlify Forms if you need real submissions.
- **Fonts** (Cormorant Garamond, Manrope, Pinyon Script) load from Google Fonts. Self-host them if you need to avoid third-party requests.
- **Images** are AI-generated. Keep the "fictional portfolio demonstration" notices in place.
- Preview locally with `python3 -m http.server` inside the folder, then open http://localhost:8000.
