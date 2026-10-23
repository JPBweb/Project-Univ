# Jibril Paddil Portfolio

Static portfolio website for Jibril Paddil's mechatronics engineering projects and certificates.

## Open locally

Open `index.html` in a browser. The page uses the assets in `html5up-forty`.

## Pages and navigation

- `index.html` is the home page and main portfolio. Its links are relative, so they work from the repository's `/Project-Univ/` GitHub Pages path.
- `html5up-forty/landing.html?project=...` renders the existing project galleries and editable case-study details.
- Project entries distinguish personally completed work from team projects and guided training. The RC-car entry intentionally shows an empty media state until original evidence is supplied.
- `training.html` contains separate PLC experience, electropneumatic schematic, and wiring-media sections.
- `certificates.html` lists the certificate images already in `html5up-forty/Certificates/`.
- `portfolio.css` holds the shared accessible colours, focus indicators, and responsive styling.

## Adding verified content

- **Resume:** In the small configuration script near the end of `index.html`, set `resumeUrl` to the path of a real resume file. The download button is intentionally not shown while the value is empty.
- **Project details:** In `html5up-forty/landing.html`, add verified text to a project's `caseStudy` object using `problem`, `objectives`, `contribution`, `architecture`, `implementation`, `testing`, `limitations`, or `lessons`. Set `architectureImage` to a diagram filename in `html5up-forty/images/`, and `sourceUrl` to a real HTTPS source-code link only when those materials exist. Do not replace the empty-state `media` array for the RC-car entry until relevant images, diagrams, or videos are available.
- **Wiring videos:** The two electropneumatic videos are `training-media/videos/electropneumatic1.mp4` and `training-media/videos/electropneumatic2.mp4`; their paths are set in `training.html`. MP4 files are covered by the existing Git LFS rule; the page uses the GitHub LFS media endpoint with an immutable commit reference so browsers receive the video rather than the small LFS pointer. When publishing new MP4 files, update `githubMediaBase` in `training.html` to a commit that contains those LFS objects. WebM and Ogg are also supported.
- **PLC experience:** Add an entry to the `plcExperiences` array in `training.html`. Include a factual title, summary, equipment, role, skills, and (if available) a video path such as `training-media/videos/plc-ladder-demo.mp4`.
- **Electropneumatic schematics:** The two original diagram previews are `training-media/diagrams/schematicdiagram1.png` and `training-media/diagrams/schematicdiagram2.png`. Their circuit descriptions and paths are set in `training.html`; optionally set `downloadSrc` to an original PDF in the diagrams folder. Previews can be PNG, JPEG, or WebP.
- **Wiring photos:** Three original photos are included in `training-media/photos/` and linked in `training.html`: `wiringportrait1.jpg`, `wiringportrait2.jpg`, and `wiringportait3.jpg`. JPEG and WebP are supported.
- **Certificates:** Edit the `certificates` array in `certificates.html`. Add an `issuer` or `date` only after verifying it from the certificate. Filenames must exactly match files under `html5up-forty/Certificates/`.

Keep media files optimized and avoid committing duplicate copies of existing project videos. Homepage cards use image previews only; project videos remain in the case-study gallery with native controls. RC-car media is not present in the current repository, so its case study displays an explicit empty state rather than unrelated images.