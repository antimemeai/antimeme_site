# Single-column homepage introduction

The operator wants to try one column with larger introductory text, then
simplify the wording themselves. Stack the two current intro blocks, enlarge
their text from 16px to a responsive 20–24px, and retain the full copy. Keep
the services grid and shared page styles intact. Remove the tablet-only width
constraint that would make the enlarged intro wrap prematurely. Check phone,
tablet, and desktop layout and publish the experiment for the operator to see.

Implemented the single-track intro grid with a 52ch maximum measure, 20px
between its blocks, and inherited responsive type throughout the intro.
The headline, all wording, and the services grid are unchanged. The selectors
are used only on the homepage. Article pages change only their CSS hash.

Verified in Chrome at 320×568, 390×844, 768×1024, and 1440×900: intro blocks
share a left edge and stack without overlap, all intro text computes to 20px
on phone/tablet and 24px on desktop, all six services remain present in their
existing responsive columns, and there is no horizontal overflow. Inspected
phone and desktop screenshots. The current copy makes the desktop page 962px
tall at 1440×900; it scrolls naturally pending the operator's simplification.
git diff --check passes. Stylesheet version 037f83c6cf5f.
