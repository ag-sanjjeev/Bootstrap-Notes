## &#10162; Bootstrap Content:

### &#9780; Overview:
1. [Reboot](#-reboot)
2. [Typography](#-typography)
3. [Images](#-images)
4. [Tables](#-tables)
5. [Figures](#-figures)

### &#10022; Reboot:
A set of styles that normalize the browser default styles, Which ensuring a consistent baseline across different browsers. To use link the reboot.css file in the HTML document to apply the reboot styles.

### &#10022; Typography
- Headings: The HTML has heading tags of `<h1> to <h6>`. In same, bootstrap has heading classes `.h1 to .h6` to match styling corresponding heading tag.
- Display Headings: To display heading as larger to stand-out than traditional heading tags. Bootstrap has display class `.display-1 to .display-6`. Which display the text from larger to smaller.
Body text: To display paragraph that look easier to read. Bootstrap has class `.lead` to make paragraph readable.

### &#10022; Images:
- Responsive Images:
To make images responsive in the web pages, Bootstrap has class to make images responsive across different devices.

```html
<img src="{URL/Location}" class="img-fluid" alt="{alt-text}">
```

- Thumbnail Images:
To represent the images as thumbnails with 1px border-radius in bootstrap.

```html
<img src="{URL/Location}" class="img-thumbnail" alt="{alt-text}">
```

- Image Alignment:
To align images in left or right or center to the container.

```html
<!-- Left Aligned Image -->
<img src="{URL/Location}" class="float-start" alt="{alt-text}">

<!-- Right Aligned Image -->
<img src="{URL/Location}" class="float-end" alt="{alt-text}">

<!-- Center Aligned Image-->
<img src="{URL/Location}" class="mx-auto d-block" alt="{alt-text}">

<!-- Center Aligned Image Using Text Alignment -->
<div class="text-center">
  <img src="{URL/Location}" alt="{alt-text}">
</div>
```

### &#10022; Tables:
Bootstrap can be used to create beautiful and responsive tables.

*Syntax: add `.table` class in the table element.*
```html
<table class="table">
  <thead> ... </thead>
  <tbody>
    ...
  </tbody>
</table>
```

- Colored Table:
To add different color schemes to table elements. Which is described in the bootstrap as, `table-primary`, `table-secondary`, `table-success`, `table-danger`, `table-warning`, `table-info`, `table-light`, `table-dark`.

It can be applied to entire table, entire table row, specific table cell.

```html
<!-- This will apply color scheme to entire table -->
<table class="table-primary">...</table>

<!-- This will apply color scheme to entire table row -->
<tr class="table-success">...</tr>

<!-- This will apply color scheme to specific table cell -->
<td class="table-warning">...</td>
```

- Zebra Stripped Table:
*Syntax: add `.table-striped` class to table*

```html
<table class="table table-striped">
  ...
</table>
```

- Add dark themed Table:
*Syntax: add `.table-dark` class to table*

```html
<table class="table table-dark">
  ...
</table>
```

- Add hoverable Table:
*Syntax: add `.table-hover` class to table*

```html
<table class="table table-hover">
  ...
</table>
```

- Active Tables:
To Highlight a table row or cell by adding a `.table-active` class.

```html
<!-- Highlight Table Row -->
<tr class="table-active">
...
</tr>
<!-- Highlight Table Cell -->
<td class="table-active">...</td>
```

- Table Borders:
To Add borders on all sides of the table and cells by adding `.table-bordered` class. To make table border less by adding `.table-borderless` class.

```html
<!-- Default Border Color -->
<table class="table table-bordered">
  ...
</table>

<!-- Custom Border Color -->
<table class="table table-bordered border-primary">
  ...
</table>

<!-- Borderless Table -->
<table class="table table-borderless">
  ...
</table>
```

- Small Tables:
To make table compact in size by adding `.table-sm` class.

```html
<table class="table table-sm">
  ...
</table>
```

- Vertical Alignment:
To align table cells data based on vertical axis. By default, [`<thead>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/thead-tag.md) are aligned vertically to the bottom. [`<tbody>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/tbody-tag.md) inherit their vertical alignment from [`<table>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/table-tag.md) but it is aligned vertically to the the top.

Bootstrap has vertical align classes such as `.align-top`, `.align-middle`, `.align-bottom`.
```html
<!-- It aligns vertically to the bottom through out table -->
<table class="table align-bottom">
  ...
</table>
```

```html
<!-- It aligns vertically to the top through out table row -->
<tr class="align-top">
  ...
</tr>
```

```html
<!-- It aligns vertically to the middle for particular table cell -->
<td class="align-middle">
  ...
</td>
```

- Table head Design:
To apply background color to the table head with modifier classes such `.table-light` or `.table-dark`

```html
<thead class="table-dark">
  ...
</thead>
```

- Table Captions:
To make table captions look nice and readable with bootstrap.

```html
<!-- This will make some table caption to the bottom of the table -->
<table class="table">
  <caption>Table Caption</caption>
  <thead>
    ...
  </thead>
  <tbody>
    ...
  </tbody>
</table>
```

```html
<!-- To make table caption to be appear on the top of the table -->
<table class="table caption-top">
  <caption>Table Caption</caption>
  <thead>
    ...
  </thead>
  <tbody>
    ...
  </tbody>
</table>
```

- Responsive Tables:
To make tables to be scrolled horizontally. That makes table responsive across all viewports. 
To apply responsive to tables by wrapping a `.table` class with `.table-responsive` class. 
And apply a maximum breakpoint to have a table to be responsive with classes such as `.table-responsive-{sm|md|lg|xl|xxl}`.

Otherwise, To make table to be always responsive nature by adding class `.table-responsive`.

```html
<div class="table-responsive">
  <table class="table">
    ...
  </table>
</div>
```

### &#10022; Figures:
Bootstrap can add some baseline style to the elements such as [`<figure>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/figure-tag.md), [`<figcaption>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/figcaption-tag.md) with classes such as `.figure`, `.figure-img`, `.fig-caption`.

```html
<figure class="figure">
  <img src="{URL/Location}" class="figure-img img-fluid" alt="{alt-text}">
  <figcaption class="figure-caption">{Figure Caption}</figcaption>
</figure>
```

---
[&#8682; To Top](#-bootstrap-content)

[&#10094; Previous Topic](./bootstrap-layouts.md) &emsp; [Next Topic &#10095;](./components.md)

[&#8962; Goto Home Page](../../README.md)