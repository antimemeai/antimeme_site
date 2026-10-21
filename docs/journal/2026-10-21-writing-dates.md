# Entity copyright and writing dates

The operator requested Antimeme AI LLC as the footer copyright holder, dates
on the writing list, approximate 2023/2024 dates for the four recovered essays
in their existing order, and a fifth item: The Hacker Perspective in 2600,
volume 40, number 1. They supplied OCR text and the exact archive-scan link.
A second new piece is forthcoming; no second title/source has been provided.

Plan: update all published footers and the import source footer. Add quiet
monospace dates to the list; preserve the relative order Intuition, Cell/Atom
Bomb, Intersubjective, Invariants. List the Spring 2023 magazine publication
before that approximate 2023/2024 group and link directly to the specified
scan, with publication metadata. Retain the four local essays' reading sequence.
Keep index metadata in the import utility so reimport cannot drop the entry
or dates. Check phone/desktop list and footer layout, source links, and article
content, version CSS, and publish through the existing Git workflow.

Retrieved original OCR and archive metadata into ignored context/writing-sources/
from the user's Internet Archive identifier. The metadata dates the issue to
2023 and repeated printed footers in the OCR identify Spring 2023. The text
includes the user's Hacker Perspective column beginning after printed page 25.
The publisher's issue listing independently identifies the same seasonal issue
and includes HACKER PERSPECTIVE in its contents:
https://store.2600.com/products/new-issue-pdf-spring-2023
User-specified destination:
https://archive.org/details/2600-volume-40-issue-1/page/n13/mode/2up
The approximate range comes from the operator, not the ODT export timestamps.

Implemented ©2026 Antimeme AI LLC in every published footer. Added a Spring
2023 time label and publication credit to the direct archive entry, and the
operator-supplied approximate 2023/2024 labels to each local essay. The four
local entries retain their relative order; the external publication precedes
them. Dates use the existing monospace face, at right on desktop and above
titles on phones. Footer groups may wrap on narrow screens. CSS version:
cae8467ad33f. No essay prose or figures changed.

Verified the exact archive scan URL returns HTTP 200. Direct source checks
confirmed all seven copyright footers and byte-for-byte unchanged article
markup in all four local essays. Chrome checks at 320x568, 390x844, and
1440x900 covered all seven routes: no horizontal overflow, footer bounds,
five titles/date labels in the specified relative order, exact archive target,
publication credit, desktop/mobile date placement, and a working dated local
link. The index fits the 1440x900 viewport. Inspected phone/desktop screenshots.
Driver: /tmp/antimeme-writing-dates-check.mjs. git diff --check passed.
Known unavailable beads board not reinitialized; business note untouched.
