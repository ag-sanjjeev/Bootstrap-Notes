## &#10022; Buttons:
Bootstrap can make buttons that looks beautiful and nice.

*Syntax: add `.btn` class*
```html
<button type="{...}" class="btn btn-primary">{Button Text}</button>
```

- To create different buttons by adding `btn-primary, btn-secondary, btn-success, btn-danger, btn-warning, btn-info, btn-light, btn-dark` classes.

- To style button as anchor link.
```html
<button type="button" class="btn btn-link">Link</button>
```

- To create outline based buttons by adding `btn-outline-primary, btn-outline-secondary, btn-outline-success, btn-outline-danger, btn-outline-warning, btn-outline-info, btn-outline-light, btn-outline-dark` classes.

```html
<button type="button" class="btn btn-outline-primary">{Button Text}</button>
```

- To make buttons as larger in size by adding `.btn-lg` class with `.btn` class.
```html
<button type="button" class="btn btn-primary btn-lg">{Button Text}</button>
```

- To make buttons as smaller in size by adding `.btn-sm` class with `.btn` class. 
```html
<button type="button" class="btn btn-primary btn-sm">{Button Text}</button>
```

- To make buttons as disabled stage by adding attribute `disabled` or class `.disabled` to the button. And additionally set tabindex and ARIA attribute.
```html
<button type="button" class="btn btn-primary" disabled>{Button Text}</button>
<button type="button" class="btn btn-primary disabled">{Button Text}</button>

<!-- ARIA Attribute and Tabindex -->

<button type="button" class="btn btn-primary disabled" tabindex="-1" role="button" aria-disabled="true">{Button Text}</button>
```

- To make button being in active state by adding `.active` class.
```html
<button type="button" class="btn btn-primary active">{Button Text}</button>
```

- Methods related buttons:
  - `toggle()` -  Toggles push state. That makes button to be appeared as being active.
  - `dispose()` - Destroys a button element. (Removes from the DOM tree).
  - `getInstance()` -  Static method which allows to get the button instance.
  - `getOrCreateInstance()` Static method which returns a button instance or create a new one in case it wasn't initialized yet.
```javascript
var button = document.getElementById('{button-id}')
var bsButton = new bootstrap.Button(button);
bsButton.toggle();
```

---
[&#8682; To Top](#-buttons)

[&#10094; Previous Topic](./components.breadcrumb.md) &emsp; [Next Topic &#10095;](./components.button-group.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)