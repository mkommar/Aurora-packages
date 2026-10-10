# Aurora package site

This repository is the static, GitHub Pages-friendly companion site for the Aurora operating system and its deterministic package output. It keeps the existing `apt/`, `release-manifest.json`, and `sources/` distribution tree intact while providing a multi-page overview for both curious readers and systems builders.

## Run locally

The site has no build-time dependency or external CDN. Serve this directory with any static HTTP server so relative links behave like GitHub Pages:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000/>. The entry point is `index.html`; the other pages are `capabilities.html`, `architecture.html`, `roadmap.html`, `comparison.html`, and `builders.html`.

## Content boundary

The site distinguishes implemented QEMU/documented scope from roadmap work. Concept panels and the animated hero are explicitly labeled as visual mockups, not captured Aurora screenshots or real recordings. The comparison is intentionally high-level and should not be read as a feature audit of Windows 11 or Ubuntu Linux.

## Validation

There is no application build step. Validate the static tree with a local server, check all six HTML documents for parseable markup, and verify relative links remain rooted in this repository. Package artifacts and source metadata are published under `apt/`, `release-manifest.json`, and `sources/`.
