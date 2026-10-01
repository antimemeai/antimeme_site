# antimeme.ai

A quiet shingle for independent technical services. Plain HTML and CSS, with
locally served fonts. No JavaScript, dependencies, or build step.

## Preview

Run `./scripts/serve`, then open <http://localhost:8000>. An optional first argument
sets the port: `./scripts/serve 8080`.

## Edit

All copy is in `public/index.html`, including the page title and description.
The contact link uses `hiya@antimeme.ai`. Layout, colors, and type are in
`public/styles.css`; the colors are defined at the top of the stylesheet.

Desktop typography and whitespace adapt to viewport width and height so the page
fits on screen. The phone layout scrolls naturally.

The fonts are Inter Tight and IBM Plex Mono, stored in `public/fonts/` with their
SIL Open Font License texts. Visitors make no requests to Google Fonts.

## Cloudflare Pages

Connect this Git repository to a Pages project. Set:

- Production branch: `master`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: `public`

There is no build: Pages serves `public/` directly. Add `antimeme.ai` under the
project’s **Custom domains** after the initial deployment.

Reference: [Cloudflare’s static HTML guide](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/).
