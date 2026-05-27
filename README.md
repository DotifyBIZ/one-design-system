# Dotify One Design System

A CSS-only design kit for Dotify products. One stylesheet, 21 components, zero build step.

---

## Quick Start

```html
<link rel="stylesheet" href="https://repo.dotify.biz/one/design-system/css/index.css">
```

That's it. No npm, no PostCSS, no build tooling required.

---

## What's Included

| Layer | Contents |
|-------|----------|
| **Tokens** | Colour scales, semantic tokens, typography, spacing, radii, shadows, z-index, breakpoints |
| **Base** | Modern CSS reset + base element styles |
| **Utilities** | Colour, spacing, layout, typography, border utilities |
| **Components** | 21 ready-to-use components |
| **Icons** | Self-hosted Heroicons v2 outline SVG sprite |

---

## Components

| Component | Class | Description |
|-----------|-------|-------------|
| Button | `.dotify-btn` | Primary, secondary, ghost, danger, link variants |
| Badge | `.dotify-badge` | Tinted and filled colour variants |
| Input | `.dotify-input` | Text input with field wrapper pattern |
| Textarea | `.dotify-textarea` | Multi-line text input |
| Select | `.dotify-select` | Custom styled select dropdown |
| Checkbox | `.dotify-checkbox` | Custom styled checkbox |
| Radio | `.dotify-radio` | Custom styled radio button |
| Toggle | `.dotify-toggle` | Switch / toggle control |
| Alert | `.dotify-alert` | Success, error, warning alert banners |
| Card | `.dotify-card` | Content card with header/body/footer |
| Modal | `.dotify-modal` | Dialog / overlay panel |
| Dropdown | `.dotify-dropdown` | Context menu / action dropdown |
| Navbar | `.dotify-navbar` | Sticky top navigation bar |
| Sidebar | `.dotify-sidebar` | Side navigation panel |
| Table | `.dotify-table` | Data table with modifiers |
| Tabs | `.dotify-tabs` | Tab navigation with panels |
| Tooltip | `.dotify-tooltip` | Hover/focus tooltip |
| Spinner | `.dotify-spinner` | Loading indicator |
| Avatar | `.dotify-avatar` | User avatar with initials/image/status |
| Breadcrumb | `.dotify-breadcrumb` | Breadcrumb navigation |
| Pagination | `.dotify-pagination` | Page navigation controls |

---

## Brand Colours

| Name | Role | Hex |
|------|------|-----|
| Dotify Red | Primary | `#B41618` |
| Dotify Indigo | Secondary / Primary Secondary | `#211F60` |
| Dotify Blue | Accent | `#1F628E` |
| Dotify Fuchsia | Accent | `#8E1F62` |
| Dotify Green | Accent / Success | `#158C36` |
| Dotify Yellow | Accent / Warning | `#EDD83D` |

---

## Dark Mode

Both system preference and manual toggle are supported:

```html
<!-- Force dark mode -->
<html class="dark">

<!-- JS toggle -->
<script>
  document.documentElement.classList.toggle('dark');
</script>
```

---

## Icons

Self-hosted Heroicons v2 sprite:

```html
<svg class="dotify-icon" aria-hidden="true">
  <use href="https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg#home"></use>
</svg>
```

---

## Documentation

| Doc | Contents |
|-----|----------|
| [01 - Getting Started](docs/01%20-%20Getting%20Started.md) | Install, quick start, file structure |
| [02 - Brand Colours](docs/02%20-%20Brand%20Colours.md) | All colour palettes with hex values |
| [03 - Typography](docs/03%20-%20Typography.md) | Font scale, tokens, utilities |
| [04 - Design Tokens](docs/04%20-%20Design%20Tokens.md) | Full token reference |
| [05 - Spacing & Layout](docs/05%20-%20Spacing%20%26%20Layout.md) | Spacing scale, flex/grid utilities |
| [06 - Components](docs/06%20-%20Components.md) | All 21 components with HTML examples |
| [07 - Dark Mode](docs/07%20-%20Dark%20Mode.md) | Dark mode setup and implementation |
| [08 - Icons](docs/08%20-%20Icons.md) | Icon usage and full icon list |
| [09 - Accessibility](docs/09%20-%20Accessibility.md) | WCAG AA compliance, ARIA patterns |
| [10 - Contributing](docs/10%20-%20Contributing.md) | Adding tokens, components, PR checklist |

**AI Reference:** [public/llms.md](public/llms.md)

---

## CDN Links

| Asset | URL |
|-------|-----|
| CSS | `https://repo.dotify.biz/one/design-system/css/index.css` |
| Icons | `https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg` |
| AI Ref | `https://repo.dotify.biz/one/design-system/llms.md` |

---

## Versioning

<!-- Version: v1.0.0 -->

---

## License

Dotify One Design System — © Dotify. All rights reserved.  
Icon set: [Heroicons](https://heroicons.com/) — MIT License.
