# Restore the saved homepage

The operator requested replacing the temporary multiplayer agents front page
with the real text saved alongside it. Restore `public/index.html` directly
from `archive/specialist-services.html`, including its title, description,
introduction, six services, and contact links. Preserve the saved wording and
use the existing stylesheet and local assets.

The served homepage matches the archived file byte for byte. Both email links
target `hiya@antimeme.ai`; the stylesheet, favicon, and both local fonts return
successfully. Chrome checks at 1024×600, 1440×900, 320×568, and 390×844 confirm
the restored heading, six services, loaded fonts, and no horizontal overflow.
Desktop layouts fit without vertical scrolling; phones scroll naturally.
`git diff --check` passes. Independent source review found no actionable issues.

Tracked as `antimeme-pyt`. Push to `master`, the documented Cloudflare Pages
production branch, to publish the restored homepage through Git integration.
