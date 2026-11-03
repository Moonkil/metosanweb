# METOSAN Website

Static multi-language landing site for METOSAN, a metronome for macOS.

## Editing images in VS Code

Images are separated into editable assets:

- `assets/images/app-icon.webp` — navigation icon and favicon
- `assets/images/metosan-hero.webp` — main MacBook and METOSAN waving illustration
- `assets/images/feature-preview.webp` — app feature screenshot

To change an image, replace the relevant WebP file while keeping the **same filename**. Or change the image URL in `index.html` to use your own PNG/WebP image. Preview the site locally, commit, and push to the `main` branch. Connected Cloudflare deployment should update automatically.

The language selector, page layout and styling remain in `index.html`.

## Pages
- `/` — main landing page, Korean/English/Japanese/Simplified Chinese
- `/support/` — contact support: **contact@danbee.ai**
- `/privacy/` — temporary privacy page; replace with finalized policy before App Store review

## Deployment
Deploy as a static site. There is no build step. Use project root `.` if the hosting provider requests an output directory.

Mac App Store download link should be updated after the app listing is live.

© 2026 danbee Inc.
