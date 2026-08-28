# studioanima.io

The live site. This repository is the single source of truth for
<https://studioanima.io> — there is no separate source repo and no build step.

## Changing the site

1. Edit `index.html` (or `404.html`).
2. Commit to `main`.

GitHub Pages rebuilds and deploys automatically, usually within a minute.
That's the whole process — nothing to copy from anywhere else.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire page — self-contained: CSS, JS and images inline |
| `404.html` | Not-found page, served by Pages with a real HTTP 404 |
| `og.jpg` | Social share image, 1200×630 |
| `CNAME` | Custom domain. **Do not edit or delete** — see below |

## Things worth knowing

- **`CNAME` is load-bearing.** It contains `studioanima.io` and is what makes
  the custom domain and its TLS certificate work. Removing it drops the site
  back to the `github.io` address and forces certificate re-issuance.
- **The page is dark-first.** The LIGHTS toggle overrides, and the choice is
  remembered per visitor in their own browser.
- **External dependencies are only Google Fonts and Plausible analytics**
  (`data-domain="studioanima.io"`). Everything else is inlined, so the page
  renders offline apart from webfonts.
- **The request-access form** currently opens the visitor's mail client with a
  pre-filled message. Setting `var FORM_ENDPOINT` in `index.html` to a form
  endpoint switches it to silent collection; it falls back to the mail client
  automatically if that endpoint ever fails.
- **Earlier design cuts** are archived in a private repository, not here.
