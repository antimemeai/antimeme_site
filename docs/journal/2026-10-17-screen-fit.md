# Restore the one-screen intent

The operator corrected the previous layout pass: scrolling is not wanted on
screens with sufficient form factor. The site is intentionally restrained.
Removing the height-responsive layout was a mistaken interpretation, not an
approved shift toward a scrolling site. This entry supersedes the previous
entry's natural-scrolling direction.

Bound this correction to 15 minutes, direct browser fit/geometry checks and
one source recheck. Restored the prior viewport-height-responsive spacing,
service type sizing, and flex main/contact arrangement. Applied those rules
above 600px so the new two-column tablet layout also benefits. Kept the
phone layout, wrapping text, keyboard skip link, and archived splash. No
HTML or copy changed. Updated README to state the one-screen intent while
allowing small windows and enlarged text to scroll rather than clip.

Chrome checks explicitly asserted document height no larger than viewport
height at 768×1024, 1000×800, 1024×600, 1280×720, 1366×768, 1440×900,
and 1920×1080. All passed. Also checked 320×568, 390×844, 601×800, and
720×450: these insufficient viewports scroll, with no horizontal overflow
or text overlap. The 720×450 viewport covers the effective CSS space of a
1440×900 window at 200% zoom, not a browser-zoom command. All eleven checks
confirmed service columns, heading/copy geometry, footer/contact ordering,
local fonts, mail links, zero animations, and keyboard skip-link operation.
Temporary direct browser driver: /tmp/antimeme-fit-check.mjs.

The source recheck confirmed HTML unchanged, a growing min-height page,
and no overflow clipping or maximum-height declarations. Its initial regex
incorrectly counted max-height media conditions as clipping declarations;
corrected that predicate to inspect declaration lines. No CSS defect was
found. git diff --check passed. No additional review layers performed.

The previously reported missing beads database remains unresolved; did not
reinitialize it or retry unrelated tracker setup. Business note untouched.
