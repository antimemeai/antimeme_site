# Center the writing-index link

The operator requested moving all writing between previous and next, centered
whether either neighboring link exists, and removing at least the top rule.
Plan: use three explicit grid columns in both essay navigation rows, with
previous left, all writing centered, and next right. Omit missing neighbors
without shifting the center. Remove both navigation rules and the standalone
index link. Keep the same typography, hover/focus behavior, and destinations.
Update the import utility and stylesheet version, check endpoint/phone/desktop
geometry and navigation, then publish through the existing Git workflow.

Implemented explicit previous/index/next grid placement with equal outer
columns, so missing neighbors leave the index at the geometric center.
Removed both rules and the standalone back link. Regenerated the four essay
pages and versioned CSS across all seven pages as a2c150f4116d. No article
text or image changes.

Chrome verification covered all four essays at 320x568, 390x844, and 1440x900.
Both navigation rows have zero top/bottom borders; all-writing center differs
from the row center by less than half a pixel. Links share one row without
overlap or horizontal overflow, and first/last neighbor omissions are correct.
Clicked the bottom index link and confirmed /writing/. Inspected phone and
desktop screenshots. Driver: /tmp/antimeme-centered-nav-check.mjs.
git diff --check passed. Existing business note untouched; known unavailable
beads board not reinitialized.
