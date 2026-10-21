# antimeme.ai

A quiet shingle for independent technical services. Plain HTML and CSS, with
locally served fonts. No JavaScript, dependencies, or build step.

## Preview

Run `./scripts/serve`, then open <http://localhost:8000>. An optional first argument
sets the port: `./scripts/serve 8080`.

## Edit

Read [site direction](docs/SITE_DIRECTION.md) before changing copy or structure:
concrete glimpses, not a catalog; no engagement explanation or funnel.

Services copy is in `public/index.html`; open-source copy is in
`public/open-source/index.html`. Each page has its own title and description.
The shared top navigation links `/`, `/open-source/`, and `/writing/`; keep it
in sync across all seven pages. Set `aria-current="page"` on the current page's
link, or `aria-current="location"` on Writing while reading an essay.
The contact link uses `hiya@antimeme.ai`. Layout, colors, and type are in
`public/styles.css`; the colors are defined at the top of the stylesheet.
After changing CSS, run `python3 scripts/version-styles` before publishing.
It updates the stylesheet URL on every page using a hash of the CSS, so a
cached stylesheet cannot hide a new layout. This is an explicit edit command,
not a build step.

The restrained page is designed to fit on one screen when the viewport has
sufficient room. Spacing responds to viewport height on desktop and tablets.
Phones, small windows, and enlarged text may scroll; content is never clipped
to force a fit. Services use three columns on desktop, two on tablets, and one
on phones; text wraps without forced line breaks. The four-entry open-source
page uses two columns above phone widths and one on phones.
A keyboard skip link leads directly to the main content.

## Writing

`public/writing/index.html` is a simple title list. Each essay lives in its own
directory beneath `public/writing/`, with readable prose and previous/next
links at both ends. The sequence is Intuition, Cell to Atom Bomb,
Intersubjective, Invariants, following the series introductions. The first
essay has no previous link; the last has no next link. Articles scroll
naturally. Their masthead and footer match the rest of the site.
Each essay starts at its first substantive section beneath the title; the
old summaries, disclaimers, welcomes, and released-essay lists are omitted.
The previous/next links share the main navigation's small monospace type and
hover underline. Destination titles remain in their accessible labels.

Edit these HTML files directly. When adding an essay, update the title list
and the neighboring essays' navigation at both ends. Keep shared navigation
consistent on any new page. Cross-links among the four imported essays stay
local; other references retain their original destinations.

The initial ODT documents were recovered from `~/Downloads/*_meta.odt` and
copied intact to ignored `context/writing-sources/`. To intentionally replace
all four published essays and regenerate the list from those sources, run
`python3 scripts/import-writing context/writing-sources`. This import utility
uses Python's standard library and is not part of serving or deployment.
Reimporting overwrites subsequent HTML edits. The evolution diagram is a
pen-and-ink redraw, served locally as `public/writing/evolution-diagram-ink.png`.
Selecting it opens the full-resolution image. Imports retain this replacement;
the original bitmap remains in the unchanged ODT source archive.

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
