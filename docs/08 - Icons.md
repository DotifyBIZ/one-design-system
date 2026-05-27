# Icons

The design system includes a self-hosted **Heroicons v2 Outline** SVG sprite (MIT License). Icons are embedded inline using the SVG `<use>` pattern — no JavaScript required.

---

## Sprite URL

```
https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg
```

---

## Basic Usage

```html
<!-- Always include aria-hidden="true" for decorative icons -->
<svg class="dotify-icon" aria-hidden="true" focusable="false">
  <use href="https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg#home"></use>
</svg>
```

Replace `#home` with any icon ID from the list below.

---

## Icon Sizes

Use size modifier classes on the `<svg>` element:

| Class | Size |
|-------|------|
| `.dotify-icon--xs` | 12px |
| `.dotify-icon--sm` | 16px |
| `.dotify-icon` (default) | 24px |
| `.dotify-icon--lg` | 32px |
| `.dotify-icon--xl` | 40px |
| `.dotify-icon--2xl` | 48px |

```html
<svg class="dotify-icon dotify-icon--sm" aria-hidden="true">
  <use href="…#magnifying-glass"></use>
</svg>
```

---

## Icon Colours

Icons inherit `currentColor` — set colour via CSS `color`:

```html
<!-- Utility class -->
<svg class="dotify-icon dotify-icon--primary" aria-hidden="true">…</svg>
<svg class="dotify-icon dotify-icon--secondary" aria-hidden="true">…</svg>
<svg class="dotify-icon dotify-icon--success" aria-hidden="true">…</svg>
<svg class="dotify-icon dotify-icon--error" aria-hidden="true">…</svg>
<svg class="dotify-icon dotify-icon--muted" aria-hidden="true">…</svg>

<!-- Or via Tailwind-style text colour utility -->
<svg class="dotify-icon dotify-text-secondary" aria-hidden="true">…</svg>
```

---

## Accessible Icon-Only Buttons

When an icon is the only content in a button, provide an accessible label:

```html
<button class="dotify-btn dotify-btn--ghost dotify-btn--icon" aria-label="Delete item">
  <svg class="dotify-icon" aria-hidden="true">
    <use href="…#trash"></use>
  </svg>
</button>
```

---

## Accessible Inline Icons with Text

When an icon accompanies visible text, hide it from screen readers:

```html
<button class="dotify-btn dotify-btn--primary">
  <svg class="dotify-icon dotify-icon--sm" aria-hidden="true">
    <use href="…#plus"></use>
  </svg>
  Add item
</button>
```

---

## Available Icons

### Navigation
| ID | Description |
|----|-------------|
| `home` | Home / house |
| `bars-3` | Hamburger menu |
| `x-mark` | Close / dismiss |
| `chevron-down` | Caret down |
| `chevron-up` | Caret up |
| `chevron-left` | Caret left |
| `chevron-right` | Caret right |
| `ellipsis-horizontal` | More options (…) |

### Arrows
| ID | Description |
|----|-------------|
| `arrow-right` | Arrow right |
| `arrow-left` | Arrow left |
| `arrow-up` | Arrow up |
| `arrow-down` | Arrow down |
| `arrow-up-tray` | Upload |
| `arrow-down-tray` | Download |
| `arrow-path` | Refresh / reload |

### Actions
| ID | Description |
|----|-------------|
| `plus` | Add |
| `minus` | Remove / subtract |
| `check` | Checkmark |
| `pencil` | Edit |
| `trash` | Delete |
| `magnifying-glass` | Search |
| `funnel` | Filter |
| `clipboard-document` | Copy |

### Users & Social
| ID | Description |
|----|-------------|
| `user` | Single user |
| `users` | Multiple users |

### Status & Feedback
| ID | Description |
|----|-------------|
| `bell` | Notifications |
| `check-circle` | Success circle |
| `x-circle` | Error circle |
| `exclamation-circle` | Warning circle |
| `exclamation-triangle` | Caution triangle |
| `information-circle` | Info circle |
| `question-mark-circle` | Help / question |
| `shield-check` | Security / verified |

### Visibility
| ID | Description |
|----|-------------|
| `eye` | Show / visible |
| `eye-slash` | Hide / invisible |

### Communication
| ID | Description |
|----|-------------|
| `envelope` | Email |
| `phone` | Phone |

### Data & Documents
| ID | Description |
|----|-------------|
| `document-text` | Document |
| `folder` | Folder |
| `chart-bar` | Chart / analytics |
| `photo` | Image / photo |
| `calendar` | Date picker |
| `clock` | Time |

### Commerce
| ID | Description |
|----|-------------|
| `credit-card` | Payment |
| `shopping-cart` | Cart |

### Misc
| ID | Description |
|----|-------------|
| `cog-6-tooth` | Settings |
| `lock-closed` | Lock / secure |
| `star` | Favourite |
| `heart` | Like |
| `bookmark` | Save |
| `map-pin` | Location |
| `globe-alt` | Website / global |
| `paper-clip` | Attachment |
| `link` | URL / link |

---

## Using Icons from CDN vs Local

The sprite file is served from the same CDN as the CSS:

```
https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg#icon-id
```

For local development, you can also copy `heroicons-sprite.svg` and reference it relatively:

```html
<use href="/assets/heroicons-sprite.svg#home"></use>
```

> **Note:** `<use href="…">` with an external URL requires the SVG to be served with the correct CORS headers. The Dotify CDN handles this automatically.

---

## Attribution

Icons are from [Heroicons](https://heroicons.com/) by Tailwind Labs, Inc.  
Licensed under [MIT](https://github.com/tailwindlabs/heroicons/blob/master/LICENSE).
