## &#10162; Bootstrap Layouts:
Bootstrap has pre-defined styles for creating CSS layout systems such as flexboxes and grids.

### &#9780; Overview:
1. [Breakpoints](#-breakpoints)
2. [Containers](#-containers)
3. [Grid](#-grid)
4. [Rows](#-rows)
5. [Columns](#-columns)
6. [Columns Alignment](#-columns-alignment)
7. [Columns Order](#-columns-order)
8. [Gutters](#-gutters)
9. [Nesting and offsets](#-nesting-and-offsets)
10. [Utilities](#-utilities)
11. [Z Index](#-z-index)

### &#10022; Breakpoints:
Bootstrap uses a responsive layout system that adapts to different screen sizes. It defines several breakpoints to adjust the layout accordingly:

*Syntax: Bootstrap Breakpoints and their notation and prefixes.*
```css
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
);
```

 - Extra small: Less than 576px
 - Small: 576px to 768px
 - Medium: 768px to 992px
 - Large: 992px to 1200px
 - Extra large: 1200px to 1400px
 - Extra extra large: 1400px or greater

### &#10022; Containers:
Containers are used to wrap the content and to align items within the viewport. It is required for implementing `grid` system layout for the elements.

 - Bootstrap has three different containers:
  - `.container`, which sets a max-width at each responsive breakpoint
  - `.container-fluid`, which sets a width: 100% at all breakpoints
  - `.container-{breakpoint}`, which sets a width: 100% until the specified breakpoint met
 - Breakpoint Containers:
  - `.container-sm` - Which sets 100% width at <576px
  - `.container-md` - Which sets 100% width at ≥576px
  - `.container-lg` - Which sets 100% width at ≥768px
  - `.container-xl` - Which sets 100% width at ≥992px
  - `.container-xxl ` - Which sets 100% width at ≥1200px
  - `.container-fluid ` - Which sets 100% width at ≥1400px
 - Default Container:
  - `.container` - Which sets 100% width at <576px. It is similar to the `.container-sm`
  ```html
  <div class="container">
    ...
  </div>
  ```
 - Fluid Containers:
  - `.container-fluid` - Which sets 100% width at all viewports and spanning the entire width of the viewport.
  ```html
  <div class="container-fluid">
    ...
  </div>
  ```

### &#10022; Grid:
Bootstrap is famous for responsive grid system layouts. It consists of rows and columns.
*Syntax:*
```html
<div class="container">
  <div class="row">
    <div class="col">...</div>
    <div class="col-3">...</div>
    <div class="col-md-3">...</div>
  </div>
</div>
```

### &#10022; Rows:
Rows are used to group columns together.

*Syntax:*
```html
<div class="row">
  <!-- Columns -->
  ...
</div>
```

### &#10022; Columns:
Bootstrap grid system comes with maximum 12 column system in a grid row.

*Syntax:*
```html
<div class="col">...</div>
<div class="col-3">...</div>
<div class="col-md-3">...</div>
```

These columns takes full until met the specific breakpoints. And evenly divides the width of column in a row upto 12 columns.
  - Each column will takes maximum width of the container until less than the breakpoints:
    - `.col-` <576px
    - `.col-sm-` ≥576px
    - `.col-md-` ≥768px
    - `.col-lg-` ≥992px
    - `.col-xl-` ≥1200px
    - `.col-xxl-` ≥1400px
  - To apply equal width for all columns in a grid row:
    - `.col`
    - `.col-sm`
    - `.col-md`
    - `.col-lg`
    - `.col-xl`
    - `.col-xxl`
  - To apply variable width for specific columns in a grid row:
    - `col-{breakpoint}-auto`
  - To apply fixed width for specific columns in a grid row:
    - `col-{breakpoint}-{nos}` - where `nos` ranges from 1 - 12
  - To apply different width for the columns use multiple column class:
    - That should be specified in the order from smaller break point to larger
    ```html
    <div class="container">
      <!-- Columns start at 50% width on mobile and span up to 33.3% width on medium screen sized devices such as laptops and desktops  -->
      <div class="row">
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
        <div class="col-6 col-md-4">.col-6 .col-md-4</div>
      </div>

      <!-- Columns are always 50% width on all devices -->
      <div class="row">
        <div class="col-6">.col-6</div>
        <div class="col-6">.col-6</div>
      </div>
    </div>
    ```
  - Row Columns:
    - To specify number of columns should be in the row
    - `.row` as a default. with `.row-cols-auto` which sets number of columns based on spaces availability.
    - `.row-cols-{nos}` classes to quickly set the number of columns in a grid row.
    ```html
    <div class="container">
      <!-- This will allow only three columns in a row and other will be wrapped into new row -->
      <div class="row row-cols-3">
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
        <div class="col">Column</div>
      </div>
    </div>
    ```

### &#10022; Columns Alignment:
Bootstrap uses flexbox utilities to align columns in the grid row.

- Vertical Alignments:
  - `align-items-start` is equivalent to `align-items: flex-start;`
  - `align-items-center` is equivalent to `align-items: center;`
  - `align-items-end` is equivalent to `align-items: flex-end;`
  - `align-self-start` is equivalent to `align-self: flex-start;`
  - `align-self-center` is equivalent to `align-self: center;`
  - `align-self-end` is equivalent to `align-self: flex-end;`
```html
<div class="container">
  <div class="row align-items-start">
    <div class="col">...</div>
    <div class="col">...</div>
    <div class="col">...</div>
  </div>
</div>

<div class="container">
  <div class="row">
    <div class="col align-self-start">...</div>
    <div class="col align-self-center">...</div>
    <div class="col align-self-end">...</div>
  </div>
</div>
```

- Horizontal Alignments:
  - `justify-content-start` is equivalent to `justify-content: flex-start;`
  - `justify-content-center` is equivalent to `justify-content: center;`
  - `justify-content-end` is equivalent to `justify-content: flex-end;`
  - `justify-content-around` is equivalent to `justify-content: space-around;`
  - `justify-content-between` is equivalent to `justify-content: space-between;`
  - `justify-content-evenly` is equivalent to `justify-content: space-evenly;`

```html
<div class="container">
  <div class="row justify-content-start">
    <div class="col-md-2">...</div>
    <div class="col-4">...</div>
  </div>
</div>
```

### &#10022; Columns Order:
Bootstrap can order the grid columns as required. The columns are to be ordered as by specified number in the `order` class.

```html
<div class="container">
  <div class="row">
    <!-- This will be first column in the row, due to no order specification -->
    <div class="col">...</div>
    <!-- This will be last column in the row, due to higher order specified -->
    <div class="col order-6">...</div>
    <!-- This will be second column in the row, due to least order specified -->
    <div class="col order-1">...</div>
  </div>
</div>
```

### &#10022; Gutters:
Gutters are the spaces between grid columns. In bootstrap, Gutters are starts at 1.5rem (24px) wide on both sides of column.

- Horizontal gutters:
  - `.gx-*` where the `*` specifies that amount of space to be added in the x axis.
```html
<div class="container">
  <div class="row gx-1">
    <div class="col">...</div>
    <div class="col">...</div>
  </div>
</div>
```
- Vertical gutters:
  - `.gy-*` where the `*` specifies that amount of space to be added in the y axis.
```html
<div class="container">
  <div class="row gy-2">
    <div class="col-6">...</div>
    <div class="col-6">...</div>
    <div class="col-6">...</div>
    <div class="col-6">...</div>
  </div>
</div>
```

- Responsive gutters:
  - It applies gutter based on the different viewport.
```html
<div class="container">
  <div class="row row-cols-2 row-cols-lg-6 g-2 g-lg-4">
    ...
  </div>
</div>
```

- Mixed Gutters:
  - `.g-*` where the `*` specifies that amount of space to be added in the both axis.
```html
<div class="container">
  <div class="row g-3">
    <div class="col-6">...</div>
    <div class="col-6">...</div>
    <div class="col-6">...</div>
    <div class="col-6">...</div>
  </div>
</div>
```

### &#10022; Nesting and offsets:
Columns can be nested within other columns, and to create uneven column layouts with offsets.
```html
<div class="row">
  <div class="col-md-6">
    <div class="row">
      <!-- These columns inside another column -->
      <div class="col-md-3"></div>
      <div class="col-md-3"></div>
      <div class="col-md-3"></div>
    </div>
  </div>
</div>
```

```html
<div class="row">
  <div class="col-md-4"></div>
  <!-- Which sets offset to create uneven layout -->
  <div class="col-md-4 offset-md-4"></div>
</div>
```

### &#10022; Utilities:
- Margin Utilities:
```html
<div class="container">
  <div class="row">
    <!-- This will be on the starting position of the grid row -->
    <div class="col-md-4">...</div>
    <!-- This will be on the ending position of the grid row -->
    <div class="col-md-4 ms-auto">...</div>
  </div>
  <div class="row">
    <!-- This will be on the ending position of first half of the grid row -->
    <div class="col-md-2 ms-md-auto">...</div>
    <!-- This will be on the ending position of last half of the grid row -->
    <div class="col-md-2 ms-md-auto">...</div>
  </div>
  <div class="row">
    <!-- This will be on the starting position of the grid row -->
    <div class="col-5 me-auto">...</div>
    <!-- This will be on the ending position of the grid row -->
    <div class="col-auto">...</div>
  </div>
</div>
```

### &#10022; Z Index:
Different z-index defined in the bootstrap as below:
- dropdown - 1000
- sticky - 1020
- fixed - 1030
- modal backdrop - 1040
- offcanvas - 1050
- modal - 1060
- popover - 1070
- tooltip - 1080

---
[&#8682; To Top](#-bootstrap-layouts)

[&#10094; Previous Topic](../../introduction.md) &emsp; [Next Topic &#10095;](./bootstrap-content.md)

[&#8962; Goto Home Page](../../README.md)