# F26 Data Privacy

Undergraduate-oriented Fall 2026 UVA Data Privacy course site.

Published site:

- <https://tianhao.wang/f26-dataprivacy/>

## Public pages

- `index.md`
- `overview.md`
- `assets/images/` (source-grounded overview images)
- `schedule.md`
- `syllabus.md`
- `lab.md`
- `project.md`
- `project-rubric.md`
- `project-present.md`
- `policy.md`

## Lab files

The local working copy may contain a `labs/` folder with notebooks, helper code,
small model checkpoints, and setup notes. That folder is intentionally ignored by
git and excluded from Jekyll processing. Use it for local editing, Canvas/Drive
distribution, or any private course workflow.

Do not commit lab releases, private lab solutions, grading scripts, student
submissions, or scratch build directories to this public site repository.

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

## Private material policy

Keep these out of the repository:

- student data and submissions
- grading notes and autograders
- solution notebooks
- lab release folders and checkpoints
- private drafts in `notes/` or `materials/`
- local build products such as `_site/`, `vendor/`, `.venv/`, and `labs/mp-spdz/`
