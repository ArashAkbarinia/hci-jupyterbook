# Writing Guide

How we add to the book so it stays coherent.

## Workflow

1. Pick an **Outline** chapter. Write in a branch (or directly on `main` for small edits).
2. Preview locally:
   ```bash
   pip install -r requirements.txt
   jupyter-book build book
   # open book/_build/html/index.html
   ```
3. Commit and push to `main`. GitHub Actions builds and publishes automatically.

## Chapter template

Every chapter should have: status admonition, **learning objectives**, a concrete hook, sections, a
**summary**, **exercises**, **further reading**.

## Style

- Write for a first-year undergraduate. Define terms on first use and add them to the [glossary](glossary.md).
- Prefer concrete everyday examples before theory.
- Cite recent work (last 5 years) next to classics. The point of this book is to not be outdated: if a
  claim depends on a technology, date it ("as of 2026").
- Use admonitions: `note`, `tip` (co-author notes), `important` (principles), `seealso` (discussion),
  `caution` (verify).
- Add citations to `book/references.bib` and cite with `` {cite}`key` ``.
- Put runnable demos in notebooks; keep them under 2 minutes and dependency-light.

## Status labels

`Outline` → `Draft` → `Reviewed` → `Stable`. Update the table in the [introduction](../intro.md).
