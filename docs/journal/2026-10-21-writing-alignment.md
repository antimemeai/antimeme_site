# Align writing-list separators

The operator requested one vertical column for the dots between dates and
categories. The existing flex metadata has variable widths and aligns its
right edge, so shorter category labels move the dots.

Use a three-column metadata grid: right-aligned dates, a separator column,
and left-aligned categories. Reserve equal date/category widths on every row,
including the stacked phone layout. Keep this change scoped to the index;
article metadata and all text stay unchanged. Allow the list 60px more width
on desktop so the longest title can retain its single line alongside the
aligned metadata. Verify actual separator positions
and overflow at phone, tablet, and desktop widths, then publish.

Before the change, Chrome at 320px reports separator x positions of 100.61,
107.20, and 113.81px across rows; the common-column assertion fails.

After the change, the same Chrome geometry check passes for all seven rows
at 320×568, 390×844, 768×1024, and 1440×900. Dates precede dots, categories
follow, and there is no horizontal overflow. Inspected phone and desktop
screenshots; the desktop title remains on one line and the index fits 900px.
Article HTML changes only in the shared stylesheet version. git diff --check
passes; stylesheet version is 07ffeff027be.
