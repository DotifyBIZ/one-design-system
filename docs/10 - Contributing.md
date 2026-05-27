# Contributing

Thank you for contributing to the Dotify One Design System. This guide covers how to add new tokens, create new components, update existing styles, and prepare changes for review.

---

## Repository Structure

```
public/
  css/
    index.css              ← Entry point — import list only
    tokens/                ← Design tokens (one file per category)
    base/                  ← Reset + base element styles
    utilities/             ← Utility classes
    components/            ← Component styles (one file per component)
  icons/
    heroicons-sprite.svg   ← SVG sprite
docs/                      ← Documentation (Markdown)
public/llms.md             ← AI reference doc
README.md
```

---

## Setup

No build tools required. The design system is plain CSS. Open any file in a text editor and link the stylesheet to an HTML file for live preview.

For local development:
```bash
# Serve the public directory with any static server
npx serve public
# or
python -m http.server -d public 3000
```

Then open `http://localhost:3000` and create a test HTML file that links:
```html
<link rel="stylesheet" href="/css/index.css">
```

---

## Adding a Design Token

1. Identify which token file the new token belongs to:
   - Colours → `public/css/tokens/colors.css`
   - Typography → `public/css/tokens/typography.css`
   - Spacing → `public/css/tokens/spacing.css`
   - etc.

2. Follow the naming convention: `--dotify-{category}-{property}`

3. If adding a **primitive** colour token: add it to the relevant scale section in `colors.css`

4. If adding a **semantic** token: add it to the `:root {}` block and add the corresponding dark mode override in both `@media (prefers-color-scheme: dark)` and `.dark {}` blocks

5. Update `docs/04 - Design Tokens.md` with the new token

6. Update `public/llms.md` with the new token

**Example — adding a new semantic token:**
```css
/* In :root {} */
--dotify-color-info: var(--dotify-blue-600);

/* In @media (prefers-color-scheme: dark) and .dark {} */
--dotify-color-info: var(--dotify-blue-400);
```

---

## Adding a New Component

1. Create a new file: `public/css/components/{component-name}.css`

2. Follow this file structure:
   ```css
   /* ============================================================
      Dotify One Design Kit — {Component Name}
      https://repo.dotify.biz/one/design-system/css/components/{name}.css

      HTML usage:
        <div class="dotify-{name}">…</div>
   ============================================================ */

   /* Base styles */
   .dotify-{name} { … }

   /* Elements */
   .dotify-{name}__element { … }

   /* Modifiers */
   .dotify-{name}--modifier { … }

   /* ---- Dark mode ---- */
   @media (prefers-color-scheme: dark) { … }
   .dark … { … }
   ```

3. Follow these conventions:
   - All classes prefixed `.dotify-`
   - BEM naming: `.dotify-block__element--modifier`
   - Use only semantic tokens (never `--dotify-red-600` directly)
   - Use `var(--dotify-radius)` for border radius (= 15px)
   - Include both `@media (prefers-color-scheme: dark)` AND `.dark` class overrides
   - Use `var(--dotify-color-focus-ring)` for focus styles on `:focus-visible`
   - No hardcoded hex, rgb, or magic numbers
   - Respect `prefers-reduced-motion` for animations/transitions

4. Add the `@import` to `public/css/index.css` in the components section

5. Document the component in `docs/06 - Components.md`

6. Add the component to `public/llms.md`

---

## Modifying Existing Tokens

When changing an existing token value:
- Check all components that reference it (search for the token name)
- Update the dark mode value if needed
- Verify WCAG contrast ratios if it's a colour token
- Update relevant docs

---

## Naming Conventions

| Thing | Pattern | Example |
|-------|---------|---------|
| CSS custom property | `--dotify-{category}-{property}` | `--dotify-color-primary` |
| Component block | `.dotify-{name}` | `.dotify-card` |
| Component element | `.dotify-{name}__{element}` | `.dotify-card__body` |
| Component modifier | `.dotify-{name}--{modifier}` | `.dotify-card--interactive` |
| Utility class | `.dotify-{property}-{value}` | `.dotify-text-sm` |

---

## PR Checklist

Before opening a pull request:

### Design Tokens
- [ ] Token follows `--dotify-{category}-{property}` naming
- [ ] Primitive token added to correct scale section
- [ ] Semantic token added to `:root {}` block
- [ ] Dark mode override added to both `@media` and `.dark` selectors
- [ ] `docs/04 - Design Tokens.md` updated
- [ ] `public/llms.md` updated

### New Component
- [ ] File created at `public/css/components/{name}.css`
- [ ] Header comment block included (name + URL + HTML usage example)
- [ ] All classes prefixed `.dotify-`
- [ ] BEM naming used consistently
- [ ] Only semantic tokens used (no primitives)
- [ ] `var(--dotify-radius)` used for border radius
- [ ] Dark mode: both `@media` and `.dark` blocks present
- [ ] Focus styles using `var(--dotify-color-focus-ring)` on `:focus-visible`
- [ ] `prefers-reduced-motion` respected for animations
- [ ] `@import` added to `public/css/index.css`
- [ ] Documented in `docs/06 - Components.md`
- [ ] Added to `public/llms.md`

### General
- [ ] No hardcoded hex/rgb values in component files
- [ ] WCAG 2.1 AA contrast verified for new colour combinations
- [ ] Tested in light mode and dark mode
- [ ] Tested with keyboard navigation
- [ ] No regressions in existing components (visual review)
- [ ] `README.md` updated if public API changed

---

## Style Guide for CSS Files

```css
/* ---- Section header ---- */
.dotify-component {
  /* group by: box model → typography → visual → transitions */
  display: flex;
  align-items: center;
  padding: var(--dotify-spacing-4);

  font-family: var(--dotify-font-body);
  font-size: var(--dotify-text-sm);

  background-color: var(--dotify-color-surface-raised);
  border: 1px solid var(--dotify-color-border);
  border-radius: var(--dotify-radius);

  transition: background-color 150ms ease;
}
```

- 2-space indentation
- One blank line between rule blocks
- Comments for each logical section
- Keep specificity low — use single class selectors where possible
