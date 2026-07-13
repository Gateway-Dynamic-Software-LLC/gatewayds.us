# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

The marketing site for Gateway Dynamic Software, LLC, an independent mobile app studio. It is a single static HTML file with no build system, no dependencies, and no JavaScript framework — everything (markup, CSS, content) lives in `index.html`.

## Repository structure

- `index.html` — the entire site: `<style>` block in `<head>`, then nav / hero / about / contact / footer sections in `<body>`.
- `CNAME` — GitHub Pages custom domain config (`gatewayds.us`). This confirms the site is deployed via GitHub Pages directly from this repo; do not remove or repurpose this file.

There is no `package.json`, build step, linter, or test suite. To preview changes, just open `index.html` in a browser (or serve the directory with any static file server).

## Conventions in the existing markup

- All styling is done via CSS custom properties defined once in `:root` (`--bg`, `--surface`, `--border`, `--text`, `--muted`, `--accent1`, `--accent2`, `--gradient`). Reuse these variables instead of hardcoding new colors.
- The palette is a dark theme (near-black background, blue/purple gradient accents). Keep new sections visually consistent with this.
- Sections are separated with `<div class="section-divider"></div>`.
- The font is Inter, loaded from Google Fonts via `<link>` tags in `<head>`.
- Layout is plain flexbox/grid with a single mobile breakpoint (`@media (max-width: 680px)`) at the bottom of the `<style>` block — add responsive overrides there rather than inline.
- Contact email currently shown on the page is `support@gatewayds.us` (via `mailto:` links).
