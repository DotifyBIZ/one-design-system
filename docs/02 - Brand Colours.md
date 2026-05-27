# Brand Colours

The Dotify One Design System uses a two-layer colour system: **primitive scales** (exact hex values) and **semantic tokens** (purpose-driven aliases). Components only reference semantic tokens, making theme changes and dark mode straightforward.

---

## Semantic Colour Tokens

### Primary — Dotify Red

Dotify Red is the brand's primary colour, used for primary calls-to-action, highlights, and brand accents.

| Token | Light | Dark |
|-------|-------|------|
| `--dotify-color-primary` | `#B41618` (red-600) | red-500 |
| `--dotify-color-primary-hover` | red-700 | red-400 |
| `--dotify-color-primary-active` | red-800 | red-300 |
| `--dotify-color-primary-light` | red-50 | red-950 |
| `--dotify-color-primary-fg` | `#ffffff` | `#ffffff` |

**WCAG:** White on `#B41618` ≈ **6.55:1** (AA Large ✓, AAA Large ✓)

### Secondary — Dotify Indigo

Dotify Indigo is the "primary secondary" — the most-used accent for secondary buttons, ghost borders, focus rings, active tabs, and links.

| Token | Light | Dark |
|-------|-------|------|
| `--dotify-color-secondary` | `#211F60` (indigo-600) | indigo-400 |
| `--dotify-color-secondary-hover` | indigo-700 | indigo-300 |
| `--dotify-color-secondary-active` | indigo-800 | indigo-200 |
| `--dotify-color-secondary-light` | indigo-50 | indigo-950 |
| `--dotify-color-secondary-fg` | `#ffffff` | indigo-950 |

**WCAG:** White on `#211F60` ≈ **14.85:1** (AA ✓, AAA ✓)

### Surface & On-Surface

| Token | Light | Dark |
|-------|-------|------|
| `--dotify-color-surface` | `#ffffff` | gray-900 |
| `--dotify-color-surface-raised` | `#ffffff` | gray-800 |
| `--dotify-color-surface-inset` | gray-50 | gray-850 |
| `--dotify-color-surface-overlay` | `#ffffff` | gray-800 |
| `--dotify-color-on-surface` | gray-900 | gray-50 |
| `--dotify-color-on-surface-muted` | gray-600 | gray-400 |
| `--dotify-color-on-surface-faint` | gray-400 | gray-600 |

### Borders

| Token | Light | Dark |
|-------|-------|------|
| `--dotify-color-border` | gray-200 | gray-700 |
| `--dotify-color-border-strong` | gray-400 | gray-600 |

### Status Colours

| Token | Light | Dark | Purpose |
|-------|-------|------|---------|
| `--dotify-color-success` | green-600 | green-400 | Success states |
| `--dotify-color-success-light` | green-50 | green-950 | Success backgrounds |
| `--dotify-color-error` | error-600 (#D91A1D) | error-400 | Error/danger states |
| `--dotify-color-error-light` | error-50 | error-950 | Error backgrounds |
| `--dotify-color-warning` | yellow-500 | yellow-400 | Warning states |
| `--dotify-color-warning-light` | yellow-50 | yellow-950 | Warning backgrounds |

### Focus

| Token | Light | Dark |
|-------|-------|------|
| `--dotify-color-focus-ring` | indigo-600 | indigo-300 |

---

## Primitive Colour Scales

Each brand colour has a full 11-step scale (50 → 950). The value in brackets is the base/default shade.

### Dotify Red `[600 = #B41618]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#fef2f2` |
| 100 | `#fee2e2` |
| 200 | `#fecaca` |
| 300 | `#fca5a5` |
| 400 | `#f87171` |
| 500 | `#d93234` |
| **600** | **`#B41618`** |
| 700 | `#991213` |
| 800 | `#7f0f10` |
| 900 | `#670c0d` |
| 950 | `#450809` |

### Dotify Indigo `[600 = #211F60]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#eef2ff` |
| 100 | `#e0e7ff` |
| 200 | `#c7d2fe` |
| 300 | `#a5b4fc` |
| 400 | `#818cf8` |
| 500 | `#3730a3` |
| **600** | **`#211F60`** |
| 700 | `#1a1849` |
| 800 | `#141233` |
| 900 | `#0e0d22` |
| 950 | `#080711` |

### Dotify Blue `[600 = #1F628E]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#eff6ff` |
| 100 | `#dbeafe` |
| 200 | `#bfdbfe` |
| 300 | `#93c5fd` |
| 400 | `#60a5fa` |
| 500 | `#3b82f6` |
| **600** | **`#1F628E`** |
| 700 | `#1a4e72` |
| 800 | `#163c56` |
| 900 | `#112b3d` |
| 950 | `#0a1929` |

### Dotify Fuchsia `[600 = #8E1F62]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#fdf4ff` |
| 100 | `#fae8ff` |
| 200 | `#f5d0fe` |
| 300 | `#f0abfc` |
| 400 | `#e879f9` |
| 500 | `#d946ef` |
| **600** | **`#8E1F62`** |
| 700 | `#72184e` |
| 800 | `#56123a` |
| 900 | `#3a0c27` |
| 950 | `#1e0614` |

### Dotify Green `[600 = #158C36]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#f0fdf4` |
| 100 | `#dcfce7` |
| 200 | `#bbf7d0` |
| 300 | `#86efac` |
| 400 | `#4ade80` |
| 500 | `#22c55e` |
| **600** | **`#158C36`** |
| 700 | `#1070ab` — wait, corrected: `#107028` |
| 800 | `#0d541e` |
| 900 | `#0a3c15` |
| 950 | `#05210b` |

### Dotify Yellow `[400 = #EDD83D]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#fefce8` |
| 100 | `#fef9c3` |
| 200 | `#fef08a` |
| 300 | `#fde047` |
| **400** | **`#EDD83D`** |
| 500 | `#caab1e` |
| 600 | `#a88c12` |
| 700 | `#86700c` |
| 800 | `#645507` |
| 900 | `#433904` |
| 950 | `#221d02` |

### Error Red `[600 = #D91A1D]`

| Step | Approximate Hex |
|------|----------------|
| 50 | `#fff1f2` |
| 100 | `#ffe4e6` |
| 200 | `#fecdd3` |
| 300 | `#fda4af` |
| 400 | `#fb7185` |
| 500 | `#f43f5e` |
| **600** | **`#D91A1D`** |
| 700 | `#be123c` |
| 800 | `#9f1239` |
| 900 | `#881337` |
| 950 | `#4c0519` |

### Gray (Tailwind verbatim)

| Step | Hex |
|------|-----|
| 50 | `#f9fafb` |
| 100 | `#f3f4f6` |
| 200 | `#e5e7eb` |
| 300 | `#d1d5db` |
| 400 | `#9ca3af` |
| 500 | `#6b7280` |
| 600 | `#4b5563` |
| 700 | `#374151` |
| 800 | `#1f2937` |
| 900 | `#111827` |
| 950 | `#030712` |

---

## Using Colour Utilities

```html
<!-- Text colour -->
<p class="dotify-text-primary">Dotify Red text</p>
<p class="dotify-text-secondary">Dotify Indigo text</p>
<p class="dotify-text-success">Success green text</p>

<!-- Background colour -->
<div class="dotify-bg-primary-light dotify-p-4">Primary tinted background</div>

<!-- Border colour -->
<div class="dotify-border-1 dotify-border-color-secondary dotify-p-4">Indigo border</div>
```
