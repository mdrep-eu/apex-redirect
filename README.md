# apex-redirect

Netlify site whose only job is a **301 redirect** from `mdrep.eu` (any path) to `https://www.mdrep.eu` (same path).

- Real website: Cloudflare Pages, repo `mdrep-eu/mdrep-site`.
- DNS: register.it. Record `A mdrep.eu → 75.2.60.5` (Netlify load balancer). `www` is a CNAME to `mdrep-site.pages.dev`.
- Netlify domain settings: only `mdrep.eu` (do **not** add `www.mdrep.eu` here).
- `public/index.html` is a fallback; the redirect itself is in `netlify.toml` (`force = true`).

Nothing to change here unless the canonical domain changes.
