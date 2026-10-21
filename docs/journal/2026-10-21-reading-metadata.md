# Reading-page metadata and The Hacker Perspective

The operator requested showing the categories/dates tastefully on the reading
pages and publishing the full Hacker Perspective text locally. Add a quiet
original-publication link near its top, pointing to the previously supplied
Internet Archive scan of 2600 40:1.

Plan: place one small monospace date/category line under every reading title.
Use the same catalog metadata as the index, preserving the note's circa label.
Add /writing/the-hacker-perspective/ with complete article text from the supplied
archive source, correcting OCR artifacts against the scanned original rather
than rewriting the prose. Preserve paragraph breaks and original emphasis.
Add Originally published in 2600 40:1 — The Hacker Perspective, linked to the
specified scan, near the title. Make the index open the local page and include
it as the first item in chronological previous/next navigation. Keep all-writing
centered. Verify the text, all seven reading headers and neighbors, phone/desktop
layout, and original-publication link before publishing.

The operator subsequently requested date before category on the index and no
circa prefix for the note's index date. Use date/category consistently and
retain the original approximate label on its reading page only.

Implemented a shared metadata renderer for index and reading headers, plus
publication credits. The importer now includes all seven writings in the same
chronological navigation. HTML article bodies remain directly editable; the
importer replaces only their shared header. The Hacker Perspective includes
all 18 body paragraphs plus the original italic author bio. Corrected OCR
artifacts against printed pp. 26–28, including the dropped words in “have the
sense that the magic is lost”; preserved the prose and paragraph boundaries.

Sources retained intact in ignored context/writing-sources/:

- 2600-v40n1-ocr.txt, supplied source:
  https://archive.org/stream/2600-volume-40-issue-1/2600%20Volume%2040%2C%20Issue%201_djvu.txt
- 2600-v40n1.pdf, scanned original:
  https://archive.org/download/2600-volume-40-issue-1/2600%20Volume%2040%2C%20Issue%201.pdf
- Original-publication link on the page:
  https://archive.org/details/2600-volume-40-issue-1/page/n13/mode/2up

PDF pages 14 and 15 are spreads containing printed pp. 26–29. Local pdftotext
and pdftoppm supplied reference text and previews, with no new dependencies.

Validation: direct checks first failed on the old index order, missing local
magazine page, and absent reading metadata. They pass after the change.
Compared all six existing article bodies byte-for-byte to HEAD: unchanged.
A repeated import produces identical HTML. Chrome at 320×568, 390×844, and
1440×900 verified all seven index rows and reading pages, date before category,
no circa prefix on the index note, article metadata beneath titles, the exact
archive URL, 19 magazine paragraphs, centered navigation at both ends, correct
chronological neighbors, and no horizontal overflow. Clicked from index into
the magazine article, next to the note, back through bottom previous, and back
to all writing. Inspected desktop and phone screenshots. The desktop index
still fits its 900px viewport. git diff --check passes. Stylesheet hash updated
to 796058fd4536 on every published page.
