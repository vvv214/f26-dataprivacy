# F26 Data Privacy

Undergraduate-oriented Fall 2026 draft of the UVA Data Privacy course site.

Published site:

- <https://tianhao.wang/f26-dataprivacy/>

## Public pages

- `index.md`
- `schedule.md`
- `lab.md`
- `project.md`
- `project-rubric.md`
- `project-present.md`
- `policy.md`

Private lab assets, student submissions, grading notes, and draft notes are intentionally not tracked in this repository.

## Local preview

```bash
bundle exec jekyll serve
```

## Publishing

This repository publishes with GitHub Pages through `.github/workflows/pages.yml`.

1. Commit changes on the `gh-pages` branch.
2. Push to `origin/gh-pages`.
3. GitHub Actions builds the Jekyll site with the repository base path.

The project URL should match the repository name, so this site should live under `/f26-dataprivacy/`.
