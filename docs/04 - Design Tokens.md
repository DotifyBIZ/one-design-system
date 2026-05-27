# Design Tokens

Design tokens are the foundational named values of the Dotify One Design System. All components and utilities reference these tokens — never raw hex codes or magic numbers.

---

## Token Naming Convention

Tokens follow the pattern: `--dotify-{category}-{property}`

Examples:
- `--dotify-color-primary` — semantic colour token
- `--dotify-red-600` — primitive colour token
- `--dotify-spacing-4` — spacing token
- `--dotify-text-base` — font size token
- `--dotify-radius` — default border radius

---

## All Tokens Reference

### Colour Tokens — Semantic

```css
/* Primary (Dotify Red) */
--dotify-color-primary
--dotify-color-primary-hover
--dotify-color-primary-active
--dotify-color-primary-light
--dotify-color-primary-fg

/* Secondary (Dotify Indigo) */
--dotify-color-secondary
--dotify-color-secondary-hover
--dotify-color-secondary-active
--dotify-color-secondary-light
--dotify-color-secondary-fg

/* Surface */
--dotify-color-surface
--dotify-color-surface-raised
--dotify-color-surface-inset
--dotify-color-surface-overlay

/* Text / on-surface */
--dotify-color-on-surface
--dotify-color-on-surface-muted
--dotify-color-on-surface-faint

/* Borders */
--dotify-color-border
--dotify-color-border-strong

/* Status */
--dotify-color-success
--dotify-color-success-light
--dotify-color-error
--dotify-color-error-light
--dotify-color-warning
--dotify-color-warning-light

/* Focus */
--dotify-color-focus-ring
```

### Colour Tokens — Primitives

Each brand colour has steps 50, 100, 200, 300, 400, 500, 600, 700, 800, 900, 950.

```css
/* Red: --dotify-red-{50-950} */
/* Indigo: --dotify-indigo-{50-950} */
/* Blue: --dotify-blue-{50-950} */
/* Fuchsia: --dotify-fuchsia-{50-950} */
/* Green: --dotify-green-{50-950} */
/* Yellow: --dotify-yellow-{50-950} */
/* Error: --dotify-error-{50-950} */
/* Gray: --dotify-gray-{50-950} */
```

See [02 - Brand Colours](02%20-%20Brand%20Colours.md) for all hex values.

### Typography Tokens

```css
/* Font families */
--dotify-font-body
--dotify-font-heading
--dotify-font-mono

/* Font weights */
--dotify-font-weight-normal      /* 400 */
--dotify-font-weight-semibold    /* 600 */

/* Font sizes */
--dotify-text-xs                 /* 0.75rem */
--dotify-text-sm                 /* 0.875rem */
--dotify-text-base               /* 1rem */
--dotify-text-lg                 /* 1.125rem */
--dotify-text-xl                 /* 1.25rem */
--dotify-text-2xl                /* 1.5rem */
--dotify-text-3xl                /* 1.875rem */
--dotify-text-4xl                /* 2.25rem */
--dotify-text-5xl                /* 3rem */

/* Line heights */
--dotify-leading-tight           /* 1.25 */
--dotify-leading-snug            /* 1.375 */
--dotify-leading-normal          /* 1.5 */
--dotify-leading-relaxed         /* 1.625 */
--dotify-leading-loose           /* 2 */

/* Letter spacing */
--dotify-tracking-tight          /* -0.05em */
--dotify-tracking-normal         /* 0 */
--dotify-tracking-wide           /* 0.025em */
--dotify-tracking-wider          /* 0.05em */
--dotify-tracking-widest         /* 0.1em */
```

### Spacing Tokens

Mirrors Tailwind's spacing scale for easy migration. Decimal steps use hyphens.

```css
--dotify-spacing-0               /* 0px */
--dotify-spacing-px              /* 1px */
--dotify-spacing-0-5             /* 2px */
--dotify-spacing-1               /* 4px */
--dotify-spacing-1-5             /* 6px */
--dotify-spacing-2               /* 8px */
--dotify-spacing-2-5             /* 10px */
--dotify-spacing-3               /* 12px */
--dotify-spacing-3-5             /* 14px */
--dotify-spacing-4               /* 16px */
--dotify-spacing-5               /* 20px */
--dotify-spacing-6               /* 24px */
--dotify-spacing-7               /* 28px */
--dotify-spacing-8               /* 32px */
--dotify-spacing-9               /* 36px */
--dotify-spacing-10              /* 40px */
--dotify-spacing-11              /* 44px */
--dotify-spacing-12              /* 48px */
--dotify-spacing-14              /* 56px */
--dotify-spacing-16              /* 64px */
--dotify-spacing-20              /* 80px */
--dotify-spacing-24              /* 96px */
--dotify-spacing-28              /* 112px */
--dotify-spacing-32              /* 128px */
--dotify-spacing-36              /* 144px */
--dotify-spacing-40              /* 160px */
--dotify-spacing-44              /* 176px */
--dotify-spacing-48              /* 192px */
--dotify-spacing-52              /* 208px */
--dotify-spacing-56              /* 224px */
--dotify-spacing-60              /* 240px */
--dotify-spacing-64              /* 256px */
--dotify-spacing-72              /* 288px */
--dotify-spacing-80              /* 320px */
--dotify-spacing-96              /* 384px */
```

### Border Radius Tokens

Only three values — intentionally simple.

```css
--dotify-radius-none             /* 0px */
--dotify-radius                  /* 15px (default) */
--dotify-radius-full             /* 9999px (pill/circle) */
```

### Shadow Tokens

```css
--dotify-shadow-none
--dotify-shadow-sm
--dotify-shadow                  /* DEFAULT */
--dotify-shadow-md
--dotify-shadow-lg
--dotify-shadow-xl
--dotify-shadow-2xl
--dotify-shadow-inner
```

### Z-Index Tokens

```css
--dotify-z-base                  /* 0 */
--dotify-z-raised                /* 1 */
--dotify-z-dropdown              /* 10 */
--dotify-z-sticky                /* 20 */
--dotify-z-overlay               /* 30 */
--dotify-z-modal                 /* 40 */
--dotify-z-toast                 /* 50 */
```

### Breakpoint Tokens

Reference-only tokens (not usable in `calc()` — use `@media` queries directly).

```css
--dotify-breakpoint-sm           /* 640px */
--dotify-breakpoint-md           /* 768px */
--dotify-breakpoint-lg           /* 1024px */
--dotify-breakpoint-xl           /* 1280px */
--dotify-breakpoint-2xl          /* 1536px */
```

---

## Using Tokens in Custom CSS

You can reference these tokens in your own stylesheets:

```css
.my-component {
  background-color: var(--dotify-color-surface-raised);
  border: 1px solid var(--dotify-color-border);
  border-radius: var(--dotify-radius);
  padding: var(--dotify-spacing-6);
  color: var(--dotify-color-on-surface);
  font-family: var(--dotify-font-body);
  font-size: var(--dotify-text-sm);
  box-shadow: var(--dotify-shadow-sm);
}
```

Dark mode will apply automatically as long as you use semantic tokens (not primitive ones).

---

## Two-Layer Token Architecture

```
Primitive:  --dotify-red-600: #B41618
                     ↓
Semantic:   --dotify-color-primary: var(--dotify-red-600)
                     ↓
Component:  background-color: var(--dotify-color-primary)
```

**Rule:** Components and custom styles should only ever use **semantic tokens**. Primitive tokens are for defining the scale only.
