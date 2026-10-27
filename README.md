# Dapur500 App

Standalone, Malay-language PWA for the user's ten-book recipe collection. Developed independently of `umarislah86-collab/dapur500`; that repository and its live site are untouched.

## Run

Requires Node.js 22 or newer. No dependencies, API keys or build step.

```sh
npm start
# http://127.0.0.1:4173
npm run check
```

## Features

- 518 recipes, full-text search of available digital ingredients, book and cooked/favourite filters, alphabetical and rating sorting.
- Ten source cookbooks plus personal collections; favourites, ratings, personal notes and ingredient checklists.
- Numeric recipe multipliers; cooking mode with step navigation and optional screen wake lock.
- Weekly meal planning with four meal slots; transfer digital ingredients to shopping list, check off items, share list.
- Manual shopping ingredients for image-only recipes; exact repeated rows are deduplicated without inventing unit conversions.
- Light/dark/system themes, mobile bottom navigation, installable PWA, print, validated JSON backup and restore.
- App shell/data work offline after initial load; opened images are cached. Settings offers optional download of all source pages (approximately 109 MB).

## Data integrity and limits

The original public repository provided the 518-record index, titles, tags and categories. Text was re-extracted from the original PDFs supplied by the user. All source pages are included locally as JPEG reference images. `data-audit.json` records the collection counts.

261 records have digital text extracted from PDFs. 257 are image-only: the previous repository's corrupted OCR is deliberately excluded. Their exact original pages remain readable; automated ingredient lists and automatic serving scaling are unavailable for those image-only records. Add their shopping ingredients manually while viewing the original page.

Digital text extraction is not a manual line-by-line editorial verification. Original page images are the reference for all measurements and instructions. Metadata inherited from the previous index may need correction. No recipes, photographs, nutrition, durations or serving counts are fabricated or imported from external collections. Recipe multipliers change the first numeric quantity in each ingredient; they do not change cooking temperatures or times. Unquantified ingredients remain unchanged.

The app borrows the reference app's warm neutral/orange visual direction and interaction patterns, using newly written code and its own branding. No APK JavaScript, logos, fonts or recipe data are redistributed.

No login, Firebase, backend, paid tier, family cloud sharing, external recipe import, AI analysis or telemetry. Data remains in localStorage on each browser origin. Use backups to move personal data between devices. Browser storage and offline caches can be evicted by the operating system. An offline cache is not a personal-data backup.

## Publish independently

The Pages workflow validates the app and uploads only static app assets. In repository **Settings → Pages**, choose **GitHub Actions** as source. Deployments use relative paths and work under `/dapur500-app/`.

Source PDFs and their content retain their original owners' rights. This project is a personal collection viewer; no additional redistribution licence is granted for book content.
