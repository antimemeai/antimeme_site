# Give the six service cards the spare height

The operator found the whitespace below the six service cards, above the
contact rule, unsightly and requested larger cards. Bound this pass to ten
minutes, direct layout checks and one recheck. No copy or page additions.

Added a homepage-only services-fill class. Above 600px the grid grows into
available main height and gives rows equal shares rather than collecting
spare space below the grid. Above 850px height, headings grow from 22px to
26px and body copy from 15px to 17px, with more heading spacing. Compact
viewports retain the existing smaller type. The open-source page has no
services-fill class and is not enlarged.

Chrome geometry checks passed for both pages at the existing 13 viewport
sizes, including desktop fit from 1024×600 through 1920×1080 and the roomy
tablet cases. No horizontal overflow, service text overlap, or navigation
regression observed. Phones and short windows still scroll without clipping.
Used the existing /tmp/antimeme-nav-check.mjs driver.

The single recheck compared the changed CSS against the prior committed CSS
inside Chrome at 1440×900. Service grid height grew from 227.78 to 311.39px,
first row height from 100.39 to 142.19px, and the last-copy-to-rule gap fell
from 110.61 to 52.33px. Document height remained 900px. This directly checks
the requested space redistribution, not merely absence of overflow. Driver:
/tmp/antimeme-card-check.mjs. Inspected the source diff; only the homepage
class and scoped CSS changed. git diff --check passed. No additional review
layers. Previously reported beads database blocker remains unresolved; no
tracker reinitialization. Leave the operator's port-8000 server running.
