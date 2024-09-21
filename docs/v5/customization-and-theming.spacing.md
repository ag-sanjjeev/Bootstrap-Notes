## &#10162; Spacing:
Bootstrap gives ability to apply spacing such as margin, padding and gap for grid.

### &#10022; Margin:

*Syntax:* 
- `m` for short notation for margin.
- `t` for top side
- `e` for end/right side
- `b` for bottom side
- `s` for start/left side
- `x` for horizontal/x-axis
- `y` for vertical/y-axis
- List of margin values:
	- `0` - no margin
	- `1` - level 1/smallest margin value
	- `2` - level 2/smaller margin value
	- `3` - level 3/small margin value
	- `4` - level 4/large margin value
	- `5` - level 5/larger margin value
	- `auto` - auto margin value

```html
<!-- It sets no margin on top side -->
<div class="mt-0"></div>

<!-- It sets level 3 margin on all sides -->
<div class="m-3"></div>

<!-- It sets margin auto on horizontal axis, thus makes it as centered -->
<div class="mx-auto"></div>
```

### &#10022; Padding:

*Syntax:* 
- `p` for short notation for padding.
- `t` for top side
- `e` for end/right side
- `b` for bottom side
- `s` for start/left side
- `x` for horizontal/x-axis
- `y` for vertical/y-axis
- List of padding values:
	- `0` - no padding
	- `1` - level 1/smallest padding value
	- `2` - level 2/smaller padding value
	- `3` - level 3/small padding value
	- `4` - level 4/large padding value
	- `5` - level 5/larger padding value
	- `auto` - auto padding value

```html
<!-- It sets no padding on right side -->
<div class="pe-0"></div>

<!-- It sets level 2 padding on all sides -->
<div class="p-2"></div>

<!-- It sets padding level 3 on top and bottom side of the element -->
<div class="py-3"></div>
```

### &#10022; Gap:
It will add gap between the grid items.

*Syntax:* 
- `.gap-{value}` sets gap between grid items.
- List of gap values:
	- `0` - no gap
	- `1` - level 1/smallest gap value
	- `2` - level 2/smaller gap value
	- `3` - level 3/small gap value
	- `4` - level 4/large gap value
	- `5` - level 5/larger gap value

```html
<div class="d-grid gap-2">...</div>
```

---
[&#8682; To Top](#-spacing)

[&#10094; Previous Topic](./customization-and-theming.sizing.md) &emsp; [Next Topic &#10095;](./customization-and-theming.text.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)