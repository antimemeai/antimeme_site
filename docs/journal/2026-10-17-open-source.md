# Top navigation and open source

The operator requested top navigation and a new open-source page. Bounded the
pass to 20 minutes: two-link navigation, a restrained static page, responsive
and keyboard checks, then one source recheck. No new dependencies or build.

Replaced the masthead descriptor with services / open source on both pages.
The wordmark still links home. The active link is underlined and marked with
aria-current. Links remain visible on phones; the masthead can wrap rather
than clip. Homepage content outside the masthead is unchanged.

Added public/open-source/index.html, served at /open-source/, using the same
fonts, grid, spacing, footer, contact link, and skip link. Initial entries:
Blackbird (programmable coding agent, in development), Verbs (constraints for
agent-checkable code, research), and BRepGPU (GPU boundary representation
kernel, in development). Each has a direct source link, not badges or release
claims. No speculative package, docs, Forgejo, or unreleased-project links.

Read local project READMEs/remotes to identify capabilities and maturity.
Anonymous requests to all three GitHub repositories returned 200. GitHub's
repository API reported private=false and MIT for antimemeai/blackbird,
antimemeai/verbs, and antimeme-ai/BRepGPU. Linked those existing public
repositories; this does not adopt a new canonical hosting or licensing policy.
No repository content was published or relicensed by this site change.

README now names both editable pages and the duplicated hand-edited nav.
SITE_DIRECTION records the requested open-source page while preserving the
rejected engagement-section decision and the distinction between verified
public links and a proposed hosting strategy. The untracked business note
remains untouched.

Direct Chrome checks covered both pages at 320×568, 390×844, 600×800,
601×800, 768×1024, 1000×800, 1001×800, 1024×600, 1280×720, 1366×768,
1440×900, 1920×1080, and 720×450. Checked horizontal bounds, wordmark/nav
separation, expected columns, service and metadata geometry, contact/footer
ordering, font loading, mail links, zero animations, and keyboard skip-link
behavior. Both pages fit the roomy tablet/desktop cases without vertical
scrolling. Phones/short windows may scroll. Both nav directions load the
correct route/current-page state; both local routes return 200. Page requests
remain local (source links navigate externally only when followed).
Browser driver: /tmp/antimeme-nav-check.mjs, using native Node WebSocket/CDP.

The single source recheck confirmed one h1/current nav link per page, unique
IDs, no scripts, existing internal targets, exact verified repository links,
and homepage unchanged outside masthead. git diff --check passed. No further
assurance layers. Previously reported missing beads database remains a tracker
blocker; no reinitialization attempted. Leave the operator's local server at
port 8000 running; stop only the headless test browser.
