<!-- Copilot / AI agent guidance for hero-dev-portfolio -->
# Copilot instructions

Purpose: Help AI coding agents become productive quickly in this small static portfolio project.

- **Project type:** Single-page static portfolio (no framework, no build step). Entrypoint: `index.html`.
- **Primary assets:** HTML in `index.html`, CSS in `style/style.css`, images in `images/` (icons in `images/icons/`).

Quick start
- Open `index.html` directly in a browser, or serve the folder if relative assets need HTTP (`python -m http.server 8000` or `npx http-server .`).

Key structure & patterns
- Sections are organized by IDs: `#banner`, `#about`, `#skills`, `#resume`. Keep these IDs when adding content so CSS selectors continue to apply.
- Global typography: the `font-open-sans` class on `<body>` ties to the Google font loaded in the `<head>` of `index.html` — preserve the `<link>` tag when editing fonts.
- CSS file: `style/style.css` is the single stylesheet. Note relative URLs inside CSS (e.g., `background: url(../images/developer.png)`), so paths are relative to `style/style.css`.
- Reusable UI pieces use simple class names (e.g., `.section-heading`, `.skill-card`, `.info-card`, `.btn`). Follow existing class names rather than inventing new ones for similar UI.

Content & copy
- The HTML contains placeholder copy and several typos (e.g., `formrly`, `procured`, `resulfs`). When asked to improve copy, confirm whether to correct content or preserve the original text.

Styling notes (actionable)
- Colors: accent uses `.color-orange` and `.btn` uses the same brand color — change in `style/style.css` to update globally.
- Layout: header backgrounds are composed using multiple images from `images/` and are set in `style/style.css` under the `header` selector. If you move or rename images, update these relative paths.

What agents should do first
1. Read `index.html`, `style/style.css`, and `images/` to understand layout and assets.
2. For visual changes, modify `style/style.css` and verify in a browser (live-reload recommended).
3. For content edits, update `index.html` and ask the user if copy corrections are desired.

Constraints & gotchas
- There is no JS build/test pipeline in the repo — avoid introducing complex build tooling unless the user requests it.
- Paths in CSS are relative to the CSS file; paths in HTML are relative to the HTML file. Double-check when moving files.

Examples
- To change the hero text: update the `<section id="banner">` block in `index.html` and tune sizes in `#banner .banner-content` in `style/style.css`.
- To add a new skill card: replicate the `.skill-card` structure inside `.skill-box` and drop a small icon into `images/icons/`.

When uncertain
- Ask the user whether to: (A) preserve current placeholder copy, (B) correct typos and rewrite copy, or (C) replace images.

If you make edits, include a brief CHANGELOG entry in the PR description summarizing files changed and the visual impact.

-- End of instructions --
