# Working in portfolio

Personal portfolio site (Hugo + the Toha theme), published with GitHub Pages. This file is how to change the repo.

## Scope

- Change project pages in `content/` and homepage sections in `data/en/`.
- Local layout overrides live in `layouts/`. The theme is the Hugo module `github.com/hugo-toha/toha/v4` at v4.16.0 (`go.mod`). Leave it as a module import.
- Leave the look as it is. See [DESIGN.md](./DESIGN.md).

## Docs

| File | What it is |
| --- | --- |
| [ARCHITECTURE.md](./ARCHITECTURE.md) | Config, content, layouts, static files, workflow |
| [DESIGN.md](./DESIGN.md) | Look intent |
| [../.github/workflows/deploy-site.yml](../.github/workflows/deploy-site.yml) | GitHub Pages build and deploy |

Link those files. Do not paste the section list or the workflow into a new note.

## Commands

Hugo extended **0.167.0** (the version in the workflow). SCSS in the theme and in `assets/styles/override.scss` needs the extended binary. Run `npm ci` first: Toha pipes CSS through PostCSS, and `config.yaml` mounts flag icons, Mulish, and KaTeX fonts from `node_modules`.

Serve locally:

```bash
npm ci
hugo server
```

The site is at http://localhost:1313/portfolio/ because `baseURL` is `https://miquelt9.github.io/portfolio/`. Drafts stay out. `archetypes/default.md` creates pages with `draft: true`; pass `-D` to include them.

Production build, same flags as CI:

```bash
HUGO_ENVIRONMENT=production HUGO_ENV=production hugo \
  --minify \
  --baseURL "https://miquelt9.github.io/portfolio/"
```

Output is `public/` (gitignored, with `resources/` and `node_modules/`). Hugo also rewrites `assets/jsconfig.json` to a machine-local module cache path. Leave that rewrite uncommitted.

## Deploy

`.github/workflows/deploy-site.yml` runs on push to `source`, on pull requests into `source`, and on `workflow_dispatch`.

- Installs Hugo extended 0.167.0 and Node 20, then runs `npm ci`.
- Builds with `hugo --minify` and the Pages base URL from `actions/configure-pages`.
- Uploads `./public` as a Pages artifact.
- Deploys with `actions/deploy-pages` only when the event is not a pull request and the ref is `refs/heads/source`.

The working branch is `source`. Pages itself is set to GitHub Actions in the repo settings.

## Conventions

- English only: `languages.en` in `config.yaml`, copy in `data/en/`, strings in `i18n/en.toml`.
- Homepage sections are YAML in `data/en/sections/`. Author and menus are `data/en/author.yaml` and `data/en/site.yaml`.
- Projects are page bundles under `content/posts/Personal`, `content/posts/College`, and `content/posts/Competitions`. Each bundle is `index.md` plus images or PDFs beside it.
- Project front matter sets `title`, `date`, `description`, `theme: Toha`, a `menu.sidebar` entry (`name`, `identifier`, `parent`, `weight`), `draft`, and `tags`. College pages that use math also set `math: true`.
- `i18n/en.toml` labels the posts section "Projects".
- `{{< line_break >}}` is `layouts/shortcodes/line_break.html`.
- `layouts/_default/_markup/render-link.html` opens `http` links, and links whose destination contains `.pdf`, in a new tab. Goldmark has `unsafe: true`, so project pages can include raw HTML.
