# Often Misunderstood: IC → M Transitions

Found the requested essay at
~/Desktop/oft_misunderstood_ic_m_transitions.odt. The author supplied February
4, 2024 as its writing date; document creation/export dates do not override it.

Plan: retain an intact source copy in ignored context/writing-sources/, convert
the text, heading hierarchy, three bullet lists, and callouts into the existing
reading template, and register it as an HTML essay. Use a typographic arrow in
the title. Preserve the source prose. Insert chronologically after The Hacker
Perspective and before The Strange Wilderness, refreshing both navigation rows
and retaining the aligned date/category columns. Check text against the ODT,
neighbor links, list alignment, and phone/desktop reading layout, then publish.

Added /writing/often-misunderstood-ic-m-transitions/ as an essay dated February
4, 2024. Archived ODT matches the Desktop file byte-for-byte. A one-time
transcriber in ignored context/import-ic-m.py reuses the existing ODT block
renderer without the four earlier essays' publication-preamble trimming.
The new page preserves the complete introduction and all prose, headings,
three bullet lists (5/4/2 items), and two callouts. No new dependencies.

Widened the date track from 13ch to 16ch for February 4, 2024 and the desktop
list from 940px to 960px so the long Intersubjective title retains its line.
The separator dots still align at all tested widths. CSS version e86961555412.

Validation: normalized published body matches every ODT body paragraph/heading,
including list items. All seven previously published article bodies remain
byte-for-byte unchanged. Reimport produces identical HTML. Chrome checks at
320×568, 390×844, 768×1024, and 1440×900 pass for eight chronological entries,
the exact new date/category, aligned dots, both sets of neighbors on every
article, centered all-writing links, the new page's list/callout counts, and
no horizontal overflow. Actual index/new-page/previous/next navigation clicks
pass. Inspected phone and desktop screenshots. git diff --check passes.
Existing untracked docs/NOTE_FROM_BUSINESS.md is untouched; the known
unavailable beads board is not replaced.

Publishing: push of 2490b19 succeeded, but Cloudflare had no deployment for
that commit even after waiting; the live site still served 7537a0c. Queried
the existing antimeme-site Pages project using the workspace's existing
Cloudflare credentials (never printed). Production auto-deploy is enabled,
with master selected and all paths included. No settings were changed.
Triggered that same committed master through the documented multipart
POST /accounts/{account_id}/pages/projects/antimeme-site/deployments API:
https://developers.cloudflare.com/api/resources/pages/subresources/projects/subresources/deployments/methods/create/
Deployment b035d557-1544-423b-910e-4c2589eeccd3 completed successfully for the
exact 2490b19 commit. Live HTML now matches the published index, complete new
essay, and both changed neighbor pages (ignoring Cloudflare's injected beacon).
