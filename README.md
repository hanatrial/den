# NED Propose 2026

Realtime NED (Nearing Expiry Date) approval tool for Nutrifood's Sulawesi distribution team, backed by Firebase Firestore (project: `densul-5b630`).

## Features

- **Propose List** — browse and act on proposed items
- **Recap** — summary view of proposals
- **Admin** — administrative controls
- **Tambah Item** — add new items
- **Rekap Distributor** — distributor-level recap

Realtime sync and user tracking via Firestore (collection: `ned_approvals`).

## Project structure

```
public/
  index.html        # the single-page app
firestore.rules      # Firestore security rules (deploy with `firebase deploy --only firestore:rules`)
.github/workflows/pages.yml  # GitHub Pages deploy on push to main
netlify.toml          # Netlify build/publish + SPA redirect config (alternate host, unused by default)
```

## Local development

Just open `public/index.html` in a browser, or serve it:

```
npx serve public
```

## Deployment

Hosted on **GitHub Pages**, publishing the `public/` directory via `.github/workflows/pages.yml` on every push to `main`. Enable it once in the repo: Settings → Pages → Source → "GitHub Actions".

The data backend is Firestore in the `densul-5b630` Firebase project — that's deployed separately via `firebase deploy --only firestore:rules` and is unaffected by where the static site is hosted.
