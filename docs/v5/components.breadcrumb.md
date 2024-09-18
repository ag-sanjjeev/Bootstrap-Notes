## &#10022; Breadcrumb:
Breadcrumbs are used for indicating navigation tree or order or the page, Where you are in the current page. Bootstrap makes Breadcrumb looks rich and nice.

*Syntax: add `.breadcrumb` class*

```html
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Blog</a></li>
    <li class="breadcrumb-item active" aria-current="page">Article Name</li>
  </ol>
</nav>
``` 

- To add custom dividers for breadcrumbs
```html
<nav style="--bs-breadcrumb-divider: '>';" aria-label="breadcrumb">
  <ol class="breadcrumb">
    ...
  </ol>
</nav>
```

---
[&#8682; To Top](#-breadcrumb)

[&#10094; Previous Topic](./components.badge.md) &emsp; [Next Topic &#10095;](./components.buttons.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)