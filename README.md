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

The restrained page is designed to fit on one screen when the viewport has
sufficient room. Spacing responds to viewport height on desktop and tablets.
Phones, small windows, and enlarged text may scroll; content is never clipped
to force a fit. Services use three columns on desktop, two on tablets, and one
on phones; text wraps without forced line breaks.
A keyboard skip link leads directly to the main content.

`archive/` holds previous pages for reference, including the multiplayer-agents
splash. These files are not published.

The fonts are Inter Tight and IBM Plex Mono, stored in `public/fonts/` with their
SIL Open Font License texts. Visitors make no requests to Google Fonts.

## Cloudflare Pages

Open **Workers & Pages → Create application → Pages → Import an existing Git
repository** in the Cloudflare dashboard. Connect GitHub and select
[`antimemeai/antimeme_site`](https://github.com/antimemeai/antimeme_site).
Use these settings:

- Production branch: `master`
- Framework preset: `None`
- Build command: `exit 0`
- Build output directory: `public`
- Root directory: leave blank (repository root)
- Environment variables: none

Select **Save and Deploy**. There is no build: Pages serves `public/` directly.
Subsequent pushes to `master` deploy automatically. Only `public/` is published;
repository documentation and issue-tracker files stay outside the site.

Open the resulting `*.pages.dev` URL and verify the page, fonts, and both email
links. Then open the project's **Custom domains → Set up a domain** and enter
`antimeme.ai`. The apex domain must be a zone in the same Cloudflare account, with
its nameservers pointing to Cloudflare; follow the dashboard's DNS setup.

References: [Static HTML](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/),
[Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/),
[Custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/).
