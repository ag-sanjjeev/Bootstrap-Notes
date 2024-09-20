## &#10022; Spinners:
Create animated loader and spinners with bootstrap without JavaScript.

*Syntax: For spinners, add `.spinner-border` class.*

```html
<div class="spinner-border" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

- Colored spinners:

*Syntax: add `.text-{primary|secondary|success|warning|danger|info}` class to apply color.*

```html
<div class="spinner-border text-primary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

- Growing spinner:

*Syntax: add `.spinner-grow` class instead of `.spinner-grow` class.*

```html
<!-- Default spinner grow -->
<div class="spinner-grow" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Primary colored spinner grow -->
<div class="spinner-grow text-primary" role="status">
  <span class="visually-hidden">Loading...</span>
</div>
```

- Sizing of spinners:

*Syntax:* 
  - Add `.spinner-border-sm` class to the `.spinner-border` class.
  - Add `.spinner-grow-sm` class to the `.spinner-grow` class.

```html
<!-- Default sized spinner border -->
<div class="spinner-border" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Small sized spinner border -->
<div class="spinner-border" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Custom sized spinner border -->
<div class="spinner-border" role="status" style="width: 3rem; aspect-ratio: 1;">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Default sized spinner grow -->
<div class="spinner-grow" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Small sized spinner grow -->
<div class="spinner-grow-sm" role="status">
  <span class="visually-hidden">Loading...</span>
</div>

<!-- Custom sized spinner grow -->
<div class="spinner-grow" role="status" style="width: 3rem; aspect-ratio: 1;">
  <span class="visually-hidden">Loading...</span>
</div>
```

- Spinners with button:

```html
<!-- Spinner border and button without text -->
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-border" role="status" aria-hidden="true"></span>
  <span class="visually-hidden">Loading...</span>
</button>

<!-- Spinner border and button with text -->
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-border" role="status" aria-hidden="true"></span>
  Loading...
</button>

<!-- Spinner grow and button without text -->
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-grow" role="status" aria-hidden="true"></span>
  <span class="visually-hidden">Loading...</span>
</button>

<!-- Spinner grow and button with text -->
<button class="btn btn-primary" type="button" disabled>
  <span class="spinner-grow" role="status" aria-hidden="true"></span>
  Loading...
</button>
```

---
[&#8682; To Top](#-spinners)

[&#10094; Previous Topic](./components.scrollspy.md) &emsp; [Next Topic &#10095;](./components.toasts.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)