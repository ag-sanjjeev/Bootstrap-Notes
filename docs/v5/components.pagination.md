## &#10162; Pagination:
Create beautiful pagination links to refer paged section or content in the webpage using bootstrap.

*Syntax:*
  - `.pagination` class to represent the pagination container.
  - `.page-item` class to represent the pagination item.
  - `.page-link` class to represent the pagination link.

```html
<nav aria-label="{Pagination label or title}">
  <ul class="pagination">
    <li class="page-item"><a class="page-link" href="#">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

### &#10022; Disabled page item:

*Syntax: add `.disabled` class to the `.page-item` class.*

```html
<nav aria-label="{Pagination label or title}">
  <ul class="pagination">
    <li class="page-item disabled"><a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item"><a class="page-link" href="#">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

### &#10022; Active page item:

*Syntax: add `.active` class to the `.page-item` class.*

```html
<nav aria-label="{Pagination label or title}">
  <ul class="pagination">
    <li class="page-item disabled"><a class="page-link" href="#" tabindex="-1" aria-disabled="true">Previous</a></li>
    <li class="page-item"><a class="page-link" href="#">1</a></li>
    <li class="page-item active"><a class="page-link" href="#" aria-current="page">2</a></li>
    <li class="page-item"><a class="page-link" href="#">3</a></li>
    <li class="page-item"><a class="page-link" href="#">Next</a></li>
  </ul>
</nav>
```

### &#10022; Sizing of pagination:

*Syntax: add `.pagination-{sm|lg}` classes to `.pagination` class.*

```html
<!-- Small sized pagination -->
<nav aria-label="{Pagination label or title}">
  <ul class="pagination pagination-sm">...</ul>
</nav>

<!-- Large sized pagination -->
<nav aria-label="{Pagination label or title}">
  <ul class="pagination pagination-lg">...</ul>
</nav>
```

### &#10022; Alignment of pagination:

*Syntax:*
  - Add `.justify-content-center` class to `.pagination` class for center alignment.
  - Add `.justify-content-end` class to `.pagination` class for right alignment.

```html
<!-- Center aligned pagination -->
<nav aria-label="{Pagination label or title}">
  <ul class="pagination justify-content-center">...</ul>
</nav>

<!-- Right aligned pagination -->
<nav aria-label="{Pagination label or title}">
  <ul class="pagination justify-content-end">...</ul>
</nav>
```

---
[&#8682; To Top](#-pagination)

[&#10094; Previous Topic](./components.offcanvas.md) &emsp; [Next Topic &#10095;](./components.popovers.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)