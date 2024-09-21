## &#10162; Float:
Float elements based on different viewport and screen sizes using bootstrap.

*Syntax:* 
- `float-none` to set the element do not float on any viewport. 
- `float-start` to set the element float from starting point of the container on any viewport. 
- `float-end` to set the element float to ending point of the container on any viewport. 
- `float-{breakpoint}-none` to set the element do not float on specified screen size. 
- `float-{breakpoint}-start` to set the element float from starting point of the container on specified screen size. 
- `float-{breakpoint}-end` to set the element float to ending point of the container on specified screen size.
- List of breakpoints:
	- `sm` - Small screen size
	- `md` - Medium screen size
	- `lg` - Large screen size
	- `xl` - Extra large screen size
	- `xxl` - Extra extra large screen size

```html
<!-- Float from starting point of the container -->
<div class="float-start">...</div>

<!-- Float from starting point of the container on medium screen size -->
<div class="float-sm-end">...</div>

<!-- Do not float on large screen size -->
<div class="float-lg-none">...</div>
```

---
[&#8682; To Top](#-float)

[&#10094; Previous Topic](./customization-and-theming.flex.md) &emsp; [Next Topic &#10095;](./customization-and-theming.interactions.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)