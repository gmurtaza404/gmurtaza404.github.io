# gmurtaza404.github.io

Personal academic website + CV, driven from a **single source of truth**. Add
content in `data/`, push, and GitHub Actions rebuilds both the website and the
PDF CV — they can never drift apart.

## How it works

```
data/publications.bib   ← papers (BibTeX)          ┐
data/talks.yaml         ← talks & posters          │ CV + website
data/teaching.yaml      ← courses                  │
data/mentoring.yaml     ← student advising         ┘
data/service.yaml       ← service (dept + profession)  ┐
data/honors.yaml        ← honors, awards, grants       │ CV only
data/references.yaml    ← references                   ┘
data/about.yaml         ← landing-page text, links, photo  (website only)
        │
        ▼  build.py
        ├── cv/generated/*.tex   →  \input into cv/cv.tex  →  cv.pdf  (compiled in CI)
        └── site/*.html          →  the website
```

- **Publications** live in `data/publications.bib`. The same entry renders as
  `Murtaza G` on the CV and `Ghulam Murtaza` on the site, and powers the
  `[BibTeX]` dropdown. See the comments at the top of the `.bib` for the custom
  fields (`pubtype`, `venue`, `status`, `award`, `pdf`, `code`, ...). Long author
  lists are auto-truncated to "first 3, …, Murtaza G, et al." on the CV/site,
  while the BibTeX block keeps the full list.
- Everything else is YAML. Some files feed **both** the CV and the website
  (talks, teaching, mentoring); others are **CV-only** (service, honors,
  references) and never appear on the site.
- `cv/cv.tex` keeps its original `res.cls` styling. Its dynamic sections are
  `\input` from `cv/generated/` (auto-generated — don't edit those). A handful
  of stable sections (Position, Contact, Education, Appointments) are still
  hand-written directly in `cv/cv.tex`.

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

Edit the relevant file in `data/` and push:

| To add a... | Edit | Shows up on |
|---|---|---|
| Paper | `data/publications.bib` | CV + site |
| Talk / poster | `data/talks.yaml` | CV + site |
| Course | `data/teaching.yaml` | CV + site |
| Mentee | `data/mentoring.yaml` | CV + site |
| Award / grant | `data/honors.yaml` | CV only |
| Service item | `data/service.yaml` | CV only |
| Reference | `data/references.yaml` | CV only |

For stable header sections (Education, Appointments, Contact), edit
`cv/cv.tex` directly. No HTML editing is ever required.
