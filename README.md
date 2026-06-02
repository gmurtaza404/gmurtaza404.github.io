# gmurtaza404.github.io

Personal academic website + CV, driven from a **single source of truth**. Add
content in `data/`, push, and GitHub Actions rebuilds both the website and the
PDF CV — they can never drift apart.

## How it works

```
data/publications.bib   ← add a paper here (BibTeX)
data/talks.yaml         ← talks & posters
data/teaching.yaml      ← courses
data/mentoring.yaml     ← student advising
data/about.yaml         ← landing-page text & links
        │
        ▼  build.py
        ├── cv/generated/*.tex   →  \input into cv/cv.tex  →  cv.pdf  (compiled in CI)
        └── site/*.html          →  the website
```

- **Publications** live in `data/publications.bib`. The same entry renders as
  `Murtaza G` on the CV and `Ghulam Murtaza` on the site, and powers the
  `[BibTeX]` dropdown. See the comments at the top of the `.bib` for the custom
  fields (`pubtype`, `venue`, `status`, `award`, `pdf`, `code`, ...).
- Everything else (talks/posters, courses, advising, about) lives in the YAML
  files.
- `cv/cv.tex` keeps its original `res.cls` styling; only the dynamic sections
  are `\input` from `cv/generated/` (auto-generated — don't edit those).

## Build locally

```bash
python3 -m venv .venv
.venv/bin/pip install -r requirements.txt
.venv/bin/python build.py        # writes site/*.html and cv/generated/*.tex
```

Open `site/index.html` in a browser to preview. (Compiling `cv.pdf` needs a
LaTeX install; if you don't have one, just push — CI compiles it for you.)

## Deploy

Pushing to `main` triggers `.github/workflows/build.yml`, which runs `build.py`,
compiles the CV, and deploys `site/` to GitHub Pages. One-time setup: in the
repo, **Settings → Pages → Build and deployment → Source: GitHub Actions**.

## Adding content later

Just edit the relevant file in `data/` and push. For a new paper, add a BibTeX
entry; for a talk, add a YAML block. No HTML or LaTeX editing required.
