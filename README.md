# Tree of Life Consulting, LLC — Website

Static marketing site for Tree of Life Consulting: whole-person coaching and
practical HR / business consulting. No build step, no framework — plain HTML,
one shared stylesheet and one shared script, deployed on Netlify.

## Stack

- Static HTML (8 pages), `styles.css`, `main.js`
- Forms via **Netlify Forms** (contact, guide, booking) + honeypot spam trap
- Hosting via **Netlify**, config in `netlify.toml`

## Structure

| Path | Purpose |
|---|---|
| `index.html` | Home (hero, services, founder, testimonials, lead magnet, how it works) |
| `about.html` | Founder story, name, credentials |
| `coaching.html` | 1:1 coaching packages |
| `programs.html` | Group programs (Lead and Belong, CQ team workshop) |
| `consulting.html` | HR & business consulting + case study |
| `contact.html` | Contact form (`contact`) |
| `booking.html` | In-app booking form (`booking`): date, time slot, auto-detected timezone stored as UTC (`utc_datetime`), phone with country code, country/city/region |
| `privacy.html` | Privacy policy |
| `assets/` | Logos and icons (PNG) shared by all pages |
| `styles.css` / `main.js` | Shared styles and behaviour (preloader, scroll reveal, mobile menu) |
| `netlify.toml` | Publish dir, security headers, cache rules |
| `robots.txt` / `sitemap.xml` | SEO (`https://treeoflife-consulting.com`) |

## Local preview

Any static server works, from the repo root:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

Note: Netlify Forms submissions only work on the deployed site, not locally.

## Deploy on Netlify

1. Connect this repo in Netlify (no build command, publish directory `.`).
2. After deploy, check **Forms** — `contact`, `guide` and `booking` must be listed as active.
3. Enable form notification emails and the spam filter in site settings.
4. Add the custom domain `treeoflife-consulting.com` and enable HTTPS (DNS as instructed by Netlify).

Success handling is in-page via query params: `?ok=1` (contact),
`?guide=ok` (guide), `?booked=1` (booking).

## License

© 2026 Tree of Life Consulting, LLC. All rights reserved.
