Bootstrap 3 (iTop Simplex) compatibility
=======================================

Purpose
-------
This file (`bootstrap-compat.css`) provides conservative mapping/overrides so iTop (which ships a precompiled Bootstrap 3 / Bootswatch Simplex stylesheet) visually adapts to the Dotify design tokens and components.

Usage
-----
1. Keep iTop's `bootstrap.min.css` (Simplex) as-is. Do not replace it.
2. Load `bootstrap-compat.css` after iTop's Bootstrap CSS and before or after the design-kit CSS depending on desired override order. Recommended load order:

   - iTop / bootstrap.min.css (Simplex)
   - `bootstrap-compat.css` (this file)
   - `design-kit` compiled CSS

What this covers
-----------------
- Buttons (`.btn`, `.btn-primary`, `.btn-sm`, `.btn-lg`, `.btn-block`)
- Panels (`.panel`, `.panel-body`, `.panel-heading`) mapped to card styles
- Labels (`.label-*`) and badges
- Forms: `.form-control`, `.input-group-addon`, `.form-group` validation states `.has-error`, `.has-warning`, `.has-success`
- Dropdown menus (`.dropdown-menu > li > a`)
- Pagination (`.pagination`)
- Navs (`.nav-tabs`, `.nav-pills`)
- Modals, tooltips, popovers: basic visuals
- Tables: general spacing and header background

Next steps / Testing
--------------------
- Verify in a staging iTop instance: panels, forms (validation), navbar, modals, dropdowns, pagination and tables.
- If you find any Bootswatch Simplex-specific selectors that conflict, send me examples and I will add targeted overrides.
- If you prefer a full Bootstrap rebuild with Dotify tokens, I can produce a Sass theme tied to the exact Bootstrap version used by iTop.

Notes
-----
- Overrides are intentionally conservative: brand colors and `--radius-base` are preserved per your request.
- This file is version-agnostic for Bootstrap 3, but for edge-case parity it's best to test with the exact Simplex build shipped in your iTop installation.
