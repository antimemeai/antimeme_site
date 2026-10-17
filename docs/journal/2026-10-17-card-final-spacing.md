# Final five-percent card adjustment

Operator requested roughly 5% more service-card height. Bound to two minutes,
a targeted height comparison, and one diff recheck. On roomy homepages,
borrow a little intro-bottom spacing for the grid and increase card-top
padding. No font, copy, navigation, open-source, or compact-breakpoint changes.

The first comparison showed that borrowing intro space alone enlarged the
cards but also increased the last-copy-to-rule gap. Added card-top padding
to keep the additional space inside the cards above the text. The corrected
comparison at 1440×900 passed: grid 311.39→326.70px (+4.9%), row
142.19→149.84px (+5.4%), gap 52.33→50.98px, document height still 900px.
Used /tmp/antimeme-card-check.mjs. The diff recheck and git diff --check
passed; no further assurance layers or unrelated reruns. Existing tracker
blocker unchanged. Operator's local server left running.
