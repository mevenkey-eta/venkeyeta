# Venkey.me — Cloudflare Pages Production Package

This is a production-ready static website package derived from the supplied HTML profile.

## Package
- `index.html` — production homepage
- `favicon.svg` — local favicon
- `_headers` — basic security headers
- `_redirects` — Cloudflare Pages fallback
- `assets/` — reserved for future local assets

## Cloudflare Pages — Direct Upload

1. Open Cloudflare Dashboard.
2. Go to **Workers & Pages → Create application → Pages → Upload assets**.
3. Create a new Pages project.
4. Upload the contents of this folder (or upload the ZIP package).
5. No build command is required.
6. Set the output directory to the uploaded site/root if Cloudflare asks.
7. Deploy.
8. Add your production domain, e.g. `venkey.me`.
9. In DNS, use Cloudflare's requested records/nameservers for the domain.

## Cloudflare Pages — Git Deployment

If you later put these files into GitHub:
- Framework preset: **None**
- Build command: leave blank
- Build output directory: `/`
- Root directory: `/`

Every push can then trigger a new deployment.

## Important
The original HTML was captured from an AIRO preview environment. The production package removes preview/runtime/editor dependencies and converts the preview navigation into stable one-page anchors.

The profile content itself has not been rewritten; this package is intended to preserve the supplied page while making it deployable as a static site.

## Custom domain
Recommended:
- Primary: `https://venkey.me`
- Optional: `https://www.venkey.me` → redirect to the primary domain

## Before launch
- Confirm the domain is pointing to Cloudflare.
- Test all navigation links.
- Test email, phone and LinkedIn links.
- Add a real social preview image later if desired.
- If you add downloadable CV/PDF files, place them in `assets/` and link them from `index.html`.
