# CSS Organization Cheatsheet

---

## 1. CSS File Structure

* **Reset / Normalize** – Normalize browser styles.
* **Variables / Constants** – CSS custom properties for colors, fonts, spacing.
* **Base / Global Styles** – Body, headings, links, default typography.
* **Layout / Grid** – Container, grid, flex layouts.
* **Components / UI** – Buttons, cards, modals, forms.
* **Utilities / Helpers** – Margin, padding, display, text alignment helpers.
* **Responsive / Media Queries** – Mobile-first breakpoints.
* **Animations / Transitions** – Keyframes and reusable animations.
* **Theme / Dark Mode** – Light/dark themes using variables or classes.
* **Overrides / Hacks** – Temporary fixes (keep isolated + documented).

---

## 2. Naming Conventions

### BEM (Block Element Modifier)

```css
.block { }
.block__element { }
.block--modifier { }
```

### Utility-First (Optional)

```css
.mt-1 { margin-top: 4px; }
.text-center { text-align: center; }
.flex { display: flex; }
```

### State Classes

```css
.is-active { }
.is-hidden { }
.is-disabled { }
```

---

## 3. CSS Variables (Custom Properties)

```css
:root {
  --color-primary: #4f46e5;
  --color-secondary: #9333ea;
  --font-main: 'Inter', sans-serif;
  --spacing-sm: 8px;
  --spacing-md: 16px;
}
```

Usage:

```css
button {
  background: var(--color-primary);
  padding: var(--spacing-md);
}
```

---

## 4. Mobile-First Media Queries

```css
/* Base (mobile) */
.container {
  padding: 1rem;
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    padding: 2rem;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  .container {
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

---

## 5. Common Layout Patterns

### Flexbox Centering

```css
.center {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### Grid Layout

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}
```

---

## 6. Component Structure Example

```css
.card {
  padding: 1rem;
  border-radius: 8px;
  background: white;
}

.card__title {
  font-size: 1.25rem;
}

.card--highlight {
  border: 2px solid var(--color-primary);
}
```

---

## 7. Z-Index Scale (Keep It Consistent)

```css
:root {
  --z-base: 1;
  --z-dropdown: 100;
  --z-modal: 1000;
  --z-toast: 1100;
}
```

---

## 8. Transitions & Animations

```css
.button {
  transition: background 0.3s ease;
}

@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

---

## 9. Best Practices

* Keep specificity **low** (avoid deep nesting).
* Avoid `!important` unless absolutely necessary.
* Group related styles together.
* Use **consistent spacing scale**.
* Prefer **classes over IDs**.
* Limit nesting (especially in preprocessors like SCSS).
* Comment tricky or temporary code.

---

## 10. Folder Structure Example

```
/css
  ├── base/
  ├── components/
  ├── layout/
  ├── utilities/
  ├── themes/
  └── main.css
```

---

## 11. Debugging Tips

* Use `outline: 1px solid red;` for layout debugging.
* Temporarily add:

```css
* {
  outline: 1px solid rgba(255,0,0,0.2);
}
```
---
