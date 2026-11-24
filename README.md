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
