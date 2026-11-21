# ಸುದರ್ಶನ್ ಎಚ್ ವೈ — ಕನ್ನಡ ಕವನಗಳು

Personal site of Kannada poems, built with [Hugo](https://gohugo.io) and the
[Polar](https://github.com/ArjunHaritsa/hugo-theme-polar) theme (git submodule, used unchanged).

## Local development

Requires Hugo ≥ 0.158 (standard edition is enough).

```sh
git clone --recurse-submodules <repo-url>
cd <repo>
hugo server
```

New poem: `hugo new content posts/<slug>.md`, then add the title and the poem text.
Line breaks are kept exactly as typed (`hardWraps`), so poems need no special formatting.

## Layout

| Path | Purpose |
| --- | --- |
| `content/posts/` | Poems (ಬರಹಗಳು) |
| `content/aboutme.md` | ನನ್ನ ಬಗ್ಗೆ — set `cover` to the real photo in `static/images/` |
| `i18n/kn.toml` | Kannada interface text for the theme |
| `data/accents.toml` | Accent colours with Kannada names |
| `hugo.toml` | Site configuration and menu |

## Deployment

Pushing to `main` builds the site with GitHub Actions and publishes it to GitHub Pages
(`.github/workflows/hugo.yaml`). In the repo settings, set **Pages → Source** to **GitHub Actions**.
