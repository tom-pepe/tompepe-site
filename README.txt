Tom Pepe — personal brand site
Deployment package · July 20, 2026 (v72)

IMPORTANT: open index.html from INSIDE this unzipped folder.

NEW IN v72: Framework rail's active-tab icon color now uses real
dedicated brass icon assets instead of a CSS filter trick. Tom's Gemini-
generated "-active" icons had stray sparkle-mark artifacts he wanted
removed. Root cause of a rougher-than-expected cleanup: the source
files are RGBA with genuine transparency, and treating them as flat RGB
first exposed meaningless garbage color data stored under the
transparent pixels — full pipeline redone using the real alpha channel,
with connected-component analysis isolating each tool's true silhouette
from small disconnected sparkle marks. Output icons are solid brass on
a transparent background, verified via simulated composite against the
actual viridian-surface tab color they sit on. Two of five icons matched
their base counterparts' aspect ratio exactly (0.00 and 0.01 difference),
confirming the pipeline introduces no distortion; the other three show
expected pose differences from being freshly regenerated art, not
processing errors.

Base icon + active icon both load per tab; CSS opacity-crossfades
between them on the same zero-JS radio-driven mechanism used everywhere
else on the site. Verified via real computed opacity values (1 on the
active tab, 0 on all others) before shipping, not just visual read.

Prior: thesis shortened + framework rail interaction + About timeline
updates, merged from a ChatGPT-assisted session (v71).

Contents
--------
index.html                                  the site
og-image.jpg                                social share preview image
LICENSE                                     all-rights-reserved notice
favicon.ico                                 tab mark (hawk-eye seal)
portrait-tom-pepe-2026-d.webp               hero portrait, About section
hawk-eye-seal.webp                          closing seal above the footer (animated once)
texture-viridian-weave-v3.webp              thesis panel background texture
plate-key.webp                              Case 01 — Digital Broker Experience
plate-trellis.webp                          Case 02 — Partner Ecosystem Platform
plate-prism.webp                            Case 03 — Brand Repositioning
plate-loom.webp                             Case 04 — Marketing Infrastructure & Automation
plate-meridians.webp                        Case 05 — Global Web Consolidation
plate-kaleidoscope.webp                     Case 06 — Culture & Inclusion Programs
hand-plate-1-mist.webp                      hero print sequence — plate 1
hand-plate-2-accents.webp                   hero print sequence — plate 2
hand-plate-3-key-v3.webp                    hero print sequence — plate 3
hand-plate-4-ink-v2.webp                    hero print sequence — plate 4 (umber ink)
icon-01-see.webp … icon-05-measure.webp     framework rail icons (base state)
icon-01-see-active.webp … -05-measure-active.webp  framework rail icons (active/brass state)

AFTER DEPLOYING: test the social preview at
https://www.linkedin.com/post-inspector/ and https://cards-dev.twitter.com/validator

Hosting
-------
Upload the folder to any static host (GitHub Pages, Netlify, Cloudflare Pages,
S3). One HTML file plus assets in the same directory — no build step.
