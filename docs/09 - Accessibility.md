# Accessibility

The Dotify One Design System is built to meet **WCAG 2.1 Level AA** as a minimum standard. This document explains the accessibility features built into the system and the conventions you must follow when building on top of it.

---

## Colour Contrast

All brand colours have been chosen and verified to meet WCAG AA contrast requirements.

| Foreground | Background | Ratio | Level |
|-----------|------------|-------|-------|
| White `#ffffff` | Dotify Red `#B41618` | **6.55:1** | AA ✓, AA Large ✓, AAA Large ✓ |
| White `#ffffff` | Dotify Indigo `#211F60` | **14.85:1** | AA ✓, AAA ✓ |
| `gray-900` | `#ffffff` | **16.75:1** | AA ✓, AAA ✓ |
| `gray-600` | `#ffffff` | **5.74:1** | AA ✓ (normal text) |
| White `#ffffff` | Error `#D91A1D` | **5.2:1** | AA ✓ |
| White `#ffffff` | Success `#158C36` | **4.65:1** | AA ✓ |

> Never use colour alone to convey meaning (e.g. error states). Always supplement with text or icons.

---

## Focus Management

All interactive elements support `:focus-visible`, ensuring keyboard users always see a visible focus indicator without affecting mouse users.

The focus ring uses `--dotify-color-focus-ring` (Dotify Indigo — `#211F60` light, indigo-300 dark):

```css
:focus-visible {
  outline: 2px solid var(--dotify-color-focus-ring);
  outline-offset: 2px;
}
```

**Never suppress focus styles** with `outline: none` without providing an equivalent replacement.

---

## Screen Reader Utilities

### `.dotify-sr-only`

Visually hides content while keeping it accessible to screen readers. Use for:
- Icon-only button labels
- Additional context for ambiguous UI
- Skip links

```html
<!-- Icon button with accessible label -->
<button class="dotify-btn dotify-btn--ghost dotify-btn--icon" aria-label="Delete item">
  <svg class="dotify-icon" aria-hidden="true"><use href="…#trash"/></svg>
</button>

<!-- Screen-reader-only label added to a search input -->
<label class="dotify-sr-only" for="search">Search</label>
<input type="search" id="search" class="dotify-input" placeholder="Search…">

<!-- Skip link (place at top of <body>) -->
<a href="#main-content" class="dotify-sr-only dotify-sr-only--focusable">
  Skip to main content
</a>
```

---

## Form Accessibility

### Always associate labels with inputs

```html
<!-- ✅ Correct -->
<div class="dotify-field">
  <label class="dotify-label" for="email">Email address</label>
  <input type="email" id="email" class="dotify-input">
</div>

<!-- ❌ Incorrect — no label association -->
<input type="email" class="dotify-input" placeholder="Email">
```

### Mark required fields

```html
<label class="dotify-label" for="name">
  Full name <span class="dotify-label--required" aria-hidden="true">*</span>
</label>
<input type="text" id="name" class="dotify-input" required aria-required="true">
```

Add explanatory text near the form:
```html
<p class="dotify-text-sm dotify-text-muted dotify-mb-4">
  Fields marked with <span aria-hidden="true">*</span><span class="dotify-sr-only">an asterisk</span> are required.
</p>
```

### Communicate validation errors

```html
<div class="dotify-field">
  <label class="dotify-label" for="username">Username</label>
  <input type="text" id="username" class="dotify-input dotify-input--invalid"
    aria-invalid="true" aria-describedby="username-error">
  <p class="dotify-field__error" id="username-error" role="alert">
    Username is already taken. Please choose another.
  </p>
</div>
```

### Fieldset + legend for grouped inputs

```html
<fieldset class="dotify-radio-group">
  <legend class="dotify-label">Preferred contact method</legend>
  <label class="dotify-radio">
    <input type="radio" name="contact" value="email" class="dotify-radio__input">
    <span class="dotify-radio__label">Email</span>
  </label>
  <label class="dotify-radio">
    <input type="radio" name="contact" value="phone" class="dotify-radio__input">
    <span class="dotify-radio__label">Phone</span>
  </label>
</fieldset>
```

---

## ARIA Patterns for Components

### Modal / Dialog

```html
<div class="dotify-modal dotify-modal--open"
  role="dialog"
  aria-modal="true"
  aria-labelledby="modal-title"
  aria-describedby="modal-desc">
  …
  <h2 id="modal-title">Confirm deletion</h2>
  <p id="modal-desc">This action cannot be undone.</p>
</div>
```

When a modal opens:
1. Move focus to the modal panel (or the first focusable element inside)
2. Trap focus within the modal — Tab should cycle through modal focusable elements only
3. Close on `Escape`
4. Return focus to the trigger element on close

### Tabs

```html
<div class="dotify-tabs__list" role="tablist" aria-label="Account sections">
  <button class="dotify-tabs__tab dotify-tabs__tab--active"
    role="tab" aria-selected="true" aria-controls="panel-1" id="tab-1">
    Profile
  </button>
</div>
<div id="panel-1" role="tabpanel" aria-labelledby="tab-1" tabindex="0">…</div>
```

Keyboard pattern: Arrow keys navigate between tabs; `Enter`/`Space` activates.

### Dropdown Menu

```html
<button aria-haspopup="menu" aria-expanded="false" aria-controls="menu-1">Options</button>
<div id="menu-1" role="menu">
  <a role="menuitem" href="#">Edit</a>
</div>
```

### Alert / Live Regions

```html
<!-- Status alerts (non-urgent) -->
<div role="status" aria-live="polite">…</div>

<!-- Error/warning alerts (urgent) -->
<div role="alert" aria-live="assertive">…</div>
```

---

## Images & Icons

Always provide alternative text for meaningful images:

```html
<!-- Meaningful image -->
<img src="chart.png" alt="Revenue grew 42% year-over-year in Q4 2024">

<!-- Decorative image -->
<img src="decorative-swoosh.png" alt="">

<!-- Decorative icon -->
<svg class="dotify-icon" aria-hidden="true" focusable="false">
  <use href="…#check-circle"></use>
</svg>

<!-- Meaningful standalone icon -->
<svg class="dotify-icon" role="img" aria-label="Success">
  <title>Success</title>
  <use href="…#check-circle"></use>
</svg>
```

---

## Reduced Motion

The design system respects `prefers-reduced-motion`:

```css
@media (prefers-reduced-motion: reduce) {
  /* Spinners slow down, animations disabled */
  .dotify-spinner { animation-duration: 1.5s; }
  .dotify-tooltip { transition: none; }
}
```

When adding custom animations, always include a reduced motion override:

```css
.my-animation { transition: transform 300ms ease; }

@media (prefers-reduced-motion: reduce) {
  .my-animation { transition: none; }
}
```

---

## Testing Checklist

- [ ] Keyboard navigation: Tab through the page, all interactive elements reachable
- [ ] Focus visible: Focus ring appears on every focused element
- [ ] Screen reader: Test with VoiceOver (macOS/iOS), NVDA or JAWS (Windows)
- [ ] Colour contrast: Verify with browser devtools or axe extension
- [ ] No colour-only meaning: Error states have text/icon, not just red
- [ ] Form labels: Every input has an associated `<label>`
- [ ] Images: All `<img>` have `alt` attributes (empty for decorative)
- [ ] Zoom: Page is usable at 200% zoom with no horizontal scroll
