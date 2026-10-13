# Design

Toha supplies the look: Bootstrap, Mulish, the theme's light and dark palettes, the navbar, section blocks, and project cards. This repo does not own that chrome. Dark mode is enabled in `config.yaml` (`features.darkMode.enable: true`).

## Local style

`assets/styles/override.scss` is the only stylesheet here:

- `body` font-weight 600
- headings font-weight 900
- `.home .background` blur of 2.5px

The landing image is `assets/images/home_background.jpg` (`params.background`). The portrait is `assets/images/transparent_picture.png`. Skill logos are the PNGs in `assets/images/`. Mulish files are mounted from `node_modules/@fontsource/mulish`.

## No look drift

Leave the theme chrome, type, colors, and homepage section layout as they are. Copy in `content/` and `data/en/` can change. A visual redesign (palette, type, density, or a different theme) is out of scope unless the task asks.
