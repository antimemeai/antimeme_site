# Flowing preamble and horizontal services

The operator requested bringing the homepage's loose clauses together into a
“sort of fever dream preamble” and turning the service cards into larger
horizontal anchors. Combine the existing claims into one flowing paragraph,
keeping the restrained lowercase voice and email invitation. Make each of the
six services a full-width row: small number, large title, supporting sentence.
On phones, put the supporting sentence beneath the title. Preserve all service
wording, writing pages, software page, and masthead/footer. Let the larger rows
scroll naturally rather than compacting them to fit a fixed screen.

Retire the superseded intro block styles and homepage card-height rules.
Keep the shared software cards intact by scoping the new row styles to the
homepage's service-rows class. Check responsive layout, text/link preservation,
keyboard access, and screenshots before publishing.

Combined the prior introduction into one paragraph without adding claims.
It uses responsive 20–28px type; service headings use 30–46px type. Desktop
rows align number, title, and description across the page; at 700px and below,
the description moves beneath the title. Removed obsolete intro/card-fill
selectors. The software page retains its shared two-column card layout.

Chrome at 320×568, 390×844, 768×1024, and 1440×900 verified all six full-width
rows, no overlaps/overflow, minimum 30px titles, responsive description
placement, both email links, the single preamble, and the unchanged software
layout. Keyboard Tab/Enter on the skip link focuses main. Inspected phone and
desktop screenshots. All six service article blocks match HEAD byte-for-byte;
all other published HTML differs only by stylesheet hash 90f2e77e3593.
git diff --check passes.

The Pages Git trigger has repeatedly failed to enqueue recent pushes, so the
existing documented API publishing fallback is now the utility
scripts/deploy-pages. It requires pushed master and committed public changes,
reuses an existing production deployment for that commit or creates one,
then checks production success for the requested SHA. Credentials are read
without shell evaluation or logging. No project settings change. This replaces
repeated inline API commands; the actual publishing run exercises the API.
