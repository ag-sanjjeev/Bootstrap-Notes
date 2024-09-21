## &#10162; Flex:
Apply display property as flex to the elements with bootstrap class on different breakpoints.

*Syntax:* 
- `.d-flex` for mentions display property flex without breakpoint is always focus on extra small screen size.
- `.d-inline-flex` for mentions display property inline flex without breakpoint is always focus on extra small screen size.
- `.d-{breakpoint}-flex` to set display property flex on different screen size.
- `.d-{breakpoint}-inline-flex` to set display property inline flex on different screen size.
- List of breakpoints:
	- `sm` - Small screen size
	- `md` - Medium screen size
	- `lg` - Large screen size
	- `xl` - Extra large screen size
	- `xxl` - Extra extra large screen size

```html
<!-- Flex box container -->
<div class="d-flex">...</div>

<!-- Inline Flex box container -->
<div class="d-inline-flex">...</div>
```

### &#10022; Direction of flex items:
Flex direction modified with row and column with reverse.

*Syntax:* 
- `.flex-{row|column}` for items are arrange in a single horizontal axis or vertical.
- `.flex-{row|column}-reverse` for items are arranged in reverse to horizontal axis or vertical.
- `.flex-{breakpoint}-{row|column}` for items are arrange in a single horizontal axis or vertical based on breakpoint.
- `.flex-{breakpoint}-{row|column}-reverse` for items are arranged in reverse to horizontal axis or vertical based on breakpoint.

```html
<!-- Flex items in a row -->
<div class="d-flex flex-row">...</div>
<!-- Flex items in a row when small screen devices -->
<div class="d-flex flex-sm-row">...</div>
<!-- Flex items in a row with reverse order when medium screen sizes -->
<div class="d-flex flex-md-row-reverse">...</div>

<!-- Flex items in a column -->
<div class="d-flex flex-column">...</div>
<!-- Flex items in a column when medium screen sizes -->
<div class="d-flex flex-md-column">...</div>
<!-- Flex items in a column with reverse order when small screen sizes -->
<div class="d-flex flex-sm-column-reverse">...</div>
```

### &#10022; Justify Content:
It justifies entire flex items inside the flexbox container.

*Syntax:*
- `.justify-content-{value}` always set from extra small screen size.
- `.justify-content-{breakpoint}-{value}` sets justify content values based on screen sizes.
- List of justify content values:
	- `start`
	- `end`
	- `center`
	- `between`
	- `around`
	- `evenly`

```html
<!-- Justify content by adding space around flex items -->
<div class="d-flex justify-content-around">...</div>

<!-- Justify content by center for flex items on small screen sizes -->
<div class="d-flex justify-content-sm-center">...</div>

<!-- Justify content by adding space evenly to flex items -->
<div class="d-flex justify-content-evenly">...</div>
```

### &#10022; Align Content:
It aligns entire flex items together inside the flexbox container on the cross axis.

*Syntax:*
- `.align-content-{value}` always set from extra small screen size.
- `.align-content-{breakpoint}-{value}` sets align entire flex items together based on values and screen sizes.
- List of align content values:
	- `start`
	- `end`
	- `center`
	- `around`
	- `stretch`

```html
<!-- Align flex items together by adding space around flex items together -->
<div class="d-flex align-content-around">...</div>

<!-- Align content by center for flex items together on medium screen sizes -->
<div class="d-flex align-content-md-center">...</div>

<!-- Align content by stretching height evenly on each flex items -->
<div class="d-flex align-content-stretch">...</div>
```

### &#10022; Align Items:
It aligns entire flex items inside the flexbox container.

*Syntax:*
- `.align-items-{value}` always set from extra small screen size.
- `.align-items-{breakpoint}-{value}` align items based on values and screen sizes.
- List of align items values:
	- `start`
	- `end`
	- `center`
	- `baseline`
	- `stretch`

```html
<!-- Align flex items to starting point of main axis -->
<div class="d-flex align-items-start">...</div>

<!-- Align flex items to center of the main axis on small screen sizes -->
<div class="d-flex align-items-sm-center">...</div>

<!-- Align flex items by stretching their height by utilizing excess space of main axis -->
<div class="d-flex align-items-stretch">...</div>
```

### &#10022; Align Self:
It aligns individual flex item of the flexbox container.

*Syntax:*
- `.align-self-{value}` always set from extra small screen size.
- `.align-self-{breakpoint}-{value}` align particular flex item based on values and screen sizes.
- List of align self values:
	- `start`
	- `end`
	- `center`
	- `baseline`
	- `stretch`

```html
<!-- Align particular flex item to ending point of main axis -->
<div class="d-flex align-items-end">...</div>

<!-- Align particular flex item to baseline of the main axis on large screen sizes -->
<div class="d-flex align-items-lg-baseline">...</div>

<!-- Align particular flex item by stretching their height by utilizing excess space of main axis -->
<div class="d-flex align-items-stretch">...</div>
```

### &#10022; Flex fill:
It fills the width of flex items by utilizing excess space available in the flexbox container.

*Syntax:*
- `.flex-fill` always set from extra small screen size.
- `.flex-{breakpoint}-fill` fills available excess space to flex item based on screen sizes.

```html
<div class="d-flex">
  <div class="flex-fill">...</div>
  <div class="flex-fill">...</div>
  <div class="flex-fill">...</div>
</div>
```

### &#10022; Flex grow and shrink:
It will grow or shrink the specific flex items in the flexbox container.

*Syntax:*
- `.flex-{grow|shrink}-{value}` always set from extra small screen size.
- `.flex-{breakpoint}-{grow|shrink}-{value}` It will grow or shrinks flex item based on values and screen sizes.
- List of values:
	- `1` - takes whether to be grown or shrunken.
	- `0` - avoids whether to be grown or shrunken. 

```html
<!-- Flex grow -->
<div class="d-flex">
	<!-- It will grow by utilizing available excess space on this flexbox container -->
  <div class="flex-grow-1">...</div>

	<!-- It will grow when small screen size by utilizing available excess space on this flexbox container -->
  <div class="flex-sm-grow-1">...</div>
  
	<!-- It will not grow -->
  <div class="flex-grow-0">...</div>  

  <!-- This will be fit in this flexbox container -->
  <div>...</div>
  <div>...</div>
</div>

<!-- Flex shrink -->
<div class="d-flex">
	<!-- It will shrink as much as possible -->
  <div class="flex-shrink-1">...</div>

	<!-- It will shrink when small screen size as much as possible  -->
  <div class="flex-sm-shrink-1">...</div>
  
	<!-- It will not shrink -->
  <div class="flex-shrink-0">...</div>  

  <!-- This will be grown or takes advantage in this flexbox container -->
  <div>...</div>
  <div>...</div>
</div>
```

### &#10022; Flex auto margin:
	
```html
<!-- Margin auto on start and end side of the flex item -->
<div class="d-flex">
	<!-- This me-auto will set auto margin on end of this flex item -->
	<div class="me-auto">...</div>

	<!-- other flex items will be justified to the end -->
  <div>...</div>
  <div>...</div>
</div>

<!-- Margin auto on top and bottom side of the flex item -->
<div class="d-flex flex-column">
	<!-- This mb-auto will set auto margin on bottom of this flex item -->
	<div class="mb-auto">...</div>

	<!-- other flex items will be aligned to the end -->
  <div>...</div>
  <div>...</div>
</div>
```

### &#10022; Flex wrap:
Flex items are wrapping by default based on the flexbox container size. To avoid flexwrap by adding bootstrap class.

*Syntax:* 
- Add `.flex-nowrap` class to avoid wrapping of flex items on extra small screen size.
- Add `.flex-{breakpoint}-nowrap` class to avoid wrapping of flex items.
- Add `.flex-wrap` class to wrap flex items on extra small screen size.
- Add `.flex-{breakpoint}-wrap` class to wrap flex items.
- Add `.flex-wrap-reverse` class to wrap flex items in reverse direction on extra small screen size.
- Add `.flex-{breakpoint}-wrap-reverse` class to wrap flex items in reverse direction.

```html
<!-- Avoid wrapping -->
<div class="d-flex flex-nowrap">...</div>

<!-- Avoid wrapping on large screen size -->
<div class="d-flex flex-lg-nowrap">...</div>

<!-- Wrapping flex items -->
<div class="d-flex flex-wrap">...</div>

<!-- Wrapping flex items in reverse direction on small screen size -->
<div class="d-flex flex-sm-wrap-reverse">...</div>
```

### &#10022; Flex item order:
To order visually to flex items by specifying bootstrap class.

*Syntax:*
- `order-{value}` class to order on extra small screen size.
- `order-{breakpoint}-{value}` class to order based on screen size.
- List of order values:
	- `0`,
	- `1`,
	- `2`,
	- `3`,
	- `5`,
	- `first`,
	- `last`

```html
<div class="d-flex">
	<!-- Order to last among the flex items -->
  <div class="order-last">...</div>

	<!-- Order to first among the flex items -->
  <div class="order-1">...</div>
	
	<!-- Order to center or third among the flex items -->
  <div class="order-3">...</div>
</div>
```

---
[&#8682; To Top](#-flex)

[&#10094; Previous Topic](./customization-and-theming.display.md) &emsp; [Next Topic &#10095;](./customization-and-theming.float.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)