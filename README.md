# METOSAN Website

Static multi-language landing site for METOSAN, a character metronome for iPhone, iPad and Mac.

## Images

- `assets/screenshots/` — original App Store screenshots (large PNGs, source only)
- `assets/images/screens/` — web-optimized JPEGs used by the site, per language (`ko`, `en`, `ja`, `zh`):
  - `iphone-{lang}-01-main … 05-store.jpg` (640px wide, from `iPhone-6.3`)
  - `ipad-{lang}-01-main.jpg` (900px wide, from `iPad-13`)
  - `mac-{lang}-01-main.jpg`, `mac-{lang}-02-shortcuts.jpg` (cropped from `Mac-2880x1800`)

- `assets/images/motion/` — character motion frames (language-independent):
  - `clap-apart.jpg` + `beat-1…4.jpg` — overlays on `iphone-{lang}-02-playing.jpg` that replay the playing screen at 120 BPM (captured from the iOS simulator via a temporary UI test in the app repo)
  - `{clap,metronome,woodblock,hihat}-{1,2}.webp` — the app's own character art frames for the "Motions" section
  - `icon-*.png` — sound icons cropped from the app screen

The page swaps screenshots by language through the `data-shot` attribute (`{l}` is replaced with the language code). To refresh a screenshot, regenerate the JPEG with the same filename, e.g.:

```sh
sips -s format jpeg -s formatOptions 80 --resampleWidth 640 assets/screenshots/iPhone-6.3/ko-01-main.png --out assets/images/screens/iphone-ko-01-main.jpg
```

## Pages
- `/` — main landing page, Korean/English/Japanese/Simplified Chinese
- `/support/` — contact support: **contact@danbee.ai**
- `/privacy/` — temporary privacy page; replace with finalized policy before App Store review

## Deployment
Deploy as a static site. There is no build step. Use project root `.` if the hosting provider requests an output directory.

The iPhone and iPad versions are available on the [App Store](https://apps.apple.com/kr/app/metosan-메토상/id6830031648). Both App Store badges in `index.html` link to this listing, and release copy is localized in all four languages. Mac App Store badges remain disabled ("출시 준비 중") until the Mac listing is live.

© 2026 danbee Inc.
