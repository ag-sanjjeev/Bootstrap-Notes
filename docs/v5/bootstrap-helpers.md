## &#10162; Bootstrap Helpers:

### &#9780; Overview:
1. [Clearfix](#-clearfix)
2. [Colored links](#-colored-links)
3. [Ratio](#-ratio)
4. [Position](#-position)
5. [Visually hidden](#-visually-hidden)
6. [Stretched link](#-stretched-link)
7. [Text truncation](#-text-truncation)

### &#10022; Clearfix:
Clear float elements using bootstrap `.clearfix` class.

```html
<div class="clearfix">...</div>

<!-- clear and fix the floating element in the webpages -->
<div class="bg-primary clearfix">
  <button type="button" class="btn btn-light float-start">{Button text}</button>
  <button type="button" class="btn btn-light float-end">{Button text}</button>
</div>
```

### &#10022; Colored links
Create colored links with bootstrap classes.

*Syntax: add `.link-{primary|secondary|success|warning|danger|info|light|dark}` class to [`<a>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/a-tag.md) tag.*

```html
<a href="#" class="link-primary">{Link text}</a>
<a href="#" class="link-secondary">{Link text}</a>
<a href="#" class="link-success">{Link text}</a>
<a href="#" class="link-warning">{Link text}</a>
<a href="#" class="link-danger">{Link text}</a>
<a href="#" class="link-info">{Link text}</a>
<a href="#" class="link-light">{Link text}</a>
<a href="#" class="link-dark">{Link text}</a>
```

### &#10022; Ratio:
Apply aspect ratio to the element using bootstrap class.

*Syntax: add `.ratio` class with defined aspect ratio `.ratio-16x9` class.*

- List of predefined aspect ratios in bootstrap:
  - 1x1 - `.ratio-1x1`
  - 4x3 - `.ratio-4x3`
  - 16x9 - `.ratio-16x9`
  - 21x9 - `.ratio-21x9`

```html
<!-- Maintain the aspect ratio of the element as 16 time wide x 9 time tall -->
<div class="ratio ratio-16x9">
  <iframe src="{URL/Location}" allowfullscreen></iframe>
</div>
```

- Custom ratio in bootstrap:

*Syntax: set `--bs-aspect-ratio: {value}%;` on `.ratio` class.*

```html
<!-- Maintain aspect ratio of 2x3 -->
<div class="ratio" style="--bs-aspect-ratio: 66%;">
  <div>2x3</div>
</div>

<!-- Maintain aspect ratio of 2x3 -->
<div class="ratio" style="--bs-aspect-ratio: calc(2 / 3 * 100%);">
  <div>2x3</div>
</div>
```

### &#10022; Position:
To set position of element with bootstrap classes.

- Fixed top:
To set position as fixed on top.

*Syntax: add `.fixed-top` class.*

```html
<div class="fixed-top">...</div>
```

- Fixed Bottom:
To set position as fixed on bottom.

*Syntax: add `.fixed-bottom` class.*

```html
<div class="fixed-bottom">...</div>
```

- Sticky top:
To set position as sticky on top.

*Syntax: add `.sticky-top` class.*

```html
<div class="sticky-top">...</div>
```

- Responsive sticky top:
To set position as sticky on top based on screen size.

*Syntax: add `.sticky-{sm|md|lg|xl}-top` class.*

```html
<!-- Sticky top on smaller and wider screen devices -->
<div class="sticky-sm-top">...</div>

<!-- Sticky top on medium and wider screen devices -->
<div class="sticky-md-top">...</div>

<!-- Sticky top on large and wider screen devices -->
<div class="sticky-lg-top">...</div>

<!-- Sticky top on extra large and wider screen devices -->
<div class="sticky-xl-top">...</div>
```

### &#10022; Visually hidden:
This content are visually hidden but helpful to any accessibility tools such as screen readers.

*Syntax:*
  - `.visually-hidden` class will hide the content, but it will allows to any accessibility tools.
  - `.visually-hidden-focusable` class will hide the content, but it will display when it is focused by keyboard navigation. 

```html
<h3 class="visually-hidden">{Content for screen readers}</h3>
<a class="visually-hidden-focusable" href="{URL/Location}">{Link text}</a>
<div class="visually-hidden-focusable">... <a href="#">{Link text}</a> ... </div>
```


### &#10022; Stretched link:
Bootstrap will make any HTML element clickable by stretching a nested link with CSS.

*Syntax: add `.stretched-link` class.*

```html
<!-- Stretched link will make entire bootstrap card clickable and redirect with URL/Location -->
<div class="card">
  <div class="card-body">
    <h3 class="card-title">...</h3>
    <p class="card-text">...</p>
    <a href="{URL/Location}" class="btn btn-primary stretched-link">{Link text}</a>
  </div>
</div>
```

- Avoid stretching outside the parent element:

*Syntax: add `.position-relative` class to the parent element.*

```html
<!-- Stretched link will make entire bootstrap card clickable and redirect with URL/Location -->
<div class="card position-relative">
  <div class="card-body">
    <h3 class="card-title">...</h3>
    <p class="card-text">...</p>
    <a href="{URL/Location}" class="btn btn-primary stretched-link">{Link text}</a>
  </div>
</div>
```

- Stretched link will not stretching to parent due to containing block

  - The containing block will have following CSS properties:
    - `position` value other than `static`.
    - `transform` or `perspective` value other than `none`.
    - `will-change` value of `transform` or `perspective`.
    - `filter` value other than `none`
    - `will-change` value of `filter`.

```html
<!-- Stretched link will not work due to paragraph tag -->
<div class="card position-relative">
  <div class="card-body">
    <h3 class="card-title">...</h3>
    <p class="card-text">
      <!-- Stretched link -->
      <a href="{URL/Location}" class="btn btn-primary stretched-link">{Link text}</a>
    </p>
  </div>
</div>
```


### &#10022; Text truncation:
Truncate long string or text with an ellipsis.

*Syntax: add `.text-truncate` class.*

```html
<!-- Block level -->
<div class="row">
  <div class="col-2 text-truncate">{Long content}</div>
</div>

<!-- Inline level -->
<span class="d-inline-block text-truncate" style="max-width: 200px;">{Long content}</span>
```

---
[&#8682; To Top](#-bootstrap-helpers)

[&#10094; Previous Topic](./components.tooltips.md) &emsp; [Next Topic &#10095;](./customization-and-theming.md)

[&#8962; Goto Home Page](../../README.md)