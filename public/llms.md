# Dotify One Design System — AI Reference

> Machine-readable reference for AI coding assistants.  
> CDN: `https://repo.dotify.biz/one/design-system/css/index.css`

---

## Installation

```html
<!-- In <head> -->
<link rel="stylesheet" href="https://repo.dotify.biz/one/design-system/css/index.css">
```

Or via CSS `@import`:
```css
@import url('https://repo.dotify.biz/one/design-system/css/index.css');
```

Dark mode: add `class="dark"` to `<html>` for forced dark mode. Both `class="dark"` and `@media (prefers-color-scheme: dark)` are supported.

---

## Design Tokens

### Colours — Primitives

| Token | Value (approx) |
|-------|---------------|
| `--dotify-red-50` … `--dotify-red-950` | Red scale, base `#B41618` at 600 |
| `--dotify-indigo-50` … `--dotify-indigo-950` | Indigo scale, base `#211F60` at 600 |
| `--dotify-blue-50` … `--dotify-blue-950` | Blue scale, base `#1F628E` at 600 |
| `--dotify-fuchsia-50` … `--dotify-fuchsia-950` | Fuchsia scale, base `#8E1F62` at 600 |
| `--dotify-green-50` … `--dotify-green-950` | Green scale, base `#158C36` at 600 |
| `--dotify-yellow-50` … `--dotify-yellow-950` | Yellow scale, base `#EDD83D` at 400 |
| `--dotify-error-50` … `--dotify-error-950` | Error red scale, base `#D91A1D` at 600 |
| `--dotify-gray-50` … `--dotify-gray-950` | Tailwind verbatim gray scale |

### Colours — Semantic Tokens

| Token | Light value | Dark value |
|-------|------------|------------|
| `--dotify-color-primary` | red-600 (#B41618) | red-500 |
| `--dotify-color-primary-hover` | red-700 | red-400 |
| `--dotify-color-primary-active` | red-800 | red-300 |
| `--dotify-color-primary-light` | red-50 | red-950 |
| `--dotify-color-primary-fg` | white | white |
| `--dotify-color-secondary` | indigo-600 (#211F60) | indigo-400 |
| `--dotify-color-secondary-hover` | indigo-700 | indigo-300 |
| `--dotify-color-secondary-active` | indigo-800 | indigo-200 |
| `--dotify-color-secondary-light` | indigo-50 | indigo-950 |
| `--dotify-color-secondary-fg` | white | indigo-950 |
| `--dotify-color-surface` | white | gray-900 |
| `--dotify-color-surface-raised` | white | gray-800 |
| `--dotify-color-surface-inset` | gray-50 | gray-850 |
| `--dotify-color-surface-overlay` | white | gray-800 |
| `--dotify-color-on-surface` | gray-900 | gray-50 |
| `--dotify-color-on-surface-muted` | gray-600 | gray-400 |
| `--dotify-color-on-surface-faint` | gray-400 | gray-600 |
| `--dotify-color-border` | gray-200 | gray-700 |
| `--dotify-color-border-strong` | gray-400 | gray-600 |
| `--dotify-color-success` | green-600 | green-400 |
| `--dotify-color-success-light` | green-50 | green-950 |
| `--dotify-color-error` | error-600 | error-400 |
| `--dotify-color-error-light` | error-50 | error-950 |
| `--dotify-color-warning` | yellow-500 | yellow-400 |
| `--dotify-color-warning-light` | yellow-50 | yellow-950 |
| `--dotify-color-focus-ring` | indigo-600 | indigo-300 |

### Typography

| Token | Value |
|-------|-------|
| `--dotify-font-body` | 'Montserrat', sans-serif |
| `--dotify-font-heading` | 'Montserrat', sans-serif |
| `--dotify-font-mono` | ui-monospace, monospace |
| `--dotify-text-xs` | 0.75rem |
| `--dotify-text-sm` | 0.875rem |
| `--dotify-text-base` | 1rem |
| `--dotify-text-lg` | 1.125rem |
| `--dotify-text-xl` | 1.25rem |
| `--dotify-text-2xl` | 1.5rem |
| `--dotify-text-3xl` | 1.875rem |
| `--dotify-text-4xl` | 2.25rem |
| `--dotify-text-5xl` | 3rem |
| `--dotify-font-weight-normal` | 400 |
| `--dotify-font-weight-semibold` | 600 |
| `--dotify-leading-tight` | 1.25 |
| `--dotify-leading-snug` | 1.375 |
| `--dotify-leading-normal` | 1.5 |
| `--dotify-leading-relaxed` | 1.625 |
| `--dotify-leading-loose` | 2 |
| `--dotify-tracking-tight` | -0.05em |
| `--dotify-tracking-normal` | 0 |
| `--dotify-tracking-wide` | 0.025em |
| `--dotify-tracking-wider` | 0.05em |
| `--dotify-tracking-widest` | 0.1em |

### Spacing (Tailwind-mirrored)

| Token | Value |
|-------|-------|
| `--dotify-spacing-0` | 0px |
| `--dotify-spacing-px` | 1px |
| `--dotify-spacing-0-5` | 2px |
| `--dotify-spacing-1` | 4px |
| `--dotify-spacing-1-5` | 6px |
| `--dotify-spacing-2` | 8px |
| `--dotify-spacing-2-5` | 10px |
| `--dotify-spacing-3` | 12px |
| `--dotify-spacing-3-5` | 14px |
| `--dotify-spacing-4` | 16px |
| `--dotify-spacing-5` | 20px |
| `--dotify-spacing-6` | 24px |
| `--dotify-spacing-7` | 28px |
| `--dotify-spacing-8` | 32px |
| `--dotify-spacing-9` | 36px |
| `--dotify-spacing-10` | 40px |
| `--dotify-spacing-11` | 44px |
| `--dotify-spacing-12` | 48px |
| `--dotify-spacing-14` | 56px |
| `--dotify-spacing-16` | 64px |
| `--dotify-spacing-20` | 80px |
| `--dotify-spacing-24` | 96px |
| `--dotify-spacing-28` | 112px |
| `--dotify-spacing-32` | 128px |
| `--dotify-spacing-36` | 144px |
| `--dotify-spacing-40` | 160px |
| `--dotify-spacing-44` | 176px |
| `--dotify-spacing-48` | 192px |
| `--dotify-spacing-52` | 208px |
| `--dotify-spacing-56` | 224px |
| `--dotify-spacing-60` | 240px |
| `--dotify-spacing-64` | 256px |
| `--dotify-spacing-72` | 288px |
| `--dotify-spacing-80` | 320px |
| `--dotify-spacing-96` | 384px |

### Border Radius

| Token | Value |
|-------|-------|
| `--dotify-radius-none` | 0px |
| `--dotify-radius` | 15px |
| `--dotify-radius-full` | 9999px |

### Shadows

| Token | Value |
|-------|-------|
| `--dotify-shadow-none` | none |
| `--dotify-shadow-sm` | small drop shadow |
| `--dotify-shadow` | medium drop shadow |
| `--dotify-shadow-md` | medium-large |
| `--dotify-shadow-lg` | large |
| `--dotify-shadow-xl` | extra large |
| `--dotify-shadow-2xl` | 2x large |
| `--dotify-shadow-inner` | inset |

### Z-Index

| Token | Value |
|-------|-------|
| `--dotify-z-base` | 0 |
| `--dotify-z-raised` | 1 |
| `--dotify-z-dropdown` | 10 |
| `--dotify-z-sticky` | 20 |
| `--dotify-z-overlay` | 30 |
| `--dotify-z-modal` | 40 |
| `--dotify-z-toast` | 50 |

---

## Utility Classes

### Colours
- `.dotify-text-{semantic}` — text colour (primary, secondary, success, error, warning, muted, faint)
- `.dotify-bg-{semantic}` — background colour
- `.dotify-border-color-{semantic}` — border colour

### Spacing
- `.dotify-p-{n}`, `.dotify-px-{n}`, `.dotify-py-{n}`, `.dotify-pt-{n}`, `.dotify-pr-{n}`, `.dotify-pb-{n}`, `.dotify-pl-{n}`
- `.dotify-m-{n}`, `.dotify-mx-{n}`, `.dotify-my-{n}`, `.dotify-mt-{n}`, `.dotify-mr-{n}`, `.dotify-mb-{n}`, `.dotify-ml-{n}`
- `.dotify-gap-{n}`, `.dotify-gap-x-{n}`, `.dotify-gap-y-{n}`
- `.dotify-space-y-{n}`, `.dotify-space-x-{n}`
- Where `{n}` is a spacing step: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `8`, `10`, `12`, `16`, `20`, `24`, etc.

### Layout
- `.dotify-container` — centred container with responsive max-widths
- `.dotify-flex`, `.dotify-inline-flex`, `.dotify-grid`, `.dotify-block`, `.dotify-inline`, `.dotify-hidden`
- `.dotify-flex-row`, `.dotify-flex-col`, `.dotify-flex-wrap`
- `.dotify-items-{start|center|end|stretch|baseline}`
- `.dotify-justify-{start|center|end|between|around|evenly}`
- `.dotify-flex-{1|auto|none|grow|shrink}`
- `.dotify-grid-cols-{1-12}`, `.dotify-col-span-{1-12}`
- `.dotify-w-full`, `.dotify-h-full`, `.dotify-w-screen`, `.dotify-h-screen`
- `.dotify-max-w-{sm|md|lg|xl|2xl|3xl|4xl|5xl|6xl|7xl|full|none}`
- `.dotify-overflow-{hidden|auto|scroll|visible}`, `.dotify-overflow-x-auto`, `.dotify-overflow-y-auto`
- `.dotify-relative`, `.dotify-absolute`, `.dotify-fixed`, `.dotify-sticky`
- `.dotify-z-{10|20|30|40|50}`
- `.dotify-sr-only` — visually hidden, accessible to screen readers

### Typography
- `.dotify-font-body`, `.dotify-font-heading`, `.dotify-font-mono`
- `.dotify-text-{xs|sm|base|lg|xl|2xl|3xl|4xl|5xl}`
- `.dotify-font-normal`, `.dotify-font-semibold`
- `.dotify-leading-{tight|snug|normal|relaxed|loose}`
- `.dotify-tracking-{tight|normal|wide|wider|widest}`
- `.dotify-text-{left|center|right|justify}`
- `.dotify-uppercase`, `.dotify-lowercase`, `.dotify-capitalize`, `.dotify-normal-case`
- `.dotify-underline`, `.dotify-no-underline`, `.dotify-line-through`
- `.dotify-truncate`, `.dotify-text-ellipsis`, `.dotify-whitespace-nowrap`
- `.dotify-prose` — readable body prose (max-width, line-height)

### Borders
- `.dotify-rounded-none`, `.dotify-rounded`, `.dotify-rounded-full`
- `.dotify-border-{0|1|2|4|8}`, `.dotify-border-t/r/b/l-{0|1|2|4}`
- `.dotify-border-solid`, `.dotify-border-dashed`, `.dotify-border-dotted`
- `.dotify-ring-{1|2|4}` — box-shadow based ring
- `.dotify-divide-y-{1|2}`, `.dotify-divide-x-{1|2}` — child element dividers

---

## Components

### Button — `.dotify-btn`
```html
<button class="dotify-btn dotify-btn--primary">Primary</button>
<button class="dotify-btn dotify-btn--secondary">Secondary</button>
<button class="dotify-btn dotify-btn--ghost">Ghost</button>
<button class="dotify-btn dotify-btn--danger">Danger</button>
<button class="dotify-btn dotify-btn--link">Link</button>
```
Sizes: `dotify-btn--sm`, `dotify-btn--lg`  
Modifiers: `dotify-btn--icon` (square), `dotify-btn--block` (full width)  
Notes: Primary = red, Secondary = indigo (filled), Ghost = indigo outline.

### Badge — `.dotify-badge`
```html
<span class="dotify-badge dotify-badge--primary">New</span>
<span class="dotify-badge dotify-badge--success-filled dotify-badge--pill">Active</span>
```
Variants: `--primary`, `--secondary`, `--success`, `--error`, `--warning`, `--gray`  
Filled variants: add `-filled` suffix  
Modifiers: `--pill` (fully rounded), `--sm`, `--lg`

### Input — `.dotify-input`
```html
<div class="dotify-field">
  <label class="dotify-label" for="email">Email <span class="dotify-label--required">*</span></label>
  <input type="email" id="email" class="dotify-input" placeholder="you@example.com">
  <p class="dotify-field__hint">We'll never share your email.</p>
</div>
```
Invalid: add `dotify-input--invalid`; Disabled: `disabled` attribute  
Sizes: `dotify-input--sm`, `dotify-input--lg`  
Icon adornment: wrap in `.dotify-input-group`

### Textarea — `.dotify-textarea`
```html
<div class="dotify-field">
  <label class="dotify-label" for="bio">Bio</label>
  <textarea id="bio" class="dotify-textarea" rows="4"></textarea>
</div>
```
Modifiers: `dotify-textarea--no-resize`, `dotify-textarea--invalid`

### Select — `.dotify-select`
```html
<div class="dotify-field">
  <label class="dotify-label" for="country">Country</label>
  <div class="dotify-select-wrapper">
    <select id="country" class="dotify-select">
      <option>Australia</option>
    </select>
  </div>
</div>
```

### Checkbox — `.dotify-checkbox`
```html
<label class="dotify-checkbox">
  <input type="checkbox" class="dotify-checkbox__input">
  <span class="dotify-checkbox__label">Accept terms</span>
</label>
```

### Radio — `.dotify-radio`
```html
<fieldset class="dotify-radio-group">
  <legend class="dotify-label">Plan</legend>
  <label class="dotify-radio">
    <input type="radio" class="dotify-radio__input" name="plan" value="free">
    <span class="dotify-radio__label">Free</span>
  </label>
</fieldset>
```
Modifier: `dotify-radio-group--inline`

### Toggle — `.dotify-toggle`
```html
<label class="dotify-toggle">
  <input type="checkbox" class="dotify-toggle__input" role="switch">
  <span class="dotify-toggle__track" aria-hidden="true"></span>
  <span class="dotify-toggle__label">Enable notifications</span>
</label>
```
Sizes: `dotify-toggle--sm`, `dotify-toggle--lg`

### Alert — `.dotify-alert`
```html
<div class="dotify-alert dotify-alert--success" role="alert">
  <svg class="dotify-alert__icon dotify-icon" aria-hidden="true"><use href="…#check-circle"/></svg>
  <div class="dotify-alert__content">
    <p class="dotify-alert__title">Success!</p>
    <p class="dotify-alert__body">Changes saved.</p>
  </div>
</div>
```
Variants: `--success`, `--error`, `--warning`  
Modifier: `--banner` (full-width, no radius)

### Card — `.dotify-card`
```html
<div class="dotify-card">
  <div class="dotify-card__header">
    <h3 class="dotify-card__title">Title</h3>
  </div>
  <div class="dotify-card__body">Content</div>
  <div class="dotify-card__footer">
    <button class="dotify-btn dotify-btn--primary">Action</button>
  </div>
</div>
```
Modifiers: `--interactive`, `--flat`, `--elevated`

### Modal — `.dotify-modal`
```html
<div class="dotify-modal dotify-modal--open" role="dialog" aria-modal="true" aria-labelledby="title">
  <div class="dotify-modal__overlay"></div>
  <div class="dotify-modal__panel">
    <div class="dotify-modal__header">
      <h2 class="dotify-modal__title" id="title">Dialog</h2>
      <button class="dotify-modal__close" aria-label="Close">×</button>
    </div>
    <div class="dotify-modal__body">Content</div>
    <div class="dotify-modal__footer">
      <button class="dotify-btn dotify-btn--ghost">Cancel</button>
      <button class="dotify-btn dotify-btn--primary">Confirm</button>
    </div>
  </div>
</div>
```
Sizes: `--sm`, `--lg`, `--xl`, `--full`  
Toggle: add/remove `dotify-modal--open`

### Dropdown — `.dotify-dropdown`
```html
<div class="dotify-dropdown dotify-dropdown--open">
  <button class="dotify-btn dotify-btn--ghost">Options</button>
  <div class="dotify-dropdown__menu" role="menu">
    <a class="dotify-dropdown__item" href="#">Edit</a>
    <div class="dotify-dropdown__divider"></div>
    <button class="dotify-dropdown__item dotify-dropdown__item--danger">Delete</button>
  </div>
</div>
```
Position modifiers: `--right`, `--up`  
Toggle: add `dotify-dropdown--open` or set `aria-expanded="true"` on trigger

### Navbar — `.dotify-navbar`
```html
<header class="dotify-navbar">
  <div class="dotify-container dotify-navbar__inner">
    <a href="/" class="dotify-navbar__brand">Dotify</a>
    <nav class="dotify-navbar__nav">
      <a href="/" class="dotify-navbar__link dotify-navbar__link--active">Home</a>
    </nav>
    <div class="dotify-navbar__actions">
      <button class="dotify-btn dotify-btn--primary dotify-btn--sm">Sign up</button>
    </div>
  </div>
</header>
```
Modifier: `--branded` (red top accent)

### Sidebar — `.dotify-sidebar`
```html
<aside class="dotify-sidebar">
  <nav class="dotify-sidebar__nav">
    <div class="dotify-sidebar__section">
      <p class="dotify-sidebar__section-label">Main</p>
      <a href="/" class="dotify-sidebar__link dotify-sidebar__link--active">Home</a>
    </div>
  </nav>
</aside>
```
Active state: `dotify-sidebar__link--active` (indigo highlight)

### Table — `.dotify-table`
```html
<div class="dotify-table-wrapper">
  <table class="dotify-table dotify-table--striped">
    <thead><tr><th>Name</th></tr></thead>
    <tbody><tr><td>Alice</td></tr></tbody>
  </table>
</div>
```
Modifiers: `--striped`, `--bordered`, `--hover-rows`, `--compact`

### Tabs — `.dotify-tabs`
```html
<div class="dotify-tabs">
  <div class="dotify-tabs__list" role="tablist">
    <button class="dotify-tabs__tab dotify-tabs__tab--active" role="tab" aria-selected="true">Tab 1</button>
    <button class="dotify-tabs__tab" role="tab" aria-selected="false">Tab 2</button>
  </div>
  <div class="dotify-tabs__panel" role="tabpanel">Panel 1</div>
</div>
```
Modifier: `dotify-tabs--pills` (pill/boxed style)

### Tooltip — `.dotify-tooltip`
```html
<span class="dotify-tooltip-wrapper">
  <button class="dotify-btn dotify-btn--ghost" aria-describedby="tip-1">Hover</button>
  <span class="dotify-tooltip dotify-tooltip--top" id="tip-1" role="tooltip">Hint text</span>
</span>
```
Positions: `--top` (default), `--bottom`, `--left`, `--right`

### Spinner — `.dotify-spinner`
```html
<span class="dotify-spinner dotify-spinner--lg" role="status" aria-label="Loading…"></span>
```
Sizes: `--xs`, `--sm`, (default md), `--lg`, `--xl`  
Variants: `--white`, `--primary`, `--muted`

### Avatar — `.dotify-avatar`
```html
<span class="dotify-avatar dotify-avatar--md">
  <img class="dotify-avatar__image" src="photo.jpg" alt="Alice">
  <span class="dotify-avatar__status dotify-avatar__status--online"></span>
</span>
```
Sizes: `--xs`, `--sm`, (default md), `--lg`, `--xl`, `--2xl`  
Status: `--online`, `--away`, `--busy`, `--offline`  
Colour variants: `--red`, `--blue`, `--green`, `--gray`  
Group: wrap in `.dotify-avatar-group`

### Breadcrumb — `.dotify-breadcrumb`
```html
<nav class="dotify-breadcrumb" aria-label="Breadcrumb">
  <ol class="dotify-breadcrumb__list">
    <li class="dotify-breadcrumb__item"><a href="/" class="dotify-breadcrumb__link">Home</a></li>
    <li class="dotify-breadcrumb__item" aria-hidden="true"><span class="dotify-breadcrumb__separator"></span></li>
    <li class="dotify-breadcrumb__item"><span class="dotify-breadcrumb__current" aria-current="page">Page</span></li>
  </ol>
</nav>
```
Modifier: `--slash` (slash separator)

### Pagination — `.dotify-pagination`
```html
<nav class="dotify-pagination" aria-label="Pagination">
  <a href="#" class="dotify-pagination__prev">← Prev</a>
  <ol class="dotify-pagination__list">
    <li><a href="#" class="dotify-pagination__link dotify-pagination__link--active" aria-current="page">1</a></li>
    <li><a href="#" class="dotify-pagination__link">2</a></li>
  </ol>
  <a href="#" class="dotify-pagination__next">Next →</a>
</nav>
```
Disabled: `dotify-pagination__link--disabled` or `aria-disabled="true"`  
Modifier: `dotify-pagination--compact`

---

## Icons

Self-hosted Heroicons v2 outline SVG sprite at:  
`https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg`

```html
<svg class="dotify-icon" aria-hidden="true">
  <use href="https://repo.dotify.biz/one/design-system/icons/heroicons-sprite.svg#magnifying-glass"></use>
</svg>
```

Available icon IDs: `home`, `bars-3`, `x-mark`, `chevron-down`, `chevron-up`, `chevron-left`, `chevron-right`, `arrow-right`, `arrow-left`, `arrow-up`, `arrow-down`, `arrow-up-tray`, `arrow-down-tray`, `arrow-path`, `plus`, `minus`, `check`, `pencil`, `trash`, `magnifying-glass`, `funnel`, `user`, `users`, `bell`, `check-circle`, `x-circle`, `exclamation-circle`, `exclamation-triangle`, `information-circle`, `question-mark-circle`, `shield-check`, `eye`, `eye-slash`, `envelope`, `phone`, `document-text`, `folder`, `clipboard-document`, `chart-bar`, `credit-card`, `shopping-cart`, `cog-6-tooth`, `lock-closed`, `star`, `heart`, `bookmark`, `map-pin`, `globe-alt`, `paper-clip`, `link`, `photo`, `calendar`, `clock`, `ellipsis-horizontal`

Icon sizes: `.dotify-icon--xs` (12px), `.dotify-icon--sm` (16px), (default 24px), `.dotify-icon--lg` (32px), `.dotify-icon--xl` (40px)

---

## Dark Mode

Both methods are supported simultaneously:

```css
/* Method 1 — system preference */
@media (prefers-color-scheme: dark) { … }

/* Method 2 — manual class on <html> */
<html class="dark">
```

JS toggle snippet:
```js
document.documentElement.classList.toggle('dark');
```

---

## Accessibility

- All interactive components support `:focus-visible` using `--dotify-color-focus-ring` (indigo)
- Use `.dotify-sr-only` for visually-hidden accessible labels
- Modals use `role="dialog"` + `aria-modal="true"` + `aria-labelledby`
- Form fields: always associate `<label>` via `for`/`id`; use `.dotify-label--required` + `required` attribute
- Tabs: `role="tablist"`, `role="tab"`, `aria-selected`, `role="tabpanel"`, `aria-labelledby`
- Colour contrast: white on primary red (#B41618) ≈ 6.55:1 ✓; white on secondary indigo (#211F60) ≈ 14.85:1 ✓
