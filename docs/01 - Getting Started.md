# Getting Started

Dotify One Design System is a CSS-only design kit for Dotify products. It provides design tokens, utility classes, and 21 ready-to-use component styles — all from a single CDN link.

---

## Quick Install

Add this single `<link>` tag to your HTML `<head>`:

```html
<link rel="stylesheet" href="https://repo.dotify.biz/one/design-system/css/index.css">
```

Or via CSS `@import` (e.g. in a SCSS entry point):

```css
@import url('https://repo.dotify.biz/one/design-system/css/index.css');
```

That's it — no build step, no npm package, no PostCSS required.

---

## Quick Start HTML

A minimal page using the design system:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My App — Dotify</title>
  <link rel="stylesheet" href="https://repo.dotify.biz/one/design-system/css/index.css">
</head>
<body>
  <header class="dotify-navbar">
    <div class="dotify-container dotify-navbar__inner">
      <a href="/" class="dotify-navbar__brand">My App</a>
    </div>
  </header>

  <main class="dotify-container dotify-py-12">
    <h1 class="dotify-text-3xl dotify-font-semibold dotify-mb-4">Hello, Dotify</h1>
    <p class="dotify-text-base dotify-mb-6">Start building with the design system.</p>
    <button class="dotify-btn dotify-btn--primary">Get started</button>
    <button class="dotify-btn dotify-btn--ghost dotify-ml-3">Learn more</button>
  </main>
</body>
</html>
```

---

## Dark Mode

Dark mode responds automatically to the user's OS preference. You can also force dark mode by adding `class="dark"` to the `<html>` element:

```html
<html lang="en" class="dark">
```

Both methods work simultaneously. See [07 - Dark Mode](07%20-%20Dark%20Mode.md) for full details.

---

## Icons

The design system includes a self-hosted Heroicons v2 sprite. Reference icons using the SVG `<use>` pattern:

```html
<svg class="dotify-icon" aria-hidden="true">
  <use href="https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg#home"></use>
</svg>
```

See [08 - Icons](08%20-%20Icons.md) for all available icons and size utilities.

---

## Browser Support

The design system targets all modern evergreen browsers:

| Browser | Minimum version |
|---------|----------------|
| Chrome  | 90+ |
| Firefox | 88+ |
| Safari  | 14+ |
| Edge    | 90+ |

Features used:
- CSS custom properties (variables)
- CSS `clamp()` and `min()`/`max()`
- CSS `mask-image` (for custom checkmarks, radio buttons, select chevrons)
- `:focus-visible` pseudo-class
- `@media (prefers-color-scheme)` and `@media (prefers-reduced-motion)`
- CSS Grid and Flexbox

> Internet Explorer is not supported.

---

## File Structure

```
public/
  css/
    index.css              ← single entry point (CDN link)
    tokens/
      colors.css           ← primitive + semantic colour tokens
      typography.css       ← font import + type tokens
      spacing.css          ← spacing scale
      radii.css            ← border radius tokens
      shadows.css          ← shadow tokens
      z-index.css          ← z-index scale
      breakpoints.css      ← breakpoint tokens
    base/
      reset.css            ← minimal modern CSS reset
      base.css             ← base element styles
    utilities/
      colors.css           ← colour utility classes
      spacing.css          ← padding/margin/gap utilities
      layout.css           ← display/flex/grid/position utilities
      typography.css       ← font/text utility classes
      borders.css          ← border-radius/width/ring utilities
    components/
      button.css           ← .dotify-btn
      badge.css            ← .dotify-badge
      input.css            ← .dotify-input / .dotify-field
      textarea.css         ← .dotify-textarea
      select.css           ← .dotify-select
      checkbox.css         ← .dotify-checkbox
      radio.css            ← .dotify-radio
      toggle.css           ← .dotify-toggle
      alert.css            ← .dotify-alert
      card.css             ← .dotify-card
      modal.css            ← .dotify-modal
      dropdown.css         ← .dotify-dropdown
      navbar.css           ← .dotify-navbar
      sidebar.css          ← .dotify-sidebar
      table.css            ← .dotify-table
      tabs.css             ← .dotify-tabs
      tooltip.css          ← .dotify-tooltip
      spinner.css          ← .dotify-spinner
      avatar.css           ← .dotify-avatar
      breadcrumb.css       ← .dotify-breadcrumb
      pagination.css       ← .dotify-pagination
  icons/
    heroicons-sprite.svg   ← SVG icon sprite
```
