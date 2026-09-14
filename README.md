# Botanica · Prana — preview builds

Four static builds of the same landing page, published with GitHub Pages.

| Page | What differs |
|---|---|
| [`/band/`](band/) | A brochure-style shop band pinned down the right edge, on screen at all times. |
| [`/pull-tab/`](pull-tab/) | The shop hides behind a frosted tab on the right edge. Hover or click it to open. |
| [`/bottle-button/`](bottle-button/) | A floating bottle button, bottom right, opening a cart drawer. |
| [`/static/`](static/) | Nothing follows the scroll wheel: both films play by themselves and the shop shows stills. |

Everything is static: HTML, CSS, JS and media. No build step, no backend.

## Running it locally

The pages fetch video files, which browsers block on a `file://` page, so use
any static server from the repo root. For example:

```
python -m http.server 8000
```

then open <http://localhost:8000/>.

## Notes

- The repo is public because GitHub Pages needs that on a free plan. Every page
  sends `noindex, nofollow` and `robots.txt` disallows crawling, so the site is
  reachable by link but should stay out of search results.
- The Journey film is embedded from YouTube; the two fonts load from Fontshare
  and Google Fonts. Everything else is served from this repo.
- "Add to cart" links point at the live Botanica store.
