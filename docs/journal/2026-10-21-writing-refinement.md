# Essay openings and navigation

The operator requested removing everything in the essay preambles except the
titles, and making the previous/next arrow links stylistically coherent with
the rest of the site. The screenshot also shows the new reading-column and
navigation rules absent while the original site styles are present.

Plan: start each essay body at its first substantive section, retaining its
title and all subsequent content. Apply that boundary in the import utility
so a later import cannot restore the preambles. Replace full neighboring-title
links with small monospace previous/next links that reuse the masthead's link
rules; keep the destination titles in accessible labels. Preserve navigation
at both ends and omit missing neighbors. Version the shared stylesheet URL on
all pages so browsers fetch the new reading and navigation styles. Verify
content boundaries, browser layout and navigation, then publish through Git.

Before changes, the direct check that each essay body begins with a section
heading fails on all four pages: their preambles are still present.

Implemented the preamble boundary in scripts/import-writing and regenerated
all four pages. Verified each begins at its expected opening section and that
the title plus all subsequent text matches the original ODT exactly after
whitespace normalization. Source archives remain intact in ignored context/.
The arrows now share site-nav with the masthead, including its font, size,
hover underline, focus treatment, and padding. Neighbor titles are retained
in aria-label; the visible labels are only previous/next and their arrows.

Live CSS responses include the new reading rules but advertise
Cache-Control: public, max-age=14400, must-revalidate. That supports a stale
browser stylesheet as the explanation for the screenshot's missing reading
layout. Added scripts/version-styles and documented its use after CSS edits.
All seven pages now request /styles.css?v=5025e9621ff2, the CSS content hash.
No serving/deployment build step or dependency was added.

Chrome checks passed on all seven routes at 320x568, 390x844, 768x1024,
1440x900, and 720x450. In addition to bounds and neighbor destinations,
checked that article bodies begin with h2, the arrow links' computed font,
font size, and decoration match the masthead links, and the current versioned
stylesheet is requested. Actual navigation, the illustration, and the keyboard
skip link passed. Inspected desktop Invariants and mobile Intersubjective
screenshots. Browser driver: /tmp/antimeme-writing-refinement-check.mjs.
The existing beads database remains unavailable as recorded in the earlier
journal; do not initialize a replacement for this task.
