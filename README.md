# kingster121.github.io

Source for [kingster121.github.io](https://kingster121.github.io), the personal site of Qin Xin (OT/ICS security & DFIR).

Plain Jekyll with custom layouts and no theme, so GitHub Pages builds it directly from `main`, without GitHub Actions.

## Layout

| Path | What it is |
|------|------------|
| `index.html` | Home |
| `projects/index.html` | Projects, grouped by `category` |
| `life/index.md` | Life page |
| `_projects/` | One Markdown file per project |
| `_layouts/`, `_includes/` | HTML templates |
| `assets/style.css` | The only stylesheet |
| `resume.pdf` | Linked from the nav (add it at the repo root) |

## Adding a project

Create `_projects/<slug>.md`. It's published at `/projects/<slug>/`.

```yaml
---
title: My Project
description: "One sentence. Used on cards, in search results and in link previews."
category: OT & Security   # OT & Security | DFIR | Hardware | Other
featured: true            # optional: show on Home (first 3, same order as /projects/)
period: "2025 – 2026"     # text shown on cards and the project page
sort_date: 2025-01-01     # start date, used for ordering (newest first)
ongoing: true             # optional: sorts before everything else
tags: [PLC, Modbus]       # optional
youtube: VIDEO_ID         # optional: the ID after watch?v=
images:                   # optional: shown after the text
  - src: /assets/img/my-project.png
    alt: Describe what the image shows
    caption: Optional caption
links:                    # optional
  - label: Source code
    url: https://github.com/...
---

Write the project here in Markdown.
```

Put images in `assets/img/`. Add new categories to `project_categories` in `_config.yml`. Categories with no projects are hidden. Projects without a `sort_date` are listed last in their category.

## Local preview

Needs Ruby and Bundler.

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
