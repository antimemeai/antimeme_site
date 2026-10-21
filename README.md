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
in sync across all published pages. Set `aria-current="page"` on the current page's
link, or `aria-current="location"` on Writing while reading an essay.
The contact link uses `hiya@antimeme.ai`. Layout, colors, and type are in
`public/styles.css`; the colors are defined at the top of the stylesheet.
After changing CSS, run `python3 scripts/version-styles` before publishing.
It updates the stylesheet URL on every page using a hash of the CSS, so a
cached stylesheet cannot hide a new layout. This is an explicit edit command,
not a build step.

The homepage uses one flowing preamble followed by six full-width service
rows with large titles. Descriptions sit alongside titles on desktop/tablet
and beneath them on phones. The page scrolls naturally to give those rows
room. The four-entry open-source page retains two columns above phone widths
and one on phones; it fits one screen where the viewport has sufficient room.
Text wraps without forced line breaks or clipping.
A keyboard skip link leads directly to the main content.

## Writing

`public/writing/index.html` is a simple title list. Each essay lives in its own
directory beneath `public/writing/`, with readable prose and previous/next
links at both ends. Local writings follow the author's supplied dates:
The Hacker Perspective, Often Misunderstood: IC → M Transitions,
The Strange Wilderness, Intuition, Intersubjective,
Cell/Atom Bomb, Invariants, then JSMNTL: Solo Bot Coding.
The first writing has no previous link; the last
has no next link. Articles scroll
naturally. Their masthead and footer match the rest of the site.
Each essay starts at its first substantive section beneath the title; the
old summaries, disclaimers, welcomes, and released-essay lists are omitted.
The previous/next links share the main navigation's small monospace type and
hover underline. Destination titles remain in their accessible labels.
Both navigation rows put all writing in the center between previous and next,
even when a neighboring link is absent. These rows have no horizontal rules.
The four recovered essays use exact dates supplied by the author, stored in
`ESSAY_DATES`. The Hacker Perspective is a local reading page with its full
text and original author bio, transcribed from the supplied archive text and
checked against the scan of 2600, Vol. 40, No. 1 (Spring 2023), pp. 26–28.
`PUBLICATION_CREDITS` in the import utility holds its original-publication
link and index credit. JSMNTL uses the explicit June 28, 2026 date from its
source document. Each row shows its date followed by a category (magazine
essay, essay, or note). Metadata sits beside titles on desktop and above them
on phones. Reading pages repeat the date and category beneath their titles;
the magazine essay also links its original publication there.
All published footers name Antimeme AI LLC.

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
portrait editorial redraw, served locally as
`public/writing/evolution-diagram-editorial.png`.
Selecting it opens the full-resolution image. Imports retain this replacement;
the original bitmap remains in the unchanged ODT source archive.

JSMNTL was recovered from `~/Documents/JSMNTL_Solo_Bot_Coding.pages` and
exported with Apple Pages to DOCX and plain text in ignored
`context/writing-sources/`. Its published HTML is directly editable, and the
operator-requested final-sentence omission is already applied. `HTML_ESSAYS`
in the import utility holds its title/date metadata; reimports retain the
existing article markup while refreshing the index and navigation.

The Strange Wilderness was transcribed from the author-supplied screenshot,
archived intact at `context/writing-sources/the-strange-wilderness-source.png`.
Its circa May 12, 2024 date is visibly approximate on the reading page; the
index displays May 12, 2024 without the circa prefix at the author's request.
It is also registered in
`HTML_ESSAYS`, with category note. The import utility pairs each article with
its metadata before sorting by date, keeping both neighbor rows chronological.
On reimport, shared reading headers refresh from the catalog while directly
edited HTML article bodies remain intact.

Often Misunderstood: IC → M Transitions was recovered from
`~/Desktop/oft_misunderstood_ic_m_transitions.odt`, archived intact in ignored
`context/writing-sources/`, and converted to directly editable HTML. Its essay
category and February 4, 2024 date (supplied by the author) live in `HTML_ESSAYS`.
The original introduction, section headings, three lists, and two prose
callouts are retained. The title uses a typographic arrow in place of `->`.

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

If a push does not enqueue a deployment, run `python3 scripts/deploy-pages`.
It deploys the already-pushed master commit through the existing antimeme-site
project and waits for production success. It uses `CLOUDFLARE_API_TOKEN` and
`CLOUDFLARE_ACCOUNT_ID`, or the existing workspace `.env` keys `cf_api_key` and
`cf_account_id`, without printing them. It does not change project settings.

Open the resulting `*.pages.dev` URL and verify the page, fonts, and both email
links. Then open the project's **Custom domains → Set up a domain** and enter
`antimeme.ai`. The apex domain must be a zone in the same Cloudflare account, with
its nameservers pointing to Cloudflare; follow the dashboard's DNS setup.

References: [Static HTML](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/),
[Git integration](https://developers.cloudflare.com/pages/get-started/git-integration/),
[Custom domains](https://developers.cloudflare.com/pages/configuration/custom-domains/).
