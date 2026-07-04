# NED Propose 2026

Realtime NED (Nearing Expiry Date) approval tool for Nutrifood's Sulawesi distribution team, backed by Supabase.

## Features

- **Propose List** — browse and act on proposed items
- **Recap** — summary view of proposals
- **Admin** — administrative controls
- **Tambah Item** — add new items
- **Rekap Distributor** — distributor-level recap

Realtime sync and user tracking via Supabase (project: `mfulbzkezwfuclisnvym`).

## Project structure

```
public/
  index.html   # the single-page app
netlify.toml   # Netlify build/publish + SPA redirect config
```

## Local development

Just open `public/index.html` in a browser, or serve it:

```
npx serve public
```

## Deployment

Deployed on Netlify at https://ned2026.netlify.app/, publishing the `public/` directory (see `netlify.toml`). Connect this repo to Netlify for continuous deployment on push, or deploy manually with the Netlify CLI:

```
netlify deploy --prod
```
