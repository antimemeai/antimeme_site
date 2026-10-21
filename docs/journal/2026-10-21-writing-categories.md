# Writing categories, exact dates, and The Strange Wilderness

The operator supplied The Strange Wilderness as an image and requested a local
note dated circa May 12, 2024. They requested row categories: magazine essay for
The Hacker Perspective; essay for the existing five local articles; note for
the new piece. They also replaced approximate dates with author-supplied dates:
Intuition May 28, 2024; Intersubjective June 2, 2024; Cell/Atom Bomb June 21,
2024; Invariants July 3, 2024. JSMNTL stays June 28, 2026.

Plan: transcribe the screenshot faithfully, including its five bullets and
emphasis, into a local reading page. Archive the image intact in ignored
context/writing-sources/the-strange-wilderness-source.png. Store dates and
categories in the import utility and sort local writings by the supplied dates,
keeping the circa qualifier visible. This places the note first and moves
Intersubjective before Cell/Atom Bomb. Refresh both sets of neighbor links.
Add quiet category/date metadata to each index row, retaining the magazine's
publication credit and exact scan destination. Check seven list entries,
chronology, six local reading routes, responsive metadata, and content before
publishing. These dates come from the author, superseding file/export guesses.

Added /writing/the-strange-wilderness/ with the source title, two paragraphs,
five bullets, italic Pax Americana/shatter, and bold italic at least. Manually
compared the transcription against the supplied image; omitted only editing
cursors/spelling underlines. Existing five article bodies are unchanged, and
the JSMNTL closing-sentence omission remains intact.

Catalog rows now pair category/date metadata. The external entry is magazine
essay; the note is note; the other five are essay. Exact author dates are in
ESSAY_DATES, and the note's visible label is c. May 12, 2024. Local entries and
article markup are paired before chronological sorting; navigation now runs
note -> Intuition -> Intersubjective -> Cell/Atom Bomb -> Invariants -> JSMNTL.
Updated accessible navigation labels to say writing. Tightened row padding
slightly so the seven-entry list still fits a roomy desktop. CSS hash:
6e90dfec6422. No dependencies or serving/build steps added.

Chrome checks passed at 320x568, 390x844, 1440x900 for all seven row categories,
ISO dates and circa label, exact local order, responsive metadata placement,
no overflow, all six local routes and both navigation rows' neighbors/centers,
five note bullets, and the entity footer. The index fits 1440x900. Actual
index-to-note, note-to-Intuition, Intuition-to-Intersubjective, and bottom-next
to Cell/Atom Bomb clicks passed. Inspected desktop/mobile index and note
screenshots. Driver: /tmp/antimeme-categories-check.mjs. git diff --check passed.
Known unavailable beads board was not reinitialized; business note untouched.
