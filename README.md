# Human–Computer Interaction — a living textbook

A Jupyter Book on HCI for bachelor students, covering classic foundations and newer topics: AI agents,
multimodal/immersive interaction, and brain–machine / brain–computer interfaces (BMI/BCI).

Live book: https://arashakbarinia.github.io/hci-jupyterbook/ (after the first deploy, see below)

## Build locally

```bash
pip install -r requirements.txt
jupyter-book build book          # output: book/_build/html/index.html
```

## Repository layout

```
book/
  _config.yml        book settings (title, repo URL, execution)
  _toc.yml           table of contents: add new chapters here
  intro.md           landing page and chapter status table
  foundations/ modalities/ design/ ai/ brain/ future/ appendix/
  references.bib     citations
.github/workflows/deploy.yml   builds and publishes to GitHub Pages on push to main
```

## Publishing (one-time setup)

1. Merge this branch into `main`.
2. On GitHub: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. The *Build and deploy book* workflow runs on every push to `main`. The book appears at
   `https://arashakbarinia.github.io/hci-jupyterbook/`.

### Serving it at `arashakbarinia.github.io/projects/hci/`

A project repository is always served under its own repo name, so this repo cannot directly appear at
`/projects/hci/` of your personal site. Two options:

- **Redirect (simplest):** in your `arashakbarinia.github.io` repo add `projects/hci/index.html`:
  ```html
  <!doctype html><meta charset="utf-8">
  <meta http-equiv="refresh" content="0; url=https://arashakbarinia.github.io/hci-jupyterbook/">
  <link rel="canonical" href="https://arashakbarinia.github.io/hci-jupyterbook/">
  ```
- **Exact path:** rename this repo's Pages path by copying the built HTML into
  `arashakbarinia.github.io/projects/hci/` (e.g. a workflow that pushes `book/_build/html` there), and set
  `html.baseurl` in `book/_config.yml` to `https://arashakbarinia.github.io/projects/hci/`.

## Contributing / writing

See `book/appendix/writing-guide.md`. License: see `LICENSE`.
