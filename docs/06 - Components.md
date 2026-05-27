# Components

The design system includes 21 pre-built components. All component classes are prefixed `.dotify-` and follow BEM naming (`.dotify-block__element--modifier`).

---

## Button

```html
<!-- Variants -->
<button class="dotify-btn dotify-btn--primary">Primary</button>
<button class="dotify-btn dotify-btn--secondary">Secondary (Indigo)</button>
<button class="dotify-btn dotify-btn--ghost">Ghost</button>
<button class="dotify-btn dotify-btn--danger">Danger</button>
<button class="dotify-btn dotify-btn--link">Link</button>

<!-- Sizes -->
<button class="dotify-btn dotify-btn--primary dotify-btn--sm">Small</button>
<button class="dotify-btn dotify-btn--primary">Default (md)</button>
<button class="dotify-btn dotify-btn--primary dotify-btn--lg">Large</button>

<!-- Modifiers -->
<button class="dotify-btn dotify-btn--primary dotify-btn--block">Full width</button>
<button class="dotify-btn dotify-btn--ghost dotify-btn--icon" aria-label="Settings">
  <svg class="dotify-icon" aria-hidden="true"><use href="…#cog-6-tooth"/></svg>
</button>

<!-- States -->
<button class="dotify-btn dotify-btn--primary" disabled>Disabled</button>
```

---

## Badge

```html
<!-- Tinted (default) -->
<span class="dotify-badge dotify-badge--primary">Primary</span>
<span class="dotify-badge dotify-badge--secondary">Secondary</span>
<span class="dotify-badge dotify-badge--success">Success</span>
<span class="dotify-badge dotify-badge--error">Error</span>
<span class="dotify-badge dotify-badge--warning">Warning</span>
<span class="dotify-badge dotify-badge--gray">Gray</span>

<!-- Filled -->
<span class="dotify-badge dotify-badge--primary-filled">Primary Filled</span>

<!-- Pill modifier -->
<span class="dotify-badge dotify-badge--success dotify-badge--pill">Active</span>

<!-- Sizes -->
<span class="dotify-badge dotify-badge--primary dotify-badge--sm">Small</span>
<span class="dotify-badge dotify-badge--primary dotify-badge--lg">Large</span>
```

---

## Input / Field

```html
<div class="dotify-field">
  <label class="dotify-label" for="email">
    Email <span class="dotify-label--required">*</span>
  </label>
  <input type="email" id="email" class="dotify-input" placeholder="you@example.com" required>
  <p class="dotify-field__hint">We'll never share your email.</p>
</div>

<!-- Invalid state -->
<div class="dotify-field">
  <label class="dotify-label" for="username">Username</label>
  <input type="text" id="username" class="dotify-input dotify-input--invalid" aria-invalid="true" aria-describedby="username-error">
  <p class="dotify-field__error" id="username-error">Username is already taken.</p>
</div>

<!-- With icon -->
<div class="dotify-field">
  <label class="dotify-label" for="search">Search</label>
  <div class="dotify-input-group">
    <span class="dotify-input-group__icon">
      <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#magnifying-glass"/></svg>
    </span>
    <input type="search" id="search" class="dotify-input dotify-input-group__input">
  </div>
</div>
```

---

## Textarea

```html
<div class="dotify-field">
  <label class="dotify-label" for="bio">Bio</label>
  <textarea id="bio" class="dotify-textarea" rows="4" placeholder="Tell us about yourself…"></textarea>
</div>

<!-- No resize -->
<textarea class="dotify-textarea dotify-textarea--no-resize" rows="3"></textarea>
```

---

## Select

```html
<div class="dotify-field">
  <label class="dotify-label" for="country">Country</label>
  <div class="dotify-select-wrapper">
    <select id="country" class="dotify-select">
      <option value="">Choose a country…</option>
      <option value="au">Australia</option>
      <option value="nz">New Zealand</option>
    </select>
  </div>
</div>
```

---

## Checkbox

```html
<label class="dotify-checkbox">
  <input type="checkbox" class="dotify-checkbox__input">
  <span class="dotify-checkbox__label">Accept terms and conditions</span>
</label>

<!-- Checked & disabled -->
<label class="dotify-checkbox dotify-checkbox--disabled">
  <input type="checkbox" class="dotify-checkbox__input" checked disabled>
  <span class="dotify-checkbox__label">Pre-selected (disabled)</span>
</label>
```

---

## Radio

```html
<fieldset class="dotify-radio-group">
  <legend class="dotify-label">Billing cycle</legend>
  <label class="dotify-radio">
    <input type="radio" class="dotify-radio__input" name="billing" value="monthly">
    <span class="dotify-radio__label">Monthly</span>
  </label>
  <label class="dotify-radio">
    <input type="radio" class="dotify-radio__input" name="billing" value="annual" checked>
    <span class="dotify-radio__label">Annual <span class="dotify-badge dotify-badge--success dotify-badge--sm">Save 20%</span></span>
  </label>
</fieldset>

<!-- Inline -->
<fieldset class="dotify-radio-group dotify-radio-group--inline">…</fieldset>
```

---

## Toggle

```html
<label class="dotify-toggle">
  <input type="checkbox" class="dotify-toggle__input" role="switch">
  <span class="dotify-toggle__track" aria-hidden="true"></span>
  <span class="dotify-toggle__label">Enable notifications</span>
</label>

<!-- Sizes -->
<label class="dotify-toggle dotify-toggle--sm">…</label>
<label class="dotify-toggle dotify-toggle--lg">…</label>
```

---

## Alert

```html
<div class="dotify-alert dotify-alert--success" role="alert">
  <svg class="dotify-alert__icon dotify-icon" aria-hidden="true"><use href="…#check-circle"/></svg>
  <div class="dotify-alert__content">
    <p class="dotify-alert__title">Changes saved</p>
    <p class="dotify-alert__body">Your profile has been updated successfully.</p>
  </div>
  <button class="dotify-alert__dismiss" aria-label="Dismiss">
    <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#x-mark"/></svg>
  </button>
</div>

<!-- Variants -->
<div class="dotify-alert dotify-alert--error" role="alert">…</div>
<div class="dotify-alert dotify-alert--warning" role="alert">…</div>

<!-- Full-width banner -->
<div class="dotify-alert dotify-alert--warning dotify-alert--banner" role="alert">…</div>
```

---

## Card

```html
<div class="dotify-card">
  <div class="dotify-card__header">
    <h3 class="dotify-card__title">Card Title</h3>
    <p class="dotify-card__subtitle">Optional subtitle</p>
  </div>
  <div class="dotify-card__body">
    <p>Card content goes here.</p>
  </div>
  <div class="dotify-card__footer">
    <button class="dotify-btn dotify-btn--ghost dotify-btn--sm">Cancel</button>
    <button class="dotify-btn dotify-btn--primary dotify-btn--sm">Save</button>
  </div>
</div>

<!-- Interactive (clickable card) -->
<a href="/product/1" class="dotify-card dotify-card--interactive">
  <div class="dotify-card__body">Click me</div>
</a>

<!-- Flat / Elevated -->
<div class="dotify-card dotify-card--flat">…</div>
<div class="dotify-card dotify-card--elevated">…</div>
```

---

## Modal

```html
<!-- Trigger -->
<button class="dotify-btn dotify-btn--primary" onclick="document.getElementById('my-modal').classList.add('dotify-modal--open')">
  Open modal
</button>

<!-- Modal -->
<div class="dotify-modal" id="my-modal" role="dialog" aria-modal="true" aria-labelledby="modal-title">
  <div class="dotify-modal__overlay" onclick="this.parentElement.classList.remove('dotify-modal--open')"></div>
  <div class="dotify-modal__panel">
    <div class="dotify-modal__header">
      <h2 class="dotify-modal__title" id="modal-title">Confirm action</h2>
      <button class="dotify-modal__close" aria-label="Close"
        onclick="document.getElementById('my-modal').classList.remove('dotify-modal--open')">
        <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#x-mark"/></svg>
      </button>
    </div>
    <div class="dotify-modal__body">
      <p>Are you sure you want to continue?</p>
    </div>
    <div class="dotify-modal__footer">
      <button class="dotify-btn dotify-btn--ghost">Cancel</button>
      <button class="dotify-btn dotify-btn--primary">Confirm</button>
    </div>
  </div>
</div>

<!-- Sizes: dotify-modal--sm, dotify-modal--lg, dotify-modal--xl, dotify-modal--full -->
```

---

## Dropdown

```html
<div class="dotify-dropdown" id="actions-dropdown">
  <button class="dotify-btn dotify-btn--ghost"
    onclick="this.closest('.dotify-dropdown').classList.toggle('dotify-dropdown--open')"
    aria-haspopup="true">
    Actions
    <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#chevron-down"/></svg>
  </button>
  <div class="dotify-dropdown__menu" role="menu">
    <span class="dotify-dropdown__label">File</span>
    <a class="dotify-dropdown__item" href="#" role="menuitem">
      <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#pencil"/></svg>
      Edit
    </a>
    <a class="dotify-dropdown__item" href="#" role="menuitem">Duplicate</a>
    <div class="dotify-dropdown__divider"></div>
    <button class="dotify-dropdown__item dotify-dropdown__item--danger" role="menuitem">
      <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#trash"/></svg>
      Delete
    </button>
  </div>
</div>

<!-- Align right: dotify-dropdown--right -->
<!-- Open upward: dotify-dropdown--up -->
```

---

## Navbar

```html
<header class="dotify-navbar">
  <div class="dotify-container dotify-navbar__inner">
    <a href="/" class="dotify-navbar__brand">
      <img src="/logo.svg" alt="My App" height="28">
    </a>
    <nav class="dotify-navbar__nav" aria-label="Main navigation">
      <a href="/"        class="dotify-navbar__link dotify-navbar__link--active">Dashboard</a>
      <a href="/reports" class="dotify-navbar__link">Reports</a>
      <a href="/settings"class="dotify-navbar__link">Settings</a>
    </nav>
    <div class="dotify-navbar__actions">
      <button class="dotify-btn dotify-btn--ghost dotify-btn--sm">Log out</button>
    </div>
    <button class="dotify-navbar__mobile-toggle" aria-expanded="false" aria-label="Open menu">
      <svg class="dotify-icon" aria-hidden="true"><use href="…#bars-3"/></svg>
    </button>
  </div>
  <nav class="dotify-navbar__mobile-menu" id="mobile-menu">
    <a href="/" class="dotify-navbar__link">Dashboard</a>
  </nav>
</header>
```

---

## Sidebar

```html
<aside class="dotify-sidebar">
  <nav class="dotify-sidebar__nav" aria-label="Sidebar navigation">
    <div class="dotify-sidebar__section">
      <p class="dotify-sidebar__section-label">Main</p>
      <a href="/dashboard" class="dotify-sidebar__link dotify-sidebar__link--active">
        <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#home"/></svg>
        Dashboard
      </a>
      <a href="/users" class="dotify-sidebar__link">
        <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#users"/></svg>
        Users
      </a>
    </div>
    <div class="dotify-sidebar__divider"></div>
    <div class="dotify-sidebar__section">
      <a href="/settings" class="dotify-sidebar__link">
        <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#cog-6-tooth"/></svg>
        Settings
      </a>
    </div>
  </nav>
  <div class="dotify-sidebar__footer">
    <span class="dotify-avatar dotify-avatar--sm"><span class="dotify-avatar__initials">AJ</span></span>
    <span class="dotify-text-sm dotify-font-semibold">Alice Jones</span>
  </div>
</aside>
```

---

## Table

```html
<div class="dotify-table-wrapper">
  <table class="dotify-table dotify-table--striped dotify-table--hover-rows">
    <thead>
      <tr>
        <th>Name</th>
        <th>Email</th>
        <th>Role</th>
        <th>Status</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Alice Jones</td>
        <td>alice@example.com</td>
        <td>Admin</td>
        <td><span class="dotify-badge dotify-badge--success-filled dotify-badge--pill">Active</span></td>
      </tr>
      <tr>
        <td>Bob Smith</td>
        <td>bob@example.com</td>
        <td>User</td>
        <td><span class="dotify-badge dotify-badge--gray dotify-badge--pill">Inactive</span></td>
      </tr>
    </tbody>
  </table>
</div>

<!-- Modifiers: --striped, --bordered, --hover-rows, --compact -->
```

---

## Tabs

```html
<div class="dotify-tabs">
  <div class="dotify-tabs__list" role="tablist" aria-label="Account sections">
    <button class="dotify-tabs__tab dotify-tabs__tab--active"
      role="tab" id="tab-profile" aria-selected="true" aria-controls="panel-profile">
      Profile
    </button>
    <button class="dotify-tabs__tab"
      role="tab" id="tab-billing" aria-selected="false" aria-controls="panel-billing">
      Billing
      <span class="dotify-tabs__tab__count">3</span>
    </button>
    <button class="dotify-tabs__tab"
      role="tab" id="tab-notifications" aria-selected="false" aria-controls="panel-notifications" disabled>
      Notifications
    </button>
  </div>
  <div id="panel-profile" class="dotify-tabs__panel" role="tabpanel" aria-labelledby="tab-profile">
    Profile content
  </div>
  <div id="panel-billing" class="dotify-tabs__panel" role="tabpanel" aria-labelledby="tab-billing" hidden>
    Billing content
  </div>
</div>

<!-- Pills variant -->
<div class="dotify-tabs dotify-tabs--pills">…</div>
```

---

## Tooltip

```html
<span class="dotify-tooltip-wrapper">
  <button class="dotify-btn dotify-btn--ghost dotify-btn--sm" aria-describedby="tip-delete">
    <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#trash"/></svg>
  </button>
  <span class="dotify-tooltip dotify-tooltip--top" id="tip-delete" role="tooltip">Delete item</span>
</span>

<!-- Positions: --top (default), --bottom, --left, --right -->
```

---

## Spinner

```html
<span class="dotify-spinner" role="status" aria-label="Loading…"></span>

<!-- Sizes -->
<span class="dotify-spinner dotify-spinner--sm"></span>
<span class="dotify-spinner dotify-spinner--lg"></span>
<span class="dotify-spinner dotify-spinner--xl"></span>

<!-- Colours -->
<span class="dotify-spinner dotify-spinner--primary"></span>
<span class="dotify-spinner dotify-spinner--white"></span>   <!-- on dark backgrounds -->

<!-- Inside a button -->
<button class="dotify-btn dotify-btn--primary" disabled>
  <span class="dotify-spinner dotify-spinner--sm dotify-spinner--white" aria-hidden="true"></span>
  Saving…
</button>
```

---

## Avatar

```html
<!-- Image -->
<span class="dotify-avatar dotify-avatar--lg">
  <img class="dotify-avatar__image" src="/photos/alice.jpg" alt="Alice Jones">
</span>

<!-- Initials -->
<span class="dotify-avatar dotify-avatar--md">
  <span class="dotify-avatar__initials" aria-label="Alice Jones">AJ</span>
</span>

<!-- With status -->
<span class="dotify-avatar dotify-avatar--md">
  <img class="dotify-avatar__image" src="/photos/alice.jpg" alt="Alice Jones">
  <span class="dotify-avatar__status dotify-avatar__status--online" aria-label="Online"></span>
</span>

<!-- Sizes: --xs --sm (default md) --lg --xl --2xl -->
<!-- Colours: --red --blue --green --gray -->
<!-- Status: --online --away --busy --offline -->

<!-- Group -->
<div class="dotify-avatar-group">
  <span class="dotify-avatar dotify-avatar--sm"><span class="dotify-avatar__initials">AJ</span></span>
  <span class="dotify-avatar dotify-avatar--sm"><span class="dotify-avatar__initials">BS</span></span>
  <span class="dotify-avatar dotify-avatar--sm dotify-avatar--gray"><span class="dotify-avatar__initials">+3</span></span>
</div>
```

---

## Breadcrumb

```html
<nav class="dotify-breadcrumb" aria-label="Breadcrumb">
  <ol class="dotify-breadcrumb__list">
    <li class="dotify-breadcrumb__item">
      <a href="/" class="dotify-breadcrumb__link">Home</a>
    </li>
    <li class="dotify-breadcrumb__item" aria-hidden="true">
      <span class="dotify-breadcrumb__separator"></span>
    </li>
    <li class="dotify-breadcrumb__item">
      <a href="/products" class="dotify-breadcrumb__link">Products</a>
    </li>
    <li class="dotify-breadcrumb__item" aria-hidden="true">
      <span class="dotify-breadcrumb__separator"></span>
    </li>
    <li class="dotify-breadcrumb__item">
      <span class="dotify-breadcrumb__current" aria-current="page">Widget Pro</span>
    </li>
  </ol>
</nav>

<!-- Slash variant -->
<nav class="dotify-breadcrumb dotify-breadcrumb--slash">…</nav>
```

---

## Pagination

```html
<nav class="dotify-pagination" aria-label="Pagination">
  <a href="/page/1" class="dotify-pagination__prev" aria-label="Previous page">
    <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#chevron-left"/></svg>
    Previous
  </a>
  <ol class="dotify-pagination__list">
    <li><a href="/page/1" class="dotify-pagination__link">1</a></li>
    <li><a href="/page/2" class="dotify-pagination__link dotify-pagination__link--active" aria-current="page">2</a></li>
    <li><a href="/page/3" class="dotify-pagination__link">3</a></li>
    <li><span class="dotify-pagination__ellipsis" aria-hidden="true">…</span></li>
    <li><a href="/page/10" class="dotify-pagination__link">10</a></li>
  </ol>
  <a href="/page/3" class="dotify-pagination__next" aria-label="Next page">
    Next
    <svg class="dotify-icon dotify-icon--sm" aria-hidden="true"><use href="…#chevron-right"/></svg>
  </a>
</nav>

<!-- Disabled -->
<span class="dotify-pagination__prev dotify-pagination__prev--disabled" aria-disabled="true">← Prev</span>

<!-- Compact -->
<nav class="dotify-pagination dotify-pagination--compact">…</nav>
```
