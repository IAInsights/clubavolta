# Club Avolta Report

This folder is the complete GitHub Pages package for the Club Avolta Progressive Web App (PWA).

## Publish on GitHub Pages

1. Upload every file in this folder to the root of the same GitHub repository.
2. In GitHub, open **Settings → Pages**.
3. Select **Deploy from a branch**, choose the branch containing these files, select `/ (root)`, and save.
4. Open the GitHub Pages URL and log in with an authorized Supabase account.

Keep the filenames and folder structure unchanged. The Globe Travel Retail logo, app icon, manifest, and offline service worker are all required.

## Authentication and submissions

- The app uses Supabase email/password authentication.
- There is no public sign-up screen.
- A user may access the report only when the account email matches an active Switzerland promoter in `GI_promoters`.
- Reports are submitted through the protected Supabase Edge Function and saved into the existing `ClubAvolta` table structure.
- The publishable browser key included in `index.html` is intended for client-side use. No service-role key or server secret is included.

## First use

After login, the app asks for the promoter name, activity date, and store. The promoter name comes from the authenticated account. Before submission, the app displays a recap and asks for final confirmation.
