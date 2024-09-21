## &#10022; Display:
Apply display property to the element with bootstrap class on different breakpoints.

*Syntax:* 
- `.d-` for mentions display property.
- `.d-{breakpoint}-{value}` to set display property on different screen size.
- `.d-{value}` without breakpoint is always focus on extra small screen size.
- List of breakpoints:
	- `sm` - Small screen size
	- `md` - Medium screen size
	- `lg` - Large screen size
	- `xl` - Extra large screen size
	- `xxl` - Extra extra large screen size
- List of display property value:
	- `none` 
	-	`inline` 
	-	`inline-block`
	-	`inline-flex`
	-	`block`
	-	`flex`
	-	`grid`
	-	`table`
	-	`table-cell`
	-	`table-row`

```html
<!-- 
	The element hides on extra small devices, 
	displays as block on medium screen sizes and
	displays as inline on large screen sizes
-->
<div class="d-none d-md-block d-lg-inline">...</div>
```

- Display for print:
Apply display property to the elements when printing.

*Syntax: `.d-print-{value}`*

```html
<!-- Display on screen but not on print screen -->
<div class="d-print-none">...</div>
<!-- Hides on screen but not on print screen -->
<div class="d-none d-print-block">...</div>
```

---
[&#8682; To Top](#-display)

[&#10094; Previous Topic](./customization-and-theming.colors.md) &emsp; [Next Topic &#10095;](./customization-and-theming.flex.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)