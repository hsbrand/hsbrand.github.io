# Hockey Stock website

Production-oriented Jekyll site for hsbrand.ca.

## GitHub Pages setup

1. Copy all files into the root of `hsbrand/hockeystock`.
2. Commit and push to the default branch.
3. In GitHub: **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Select the default branch and `/ (root)`.
5. Configure the custom domain as `hsbrand.ca`.

## Brand logo

The current build uses:

`assets/images/brand/hockey-stock-mark.jpg`

To replace it with the SVG, save the SVG as:

`assets/images/brand/hockey-stock-logo.svg`

Then replace the three references to `hockey-stock-mark.jpg` in:

- `_includes/header.html`
- `index.html`
- `about.md`

## Product images

Use the established naming pattern inside each design folder. Lifestyle image `-01` is the hero.

Example:

- `assets/images/designs/hs-001/hs-001-lifestyle-01.jpg`
- `assets/images/designs/hs-001/hs-001-lifestyle-02.jpg`
- `assets/images/designs/hs-001/hs-001-colourways-01.jpg`
- `assets/images/designs/hs-001/hs-001-garment-image.jpg`

Missing images display branded placeholders automatically.

## Add a future design

Duplicate a file in `_designs`, update its front matter and text, then add the matching image folder. Design pages and the all-designs archive are generated automatically.
