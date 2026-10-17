# SALib and crate links

Operator requested Verbs' crates.io link and a SALib entry with repository and
crate links. Bound to ten minutes, direct metadata/link/layout checks, and one
source recheck. Added the standard crates.io/crates/verbs and crates/salib
links and github.com/antimemeai/salib. SALib description: global sensitivity
analysis in rust. Label: published (not a stability/API guarantee).

crates.io API confirmed Verbs 0.1.0 and SALib 0.3.0, their descriptions, and
repository URLs. GitHub API confirmed SALib public with Apache-2.0 license;
its repository page returned 200. Direct crates storefront GET probes returned
404; a version-specific HEAD and a well-known crate control HEAD returned
403. These storefront pages were not verified loading successfully. Retained
standard crate URLs based on successful registry metadata, not fabricated
replacement URLs. Do not describe the storefront probes as passing.

Switched only the open-source grid to two columns above phone widths so four
entries form two balanced rows; phones remain one column. Updated metadata,
README, and site direction. Homepage and its final spacing remain untouched.

Chrome checks of the changed open-source page passed at the existing thirteen
viewport sizes, covering phones, breakpoint edges, roomy tablets, desktop
1024×600 through 1920×1080, and short 720×450. Verified four cards, expected
columns, link/metadata geometry, no horizontal overflow, loaded fonts, mail
link, skip-link keyboard behavior, and active nav. Roomy tablet/desktop cases
still fit one screen. Driver: /tmp/antimeme-salib-check.mjs.

The one source recheck confirmed exact new URLs once each, four entries,
unique IDs, correct SALib description, homepage byte-identical, and CSS change
limited to the software-list rule. git diff --check passed. No additional
assurance layers. Existing beads database blocker unchanged. Leave the local
port-8000 server running; stop only the temporary headless browser.
