# Jibril Paddil Portfolio

Static portfolio website for Jibril Paddil's mechatronics engineering projects and certificates.

## Open locally

Open `index.html` in a browser. The page uses the assets in `html5up-forty`.

## Pages and navigation

- `index.html` is the home page and main portfolio. Its links are relative, so they work from the repository's `/Project-Univ/` GitHub Pages path.
- `html5up-forty/landing.html?project=...` renders the existing project galleries and editable case-study details.
- Project entries distinguish personally completed work from team projects and guided training. The RC-car and MeArm entries intentionally show an empty media state until original evidence is supplied.
- `training.html` contains the local training-video and schematic gallery.
- `certificates.html` lists the certificate images already in `html5up-forty/Certificates/`.
- `portfolio.css` holds the shared accessible colours, focus indicators, and responsive styling.

## Adding verified content

- **Resume:** In the small configuration script near the end of `index.html`, set `resumeUrl` to the path of a real resume file. The download button is intentionally not shown while the value is empty.
- **Project details:** In `html5up-forty/landing.html`, add verified text to a project's `caseStudy` object using `problem`, `objectives`, `contribution`, `architecture`, `implementation`, `testing`, `limitations`, or `lessons`. Set `architectureImage` to a diagram filename in `html5up-forty/images/`, and `sourceUrl` to a real HTTPS source-code link only when those materials exist. Do not replace the empty-state `media` array for RC-car or MeArm entries until relevant images, diagrams, or videos are available.
- **Training videos:** Add files to `training-media/videos/`, then set the matching entry's `src` in `training.html`, for example `training-media/videos/plc-ladder-demo.mp4`. MP4 files are covered by the existing Git LFS rule; on GitHub Pages, MP4 paths are resolved through the GitHub LFS media endpoint so the browser receives the video rather than the small LFS pointer. WebM and Ogg files are served from their local paths.
- **Training photos and schematics:** Put photos in `training-media/photos/` and set a photo entry's `src` and descriptive `alt` in `training.html`. Put diagram previews in `training-media/diagrams/`; set a schematic entry's `imageSrc` to its local diagram path. Optionally set `downloadSrc` to its original image or PDF path. Keep the diagram title, type, components, and explanation factual.
- **Certificates:** Edit the `certificates` array in `certificates.html`. Add an `issuer` or `date` only after verifying it from the certificate. Filenames must exactly match files under `html5up-forty/Certificates/`.

Keep media files optimized and avoid committing duplicate copies of existing project videos. Homepage cards use image previews only; project videos remain in the case-study gallery with native controls. MeArm and RC-car media are not present in the current repository, so those case studies display explicit empty states rather than unrelated images.