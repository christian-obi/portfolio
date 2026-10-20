# Christian Obi - Portfolio Website

A single-page portfolio showcasing blockchain analytics dashboards and speaking engagements.
Plain HTML + CSS with a small inline script, no build step.

## Live Site

Visit: `https://christian-obi.github.io/portfolio/`

## Features

- Floating glass navigation with scroll-spy and a mobile menu
- Light / dark theme toggle (follows the system setting, remembers the visitor's choice)
- Bento-style hero, about and stats layout
- Project grid with ecosystem filters (Core, NEAR, Monad, Arbitrum)
- Speaking gallery, copy-to-clipboard email, scroll reveal animations
- Respects `prefers-reduced-motion`; keyboard focus styles and a skip link

## Editing Content

All content lives in `index.html`, grouped by section (`#home`, `#about`, `#services`, `#work`, `#speaking`, `#contact`).

### Add a dashboard

Copy one of the `<a class="card project reveal">` blocks inside `#work` and update:
- the GitHub URL
- the image in `images/dashboards/` (16:10, e.g. 1600x1000)
- the tags, title and description
- `data-tags` (lowercase ecosystem name, used by the filter buttons)

### Add a speaking engagement

Copy an `<article class="card talk reveal">` block inside `#speaking`, add the photo to `images/`
(resize to ~1200px on the long side to keep the page fast) and update the event name and details.

### Change colours

Edit the design tokens at the top of `styles.css`: the `:root` block is the dark theme and
`:root[data-theme="light"]` is the light theme. `--brand` and `--accent` drive the gradient.

## Deploying

The site deploys to GitHub Pages from the `main` branch via the workflow in `.github/workflows/`.
