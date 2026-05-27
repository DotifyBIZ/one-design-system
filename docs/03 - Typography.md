# Typography

The design system uses **Montserrat** for both body text and headings, loaded from Google Fonts.

---

## Font Loading

The font is already included via the design system stylesheet — no additional `<link>` tag required:

```css
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&display=swap');
```

Two weights are loaded:
- **400** — body text, labels, UI text
- **600** — headings, buttons, strong emphasis

---

## Font Tokens

| Token | Value |
|-------|-------|
| `--dotify-font-body` | `'Montserrat', ui-sans-serif, system-ui, sans-serif` |
| `--dotify-font-heading` | `'Montserrat', ui-sans-serif, system-ui, sans-serif` |
| `--dotify-font-mono` | `ui-monospace, 'Cascadia Code', 'Source Code Pro', monospace` |
| `--dotify-font-weight-normal` | `400` |
| `--dotify-font-weight-semibold` | `600` |

---

## Type Scale

| Token | Value | Tailwind equivalent |
|-------|-------|---------------------|
| `--dotify-text-xs` | `0.75rem` (12px) | `text-xs` |
| `--dotify-text-sm` | `0.875rem` (14px) | `text-sm` |
| `--dotify-text-base` | `1rem` (16px) | `text-base` |
| `--dotify-text-lg` | `1.125rem` (18px) | `text-lg` |
| `--dotify-text-xl` | `1.25rem` (20px) | `text-xl` |
| `--dotify-text-2xl` | `1.5rem` (24px) | `text-2xl` |
| `--dotify-text-3xl` | `1.875rem` (30px) | `text-3xl` |
| `--dotify-text-4xl` | `2.25rem` (36px) | `text-4xl` |
| `--dotify-text-5xl` | `3rem` (48px) | `text-5xl` |

---

## Line Height Tokens

| Token | Value |
|-------|-------|
| `--dotify-leading-tight` | `1.25` |
| `--dotify-leading-snug` | `1.375` |
| `--dotify-leading-normal` | `1.5` |
| `--dotify-leading-relaxed` | `1.625` |
| `--dotify-leading-loose` | `2` |

---

## Letter Spacing Tokens

| Token | Value |
|-------|-------|
| `--dotify-tracking-tight` | `-0.05em` |
| `--dotify-tracking-normal` | `0` |
| `--dotify-tracking-wide` | `0.025em` |
| `--dotify-tracking-wider` | `0.05em` |
| `--dotify-tracking-widest` | `0.1em` |

---

## Base Heading Styles

Headings use the heading font at semibold weight. The base stylesheet applies these automatically to `h1`–`h6`:

| Element | Token used |
|---------|-----------|
| `h1` | `--dotify-text-5xl` |
| `h2` | `--dotify-text-4xl` |
| `h3` | `--dotify-text-3xl` |
| `h4` | `--dotify-text-2xl` |
| `h5` | `--dotify-text-xl` |
| `h6` | `--dotify-text-lg` |

---

## Typography Utility Classes

### Font Family
```html
<p class="dotify-font-body">Body font</p>
<h2 class="dotify-font-heading">Heading font</h2>
<code class="dotify-font-mono">Monospace</code>
```

### Font Size
```html
<p class="dotify-text-sm">Small text</p>
<p class="dotify-text-base">Base text</p>
<p class="dotify-text-xl">Large text</p>
```

### Font Weight
```html
<p class="dotify-font-normal">Normal weight (400)</p>
<p class="dotify-font-semibold">Semibold weight (600)</p>
```

### Line Height
```html
<p class="dotify-leading-relaxed">Relaxed line height for body copy</p>
<h2 class="dotify-leading-tight">Tight line height for headings</h2>
```

### Text Transform & Decoration
```html
<span class="dotify-uppercase">uppercase</span>
<span class="dotify-capitalize">Capitalize</span>
<span class="dotify-underline">Underlined</span>
<span class="dotify-line-through">Strikethrough</span>
<span class="dotify-no-underline">No underline</span>
```

### Text Overflow
```html
<p class="dotify-truncate">Long text that gets truncated with an ellipsis…</p>
<p class="dotify-whitespace-nowrap">Won't wrap to new line</p>
```

### Prose (Long-form Body Text)
```html
<div class="dotify-prose">
  <p>Article content with comfortable reading width, line height, and spacing.</p>
  <p>Automatically limited to ~65ch width for readability.</p>
</div>
```

---

## Full Typography Example

```html
<article class="dotify-prose">
  <h1>Product Overview</h1>
  <p class="dotify-text-lg dotify-text-muted dotify-leading-relaxed">
    A brief description of the product in slightly larger, relaxed type.
  </p>
  <h2>Key Features</h2>
  <p>
    Body copy uses <strong>Montserrat 400</strong> at 1rem (16px) with a line height of 1.5
    for comfortable reading across all screen sizes.
  </p>
  <p class="dotify-text-xs dotify-text-muted dotify-uppercase dotify-tracking-wider">
    Category Label
  </p>
</article>
```
