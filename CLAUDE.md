# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static single-page marketing website for **Aadvika Pvt Ltd**, a system-to-system/application-to-application integration consultancy. It consists of a single self-contained HTML file with no build process, no dependencies, and no package manager.

## Development

Open `integration_landing4.html` directly in a browser to preview. No server or build step is required.

To serve locally with a simple HTTP server (avoids CORS issues with external image URLs):

```bash
python3 -m http.server 8080
# or
npx serve .
```

## Architecture

Everything lives in `integration_landing4.html`:

- **CSS** — All styles are in a `<style>` block in `<head>`. Uses CSS custom properties (`:root`) for the brand palette: navy `#1e3a8a`, blue `#1d4ed8`, accent `#3b82f6`. Layout uses CSS Grid and Flexbox throughout.
- **HTML** — Eight anchor-linked sections in order: `#home` (hero), stats bar, `#technologies`, `#services`, `#process` (how we work), `#projects`, `#about`, `#contact`; plus fixed header nav and footer.
- **JavaScript** — Inline `<script>` at bottom handles: hamburger mobile nav toggle, smooth scroll, `IntersectionObserver`-based staggered `.fade-up` animations, and contact form submit feedback (button turns green for 4 s, then resets — no backend).

Brand color scheme: `linear-gradient(135deg, #1e3a8a 0%, #1d4ed8 55%, #3b82f6 100%)` — used on header, hero, buttons, stat cards, and the contact info panel.

Technology logo images are loaded from external URLs (Google Images, worldvectorlogo, GitHub avatars). The `.vscode/settings.json` hides `.mule` directories, suggesting this site is maintained alongside MuleSoft project files.
