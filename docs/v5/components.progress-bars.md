## &#10162; Progress Bars:
Create beautiful custom progress bars using bootstrap. This will make richer than HTML [`<progress>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/progress-tag.md) tag. 

*Syntax:*
  - `.progress` class represents the container for progress bars.
  - `.progress-bar` class represents the progress bar.

```html
<!-- 0% percentage progress bar -->
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
</div>

<!-- 100% percentage progress bar -->
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 100%" aria-valuenow="100" aria-valuemin="0" aria-valuemax="100"></div>
</div>
```

### &#10022; Progress bar with label:

```html
<div class="progress">
  <div class="progress-bar" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

### &#10022; Progress bar height:

```html
<div class="progress" style="height: 1px;">
  <div class="progress-bar" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

### &#10022; Colored progress bar:

*Syntax: add `.bg-{primary|secondary|success|warning|danger|info}` class to the `.progress-bar` class.*

```html
<div class="progress">
  <div class="progress-bar bg-primary" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

### &#10022; Multi stage progress bar:

*Syntax: add multiple `.progress-bar` class element with different color.*

```html
<div class="progress">
  <!-- First stage progress bar -->
  <div class="progress-bar bg-primary" role="progressbar" style="width: 20%;" aria-valuenow="20" aria-valuemin="0" aria-valuemax="100"></div>
  <!-- Middle stage progress bar -->
  <div class="progress-bar bg-success" role="progressbar" style="width: 30%;" aria-valuenow="30" aria-valuemin="0" aria-valuemax="100"></div>
  <!-- Last stage progress bar -->
  <div class="progress-bar bg-warning" role="progressbar" style="width: 10%;" aria-valuenow="10" aria-valuemin="0" aria-valuemax="100">10%</div>
</div>
```

### &#10022; Striped progress bar:

*Syntax: add `.progress-bar-striped` class to the `.progress-bar` class.*

```html
<div class="progress">
  <div class="progress-bar bg-primary progress-bar-striped" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

### &#10022; Animated progress bar:

*Syntax: add `.progress-bar-animated` class to the `.progress-bar` class.*

```html
<div class="progress">
  <div class="progress-bar bg-primary progress-bar-striped progress-bar-animated" role="progressbar" style="width: 50%;" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">50%</div>
</div>
```

---
[&#8682; To Top](#-progress-bars)

[&#10094; Previous Topic](./components.popovers.md) &emsp; [Next Topic &#10095;](./components.scrollspy.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)