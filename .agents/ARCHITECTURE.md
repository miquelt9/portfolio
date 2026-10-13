# Architecture

Static Hugo site. [Toha](https://github.com/hugo-toha/toha) v4.16.0 is a Hugo module. GitHub Pages serves the `public/` build. There is no app server.

## Config

`config.yaml` is the site config.

- `baseURL` is `https://miquelt9.github.io/portfolio/`. `title` is "Miquel's Portfolio". `locale` is `en-us`. The only language is `en`.
- `module.imports` is `github.com/hugo-toha/toha/v4`. `go.mod` requires v4.16.0. The module path in `go.mod` is still `github.com/BernatBC/BernatBC.github.io`.
- Mounts publish `static/`, `node_modules/flag-icons/flags`, `@fontsource/mulish` files, and KaTeX fonts.
- Goldmark allows raw HTML. Home outputs are HTML, RSS, and JSON. The JSON output is the client-side search index.
- Features on: dark mode, portfolio, table of contents, tags, flags, KaTeX, highlight.js, Plyr. Blog, notes, comments, analytics, and the support block are off. Flowchart (Mermaid) is configured and disabled (`features.flowchart.enable: false`).
- The navbar shows up to 10 section titles. The footer template name is `footer.html` (the theme partial; this repo does not override it). Footer navigation and contact are on. Newsletter and disclaimer are off.

## Content

`content/posts/` is the project tree.

| Path | Role |
| --- | --- |
| `content/posts/_index.md` | Section title "Projects" |
| `content/posts/Personal/_index.md` | Sidebar group, weight 300 |
| `content/posts/College/_index.md` | Sidebar group, weight 300 |
| `content/posts/Competitions/_index.md` | Sidebar group, weight 300 |

Each project is a directory with `index.md` and its media. Published URLs sit under `/portfolio/posts/` (for example `/portfolio/posts/personal/bingo-musical/`).

## Data

Homepage sections, in display order. A section renders `sections/<id>.html` from the theme unless `section.template` is set. `layouts/index.html` in the theme always renders the home partial first.

| File | Section | id | Weight | Template |
| --- | --- | --- | --- | --- |
| `data/en/sections/about.yaml` | About | `about` | 1 | `sections/about.html` |
| `data/en/sections/skills.yaml` | Skills | `skills` | 2 | `sections/skills.html` |
| `data/en/sections/experiences.yaml` | Experience | `experiences` | 3 | `sections/experiences.html` |
| `data/en/sections/education.yaml` | Education | `education` | 5 | `sections/education.html` |
| `data/en/sections/recent-posts.yaml` | Projects | `recent-posts` | 7 | `sections/recent-posts.html` (local override) |

`recent-posts` shows 6 posts and a "show more" button. `data/en/author.yaml` is the name, greeting, summary lines, portrait, and contact links. `data/en/site.yaml` is the copyright, meta description, and custom menus: Projects → `/portfolio/posts/`, Contact → `#footer`.

## Layouts

This repo overrides four theme files:

| File | Role |
| --- | --- |
| `layouts/partials/sections/home.html` | Landing hero. Greeting and summary come from author data. Background is `params.background` (`images/home_background.jpg`), resized to several widths. |
| `layouts/partials/sections/recent-posts.html` | Project cards. "Show more" links to `/portfolio/posts/`. |
| `layouts/_default/_markup/render-link.html` | Remote and PDF links open in a new tab. |
| `layouts/shortcodes/line_break.html` | `{{< line_break >}}` renders a `<br>`. |

## Assets, static, and npm

`assets/images/` holds the portrait (`transparent_picture.png`), `home_background.jpg`, `background.jpg`, and skill logos. `assets/styles/override.scss` is the only local stylesheet.

`static/webgl/spaceshooter/` is a Unity WebGL build. Hugo copies `static/` through unchanged, so it is served at `/portfolio/webgl/spaceshooter/`. The HackUPC 2021 page embeds `https://miquelt9.github.io/SpaceShooter/`, a separate site.

`i18n/en.toml` sets the posts label to "Projects". `archetypes/default.md` is the new-page skeleton (`draft: true`).

`package.json` is the Toha npm set (Bootstrap, PostCSS, Mulish, Font Awesome, KaTeX, and the rest) with a `packages/hugoautogen` workspace. CI installs it with `npm ci`.

## Workflows

`.github/workflows/deploy-site.yml` builds on every pull request into `source` and deploys on a push to `source`. Details: [AGENTS.md](./AGENTS.md).

`.github/dependabot.yml` is present. Its `package-ecosystem` is empty, so Dependabot does not update packages.
