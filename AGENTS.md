# AGENTS.md

## Overview
Static HTML coursework site ("高级网页设计" class project). Pure HTML/CSS — no build step, no package manager, no framework, no tests, no CI.

## Viewing
Open `index.html` directly in a browser, or serve the root with any static server (e.g. `python -m http.server`).

## Structure
- `index.html` — main landing page
- `1.html` … `11-4.html` — individual lesson/exercise pages
- `css.css` — global stylesheet (minimal; most pages use inline `<style>`)
- `img/` — shared images referenced via `./img/<name>.png|jpg`

## Conventions
- Pages are self-contained; each has its own inline `<style>` block.
- Image paths are relative (`./img/1.png`).
- Language is Chinese (`lang="zh-CN"`).
- All CSS class names, id names, and JS variables must start with `wang_`.
- Every new HTML file must be added to the homepage (`index.html`) page list.
