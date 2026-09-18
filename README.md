# Club Avolta Field Report

This folder contains the GitHub-ready Progressive Web App (PWA) front end.

## Files

- `index.html` — responsive field-report form
- `favicon.svg` — Club Avolta-inspired app icon
- `manifest.webmanifest` — installable-app metadata
- `sw.js` — offline application-shell cache
- `.nojekyll` — keeps GitHub Pages from modifying the files

## Upload to GitHub

Upload every file in this folder to the root of the same repository. The relative paths must stay unchanged.

## Secure submissions

The form loads promoters from `/api/club-avolta/bootstrap` and sends reports to `/api/club-avolta/submit`. The existing deployed Club Avolta site provides these secure routes and keeps the Supabase secret outside the browser.

GitHub Pages can host the PWA files, but it cannot run the secure API routes by itself. If GitHub Pages is used as the live host, a separate secure backend or reverse proxy must provide both routes; never place a Supabase secret or service-role key in `index.html`.
