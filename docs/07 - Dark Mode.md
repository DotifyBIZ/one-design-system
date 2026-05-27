# Dark Mode

The design system provides first-class dark mode support using two complementary methods. Both work simultaneously — you can support both system-level and user-toggled dark mode with no extra effort.

---

## Method 1 — System Preference (Automatic)

Dark mode activates automatically when the user's OS is set to dark mode:

```css
@media (prefers-color-scheme: dark) {
  /* semantic tokens are overridden here */
}
```

No configuration needed. Any page using the design system CDN link automatically respects the user's OS preference.

---

## Method 2 — Manual Toggle (`.dark` class)

Add `class="dark"` to the `<html>` element to force dark mode regardless of OS preference:

```html
<html lang="en" class="dark">
```

This enables user-controlled dark mode switches in your application.

---

## JavaScript Toggle Snippet

```html
<!-- Toggle button -->
<button id="theme-toggle" aria-label="Toggle dark mode">
  <svg class="dotify-icon" id="icon-sun" aria-hidden="true"><use href="…#sun"/></svg>
  <svg class="dotify-icon dotify-hidden" id="icon-moon" aria-hidden="true"><use href="…#moon"/></svg>
</button>

<script>
  const html = document.documentElement;
  const toggle = document.getElementById('theme-toggle');
  const iconSun = document.getElementById('icon-sun');
  const iconMoon = document.getElementById('icon-moon');

  // Load saved preference
  const savedTheme = localStorage.getItem('theme');
  if (savedTheme === 'dark' || (!savedTheme && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    html.classList.add('dark');
    iconSun.classList.add('dotify-hidden');
    iconMoon.classList.remove('dotify-hidden');
  }

  toggle.addEventListener('click', () => {
    const isDark = html.classList.toggle('dark');
    localStorage.setItem('theme', isDark ? 'dark' : 'light');
    iconSun.classList.toggle('dotify-hidden', isDark);
    iconMoon.classList.toggle('dotify-hidden', !isDark);
  });
</script>
```

---

## How It Works Internally

Dark mode overrides only the **semantic token** layer. Primitive colour scales stay fixed. Components automatically adapt because they reference semantic tokens.

```css
/* Light (default) */
:root {
  --dotify-color-surface: #ffffff;
  --dotify-color-on-surface: var(--dotify-gray-900);
  --dotify-color-secondary: var(--dotify-indigo-600);
}

/* Dark — system preference */
@media (prefers-color-scheme: dark) {
  :root {
    --dotify-color-surface: var(--dotify-gray-900);
    --dotify-color-on-surface: var(--dotify-gray-50);
    --dotify-color-secondary: var(--dotify-indigo-400);
  }
}

/* Dark — manual class */
.dark {
  --dotify-color-surface: var(--dotify-gray-900);
  --dotify-color-on-surface: var(--dotify-gray-50);
  --dotify-color-secondary: var(--dotify-indigo-400);
}
```

---

## Dark Mode Token Overrides

| Semantic Token | Light | Dark |
|---------------|-------|------|
| `--dotify-color-surface` | `#ffffff` | gray-900 |
| `--dotify-color-surface-raised` | `#ffffff` | gray-800 |
| `--dotify-color-surface-inset` | gray-50 | gray-850 |
| `--dotify-color-on-surface` | gray-900 | gray-50 |
| `--dotify-color-on-surface-muted` | gray-600 | gray-400 |
| `--dotify-color-border` | gray-200 | gray-700 |
| `--dotify-color-border-strong` | gray-400 | gray-600 |
| `--dotify-color-secondary` | indigo-600 | indigo-400 |
| `--dotify-color-primary` | red-600 | red-500 |
| `--dotify-color-focus-ring` | indigo-600 | indigo-300 |
| `--dotify-color-success` | green-600 | green-400 |
| `--dotify-color-error` | error-600 | error-400 |
| `--dotify-color-warning` | yellow-500 | yellow-400 |

---

## Writing Dark-Mode-Compatible Custom CSS

Always use semantic tokens in your custom styles:

```css
/* ✅ Good — adapts automatically to dark mode */
.my-widget {
  background-color: var(--dotify-color-surface-raised);
  color: var(--dotify-color-on-surface);
  border: 1px solid var(--dotify-color-border);
}

/* ❌ Avoid — hardcoded, won't adapt */
.my-widget {
  background-color: #ffffff;
  color: #111827;
  border: 1px solid #e5e7eb;
}
```

If you need component-specific dark overrides, mirror both selectors:

```css
@media (prefers-color-scheme: dark) {
  .my-widget { background-color: var(--dotify-gray-800); }
}
.dark .my-widget { background-color: var(--dotify-gray-800); }
```

---

## Testing Dark Mode

- **Chrome DevTools**: Rendering tab → Emulate CSS media feature `prefers-color-scheme`
- **Firefox**: DevTools → Inspector → Toggle dark mode
- **macOS**: System Preferences → General → Appearance
- **Windows**: Settings → Personalisation → Colours → Dark
