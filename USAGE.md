# Dotify Design System – Usage Guide

## Supported Environments
- HTML / PHP / JavaScript
- WordPress (Elementor)
- Internal tools

## Core Rules
- Never hardcode brand colors
- Never override tokens per page
- Use provided classes instead of inline styles

## Layout

Use dt-container to center content:

```html
<div class="dt-container">...</div>
```

Use dt-section for vertical spacing:

```html
<section class="dt-section dt-section--grey">
  <div class="dt-container">...</div>
</section>
```

## Buttons

```html
<a class="dt-btn dt-btn--primary">Primary</a>
```

## Elementor Guidelines
- Use CSS Classes, not widget custom CSS
- Avoid Elementor global styles
- Let spacing be handled by the design system

### Headings and integration guidance

- The design kit applies a lightweight reset to heading elements to enforce consistent typography. This can conflict with some themes or Elementor global styles.
- If you see conflicts, use one of these strategies:
  - Scope the kit by wrapping pages or parts of a page with a wrapper class and prefix selectors (e.g., `.dt-wrapper h1 { ... }`).
  - Ensure the kit's stylesheet is loaded after the theme/Elementor styles so it can take precedence for components you want to control.
  - Prefer using `dt-` prefixed classes (e.g., `dt-h1`) on elements to avoid touching global element selectors.
  - Avoid enabling Elementor global typography if you plan to use the kit's global resets.

Best practice: when installing in WordPress/iTop, load the kit after the existing theme CSS and test pages with common widgets (headings, navbars, forms). If needed, create small scoped overrides rather than changing global rules.

## Versioning
Versions are immutable and follow semantic versioning. All versions are regression tested on DTA (i.e. non-production) environments to ensure compatibility. Any breaking changes will be announced ahead of time and rolled out slowly.
