# Portfolio site

My personal site. A single self-contained `index.html` with no build step, no framework and no external assets beyond Google Fonts. The project charts are embedded directly in the file, so it works offline and anywhere you drop it.

**Live:** https://ayeshabibi8027.github.io

## Hosting it on GitHub Pages

1. Create a public repository named `ayeshabibi8027.github.io` (lowercase, exactly that pattern).
2. Upload the contents of this folder to it, with `index.html` at the root.
3. Wait a minute or two. The site is live at https://ayeshabibi8027.github.io.

Pages turns itself on for a repository named after the account. If the repo has a different name, go to **Settings > Pages**, set Source to *Deploy from a branch*, branch `main`, folder `/ (root)`, and the URL becomes `https://ayeshabibi8027.github.io/repo-name`.

## Editing it

Everything lives in one file.

- **Colours** are CSS custom properties in the `:root` block at the top. Change `--accent` and the whole page follows.
- **Sections** are plain `<section>` elements with ids matching the nav links: `home`, `about`, `skills`, `resume`, `projects`, `services`, `contact`.
- **Project charts** are base64 PNGs inside `<img src="data:image/png;base64,...">`. To swap one, generate a new PNG and replace the string.
- **Repo links on project cards** sit in a `.repo` row directly under the `.stackrow` chips. To add another, copy one of the existing anchors and change the href and label.

## Design notes

Single dark theme by choice rather than by omission, so every colour is set explicitly and the page looks the same on any host background. Tested down to 400px wide. Respects `prefers-reduced-motion`. The email copy button falls back to selecting the text when the clipboard API is unavailable.

Fonts are Sora for display, Plus Jakarta Sans for body and IBM Plex Mono for data and labels.
