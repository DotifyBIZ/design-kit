# Dotify Design Kit

A versioned, brand-consistent CSS design system for Dotify sites, tools, and WordPress (Elementor).

## Purpose
The Dotify Design System provides a single source of truth for brand colors, typography, layout primitives, and UI components.
It is designed to work across plain HTML/PHP/JS projects and WordPress sites built with Elementor.

No JavaScript. No frameworks. Just clean, predictable CSS.

## Features
- Brand-driven design tokens
- Reusable components (buttons, headings, sections)
- Utility classes for layout and text
- Elementor-safe class naming (`dt-*`)
- Semantic versioning

## Installation

Use the canonical hosted CSS (note: the URL does not include any `/branch` segment):

```html
<link rel="stylesheet" href="https://repo.dotify.biz/brand/design-kit/index.css">
```

WordPress notes:
- The theme may use `.site-header` for the site navigation/branding area — this project treats `.site-header` as a white section (background `#ffffff`) while the site page background uses `#f7f8f9`.
- The class `.site-branding` is intentionally excluded from global font and link overrides; it remains on `Montserrat` and preserves its color and size to match the theme's branding.

## Documentation
See USAGE.md for detailed usage guidelines.

© Dotify. All rights reserved.
