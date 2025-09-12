# Deployment Guide

This short guide shows two simple ways to publish the whitepaper content in this repository.

1) GitHub Pages (recommended for static Markdown sites)
- The repository already contains plain Markdown files and a CSS file at `assets/styles.css`.
- To publish via GitHub Pages (repository site):
  - In the repository Settings → Pages, set the source to branch `main` and folder `/ (root)` or use `docs/` if you prefer.
  - Push your `main` branch to GitHub. GitHub Pages will serve the repo as a static site. Note: GitHub's native Markdown rendering will not always include the `<link>` tag in the page head. For consistent styling consider using a static site generator (see below).

2) GitBook or other static site generators (recommended for nicer navigation and theming)
- GitBook: Create a new GitBook space and connect the repository or import the repository. GitBook will use `SUMMARY.md` for navigation. For styles, use GitBook's theme settings or add your CSS in the space settings (GitBook may ignore raw `<link>` tags inside Markdown files).
- Static site generator (MkDocs / Hugo / Jekyll): These will let you control the rendered HTML head so `assets/styles.css` is correctly included site-wide.

Notes & tips
- Relative CSS paths: Files in subfolders reference `../assets/styles.css`; root files reference `assets/styles.css`. If you move files or use a generator, update paths accordingly.
- Fonts: If you want Google Fonts, add a `<link>` to `index.html` or your site head template rather than in each Markdown file.
- Images: Put images into `assets/` and reference them relatively (e.g., `assets/image.png` from root pages or `../assets/image.png` from subfolders).

If you want, I can:
- Add a `docs/` version of this site ready for GitHub Pages.
- Create a small MkDocs or Jekyll scaffold to render the site with the CSS applied globally.
