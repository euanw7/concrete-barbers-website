# concrete-barbers-website

One-page website for **Concrete Barbers**, Caerphilly, served by GitHub Pages.
Plain HTML/CSS/JS with no build step.

- `docs/index.html`: the page (hero, about, prices per barber, team, gallery, reviews, find us)
- `docs/css/style.css`: styles (brand colours are CSS variables at the top)
- `docs/js/main.js`: mobile menu, price tabs, gallery lightbox
- `docs/assets/img/`: logo, team and work photos (taken from the shop's Booksy listing, resized for web)

All links are relative, so the site works both at the GitHub preview URL and on a custom domain.

## Preview locally

```sh
cd docs && python3 -m http.server 8000
# open http://localhost:8000
```

## Deploying on GitHub Pages

1. Push `main` to GitHub.
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*,
   Branch = `main`, folder = `/docs`.
3. Preview at `https://euanw7.github.io/concrete-barbers-website/`.

### Custom domain (when one is ready)

1. Add `docs/CNAME` containing the domain (or set *Custom domain* in Settings → Pages).
2. At the DNS provider: apex `A` records → `185.199.108.153`, `185.199.109.153`,
   `185.199.110.153`, `185.199.111.153`, and `www` `CNAME` → `euanw7.github.io`.
3. Once the certificate is issued, tick **Enforce HTTPS**.

## Common edits

| Change | Where |
|---|---|
| Booking link | Search `index.html` for `booksy.com/en-gb/113641` (used by every Book button) |
| Prices | The `price-list` blocks under `<!-- SERVICES -->` in `index.html`, one panel per barber |
| Add or remove a barber | A tab button, a `panel`, and a `barber` card in `index.html`, plus a photo in `assets/img/` |
| Opening hours | `<!-- TODO -->` under "Opening hours" in `index.html` |
| Review count/rating | Hero `rating-chip` and the `reviews` section in `index.html` |
| Colours/fonts | `:root` variables at the top of `css/style.css` |

## Still to confirm with the client

- **Opening hours**: Booksy didn't show weekly hours, so the page says hours vary by barber.
- **Booking system**: Booksy has a note about moving bookings to an `s-iq.co` booking portal.
  The site links to Booksy for now.
- **Phone number / email**: none published on Booksy.
- **Permission to use photos**: images come from the shop's own Booksy profile.
- **Review figures** (5.0 from 583) are a snapshot from November 2026 and need updating by hand.
