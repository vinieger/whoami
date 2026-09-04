# whoami

Single-page bio/links site, built with [Hugo](https://gohugo.io) and deployed on GitHub Pages.
Content lives in `content/_index.md`.

## Editing content

Open [`content/_index.md`](content/_index.md) and edit the front matter:

Site-wide name/tagline live in [`hugo.toml`](hugo.toml) under `[params]`.

## Local development

```bash
hugo server
```

Visit http://localhost:1313. Hugo rebuilds and live-reloads on save. (`.claude/launch.json` pins `--baseURL http://localhost:1313/` for local dev, since production `baseURL` in `hugo.toml` includes the `/whoami/` GitHub Pages subpath.)

## Deploying (GitHub Pages)

This repo builds and deploys automatically via [`.github/workflows/hugo.yml`](.github/workflows/hugo.yml) on every push to `main`. 
The workflow installs Hugo, builds with `hugo --gc --minify`, and deploys the `public/` output via `actions/deploy-pages`.
The site is live at `https://vinieger.github.io/whoami/`.
