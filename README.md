# reyo.dev website

The product website for Reyo by iBoson, served by GitHub Pages from the root of `main`.

This repository holds **built files only**. The source is the Vite/React project in `website/` of the
Code-Quality-Analyzer repository. To change the site, edit it there, then:

```bash
pnpm install --frozen-lockfile
pnpm build
node tests/interactions.mjs
```

and replace everything here except `.nojekyll` and this README with the contents of `website/dist/`.
Every page is pre-rendered (`index.html`, `guide/<topic>/`, `privacy/`, `terms/`, `404.html`) with its own
title, description, canonical URL and structured data, plus `sitemap.xml`. The build targets
`https://iboson-io.github.io/reyo-website/`; when reyo.dev points here, rebuild with `SITE_URL=https://reyo.dev/`.
