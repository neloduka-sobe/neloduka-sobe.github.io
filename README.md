# neloduka-sobe.github.io

Personal portfolio for Borys Łangowicz. Plain HTML, CSS, and a few dozen lines of vanilla JS — no framework, no build step, no dependencies to install or break.

## Structure

```
index.html      the whole site (single page)
css/tokens.css  design tokens (colour, type, spacing)
css/style.css   page styles
js/main.js      scroll-reveal only; site is fully usable without it
img/            photos, served as WebP with JPEG fallback
```

## Running locally

Any static file server works, e.g.:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploying

GitHub Pages serves this repo directly — no build step. In the repo's **Settings → Pages**, set the source to "Deploy from a branch" → this branch → `/ (root)`. The `.nojekyll` file at the root tells GitHub Pages to skip Jekyll processing entirely.

## Editing content

All content lives directly in `index.html`. There's no CMS or data file — update the markup in place.
