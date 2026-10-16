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
The build uses relative asset paths (`base: './'`), so it works both here under `/codex-website/` and
at a domain root.
