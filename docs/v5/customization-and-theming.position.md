## &#10162; Position:
Bootstrap gives the ability to adjust position of an element.

### &#10022; Position classes:

*Syntax:* 
- `.position-relative` class sets the position of an element as relative.
- `.position-absolute` class sets the position of an element as absolute.
- `.position-sticky` class sets the position of an element as sticky.
- `.position-fixed`  class sets the position of an element as fixed.
- `.position-static` class sets the position of an element as static.

```html
<div class="position-absolute">...</div>
```

### &#10022; Position arrangements:

*Syntax:* 
- `top-{value}` class will set distance from top to the position value. 
- `end-{value}` class will set distance from right to the position value. 
- `bottom-{value}` class will set distance from bottom to the position value. 
- `start-{value}` class will set distance from left to the position value. 
- The list of values:
	- `0` - for 0% distance value
	- `50` - for 50% distance value
	- `100` - for 100% distance value

```html
<!-- This will set position relative for the container -->
<div class="position-relative">
	<!-- This will set position to top left corner of the container -->
  <div class="position-absolute top-0 start-0"></div>

  <!-- This will set position sticky to top right corner of the container -->
  <div class="position-sticky top-0 end-0"></div>
</div>
```

### &#10022; Translate classes:

*Syntax:*
- `.translate-middle` class will set transform property value as translateX(-50%) and translateY(-50%).
- `.translate-middle-x` class will set transform property value as translateX(-50%).
- `.translate-middle-y` class will set transform property value as translateY(-50%).

```html
<!-- This will center the element inside the container -->
<div class="position-relative">
	<div class="position-absolute top-50 start-50 translate-middle"></div>
</div>
```

---
[&#8682; To Top](#-position)

[&#10094; Previous Topic](./customization-and-theming.overflow.md) &emsp; [Next Topic &#10095;](./customization-and-theming.shadows.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)