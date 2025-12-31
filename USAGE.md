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

## Versioning
Versions are immutable and follow semantic versioning. All versions are regression tested on DTA (i.e. non-production) environments to ensure compatibility. Any breaking changes will be announced ahead of time and rolled out slowly.
