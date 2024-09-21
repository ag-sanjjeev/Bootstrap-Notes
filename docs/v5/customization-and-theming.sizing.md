## &#10162; Sizing:
To set size for an element with bootstrap.

### &#10022; Relative to the parent:

*Syntax:* 
- `w-{value}` class sets the width of the element relative to the parent sizing.
- `h-{value}` class sets the height of the element relative to the parent sizing.
- `mw-100` class sets maximum width to `100%` of the element relative to the parent sizing.
- `mh-100` class sets maximum height to `100%` of the element relative to the parent sizing.
- List of sizing values:
	- `25` - 25% relative to the parent sizing.
	- `50` - 50% relative to the parent sizing.
	- `75` - 75% relative to the parent sizing.
	- `100` - 100% relative to the parent sizing.

```html
<!-- Sets the width is 25% and maximum width is 100% -->
<div class="w-25 mw-100">...</div>
```

### &#10022; Relative to the viewport:

*Syntax:* 
- `vw-100` class will set width of 100vw. 
- `vh-100` class will set height of 100vh. 
- `min-vw-100` class will set minimum width of 100vw. 
- `min-vh-100` class will set minimum height of 100vh.

```html
<!-- Sets width of 100vw -->
<div class="vw-100">...</div>

<!-- Sets height of 100vh -->
<div class="vh-100">...</div>

<!-- Sets minimum width of 100vw -->
<div class="min-vw-100">...</div>

<!-- Sets minimum height of 100vh -->
<div class="min-vh-100">...</div>
```

---
[&#8682; To Top](#-sizing)

[&#10094; Previous Topic](./customization-and-theming.shadows.md) &emsp; [Next Topic &#10095;](./customization-and-theming.spacing.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)