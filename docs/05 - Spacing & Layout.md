# Spacing & Layout

---

## Spacing Scale

The spacing scale mirrors Tailwind CSS exactly, making it easy to migrate from Tailwind utilities to Dotify components. The token for `0.5` (2px) uses a hyphen: `--dotify-spacing-0-5`.

| Step | Token | Value |
|------|-------|-------|
| 0 | `--dotify-spacing-0` | 0px |
| px | `--dotify-spacing-px` | 1px |
| 0.5 | `--dotify-spacing-0-5` | 2px |
| 1 | `--dotify-spacing-1` | 4px |
| 1.5 | `--dotify-spacing-1-5` | 6px |
| 2 | `--dotify-spacing-2` | 8px |
| 2.5 | `--dotify-spacing-2-5` | 10px |
| 3 | `--dotify-spacing-3` | 12px |
| 3.5 | `--dotify-spacing-3-5` | 14px |
| 4 | `--dotify-spacing-4` | 16px |
| 5 | `--dotify-spacing-5` | 20px |
| 6 | `--dotify-spacing-6` | 24px |
| 7 | `--dotify-spacing-7` | 28px |
| 8 | `--dotify-spacing-8` | 32px |
| 9 | `--dotify-spacing-9` | 36px |
| 10 | `--dotify-spacing-10` | 40px |
| 12 | `--dotify-spacing-12` | 48px |
| 16 | `--dotify-spacing-16` | 64px |
| 20 | `--dotify-spacing-20` | 80px |
| 24 | `--dotify-spacing-24` | 96px |
| 32 | `--dotify-spacing-32` | 128px |
| 40 | `--dotify-spacing-40` | 160px |
| 48 | `--dotify-spacing-48` | 192px |
| 64 | `--dotify-spacing-64` | 256px |
| 96 | `--dotify-spacing-96` | 384px |

---

## Spacing Utilities

### Padding

```html
<div class="dotify-p-4">All sides 16px</div>
<div class="dotify-px-6">Horizontal 24px</div>
<div class="dotify-py-3">Vertical 12px</div>
<div class="dotify-pt-8">Top 32px</div>
<div class="dotify-pr-4">Right 16px</div>
<div class="dotify-pb-4">Bottom 16px</div>
<div class="dotify-pl-4">Left 16px</div>
```

### Margin

```html
<div class="dotify-m-4">All sides 16px</div>
<div class="dotify-mx-auto">Horizontal auto (centred)</div>
<div class="dotify-my-6">Vertical 24px</div>
<div class="dotify-mt-8">Top 32px</div>
<div class="dotify-mr-4">Right 16px</div>
<div class="dotify-mb-4">Bottom 16px</div>
<div class="dotify-ml-4">Left 16px</div>
```

### Gap (for Flex/Grid)

```html
<div class="dotify-flex dotify-gap-4">…</div>
<div class="dotify-flex dotify-gap-x-6 dotify-gap-y-2">…</div>
```

### Space Between (stacked children)

```html
<div class="dotify-space-y-4">
  <p>First paragraph</p>
  <p>Second paragraph — 16px below first</p>
</div>
```

---

## Container

`.dotify-container` centres content with responsive max-widths and horizontal padding:

| Breakpoint | Max width |
|-----------|----------|
| Default | 100% |
| sm (640px+) | 640px |
| md (768px+) | 768px |
| lg (1024px+) | 1024px |
| xl (1280px+) | 1280px |
| 2xl (1536px+) | 1536px |

```html
<div class="dotify-container dotify-py-12">
  Page content
</div>
```

---

## Display Utilities

```html
<div class="dotify-block">Block</div>
<span class="dotify-inline">Inline</span>
<div class="dotify-inline-block">Inline block</div>
<div class="dotify-hidden">Hidden (display: none)</div>
<div class="dotify-flex">Flex container</div>
<div class="dotify-inline-flex">Inline flex</div>
<div class="dotify-grid">Grid container</div>
```

---

## Flexbox Utilities

```html
<!-- Direction -->
<div class="dotify-flex dotify-flex-row">Row (default)</div>
<div class="dotify-flex dotify-flex-col">Column</div>

<!-- Wrapping -->
<div class="dotify-flex dotify-flex-wrap">Wrapping flex</div>
<div class="dotify-flex dotify-flex-nowrap">No wrap</div>

<!-- Align items -->
<div class="dotify-flex dotify-items-start">Align start</div>
<div class="dotify-flex dotify-items-center">Align centre</div>
<div class="dotify-flex dotify-items-end">Align end</div>
<div class="dotify-flex dotify-items-stretch">Stretch</div>
<div class="dotify-flex dotify-items-baseline">Baseline</div>

<!-- Justify content -->
<div class="dotify-flex dotify-justify-start">Justify start</div>
<div class="dotify-flex dotify-justify-center">Justify centre</div>
<div class="dotify-flex dotify-justify-end">Justify end</div>
<div class="dotify-flex dotify-justify-between">Space between</div>

<!-- Flex item sizing -->
<div class="dotify-flex-1">Flex 1 (fills space)</div>
<div class="dotify-flex-auto">Flex auto</div>
<div class="dotify-flex-none">Flex none (no grow/shrink)</div>
```

---

## Grid Utilities

```html
<!-- Grid columns -->
<div class="dotify-grid dotify-grid-cols-3 dotify-gap-6">
  <div>Col 1</div>
  <div>Col 2</div>
  <div>Col 3</div>
</div>

<!-- Column span -->
<div class="dotify-grid dotify-grid-cols-12 dotify-gap-4">
  <div class="dotify-col-span-8">Main content</div>
  <div class="dotify-col-span-4">Sidebar</div>
</div>
```

Available grid columns: `dotify-grid-cols-1` through `dotify-grid-cols-12`  
Available col span: `dotify-col-span-1` through `dotify-col-span-12`

---

## Sizing Utilities

```html
<div class="dotify-w-full">Full width</div>
<div class="dotify-h-full">Full height</div>
<div class="dotify-w-screen">100vw</div>
<div class="dotify-h-screen">100vh</div>
```

### Max-width Utilities

```html
<div class="dotify-max-w-sm">384px</div>
<div class="dotify-max-w-md">448px</div>
<div class="dotify-max-w-lg">512px</div>
<div class="dotify-max-w-xl">576px</div>
<div class="dotify-max-w-2xl">672px</div>
<div class="dotify-max-w-3xl">768px</div>
<div class="dotify-max-w-4xl">896px</div>
<div class="dotify-max-w-5xl">1024px</div>
<div class="dotify-max-w-6xl">1152px</div>
<div class="dotify-max-w-7xl">1280px</div>
<div class="dotify-max-w-full">100%</div>
<div class="dotify-max-w-none">none</div>
```

---

## Position Utilities

```html
<div class="dotify-relative">Relative</div>
<div class="dotify-absolute">Absolute</div>
<div class="dotify-fixed">Fixed</div>
<div class="dotify-sticky">Sticky</div>
```

Z-index: `dotify-z-10`, `dotify-z-20`, `dotify-z-30`, `dotify-z-40`, `dotify-z-50`

---

## Overflow Utilities

```html
<div class="dotify-overflow-hidden">No overflow</div>
<div class="dotify-overflow-auto">Scroll if needed</div>
<div class="dotify-overflow-x-auto">Horizontal scroll</div>
<div class="dotify-overflow-y-auto">Vertical scroll</div>
```

---

## Accessibility: Screen Reader Only

```html
<span class="dotify-sr-only">Visually hidden but readable by screen readers</span>
```
