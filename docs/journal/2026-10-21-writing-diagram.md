# Writing list and evolution diagram

The operator requested removing the horizontal rules between entries on the
writing index, then replacing the evolution diagram with a cleaner pen-and-ink
interpretation suited to the site, preserving its content.

Plan: remove only the index list's border rules. Use the built-in image tool
with the original diagram as the edit target, preserving the labels and flow
relationships on warm paper with dark ink. Inspect text and arrows before
shipping. Store the selected asset in public/writing/ and make the import
utility retain the replacement instead of restoring the original bitmap.
Keep the original image in the unchanged ODT archive. Version CSS, verify
index/illustration layout, and publish through the existing Git workflow.

Generated with the built-in image_gen tool using the original JPG as the edit
target. Exact prompt: docs/evolution-diagram-prompt.txt. Selected output:
public/writing/evolution-diagram-ink.png (1536x1024). The default tool original
remains at ~/.codex/generated_images/01a15e47-5787-7b83-aea6-eea6150ef89a/
exec-d47953bc-a7ef-4062-9717-05b459c90837.png. Inspected all eight boxes, complete
explanatory text, connection labels, and arrow directions against the source.
The redraw retains the cycle and downstream selection/innovation/evolution
flow, with dark ink, fine outlines, and warm paper. Omitted the faint page-number
artifact. Original source bytes remain in the unchanged ODT archive.

Removed the list's per-entry top borders and final bottom border. Updated the
import utility to retain the approved redraw, with a linked figure and a quiet
view-full-size caption. Selecting the image opens the original-resolution PNG
without JavaScript. Removed the unused original bitmap from public/. Versioned
CSS across all seven pages as c6cd130aff6c.

Verification: essay prose matches the preceding revision on all four pages,
excluding the new diagram caption. Chrome checks at 320x568, 390x844, and
1440x900 confirmed four list links with zero entry/list borders, no horizontal
overflow, correct image dimensions and bounds, and actual navigation to the
full-size image. Inspected the index and desktop/mobile illustration screenshots.
Browser driver: /tmp/antimeme-writing-diagram-check.mjs. git diff --check passed.
The pre-existing business note is untouched; the known unavailable beads board
was not reinitialized.
