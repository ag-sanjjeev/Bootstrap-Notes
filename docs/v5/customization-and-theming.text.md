## &#10162; Text:
Bootstrap gives ability to apply styles on text.

### &#10022; Text alignment:

*Syntax:* 
- `.text-{alignment}` class will align text based on value on all screen size.
- `.text-{breakpoints}-{alignment}` class will align text based on value and viewport.
- List of alignments:
	- `start` - align to the start/left side of the container	
	- `end` - align to the end/right side of the container	
	- `center` - align center to the container
- List of breakpoints:
	- `sm` - small screen size	
	- `md` - medium screen size	
	- `lg` - large screen size	
	- `xl` - extra large screen size	

```html
<!-- Text aligned to the end/right side of the container -->
<p class="text-end">...</p>

<!-- Text aligned on center from small screen size and wider -->
<p class="text-sm-center">...</p>

<!-- Text aligned on start/left side from medium screen size and wider -->
<p class="text-md-start">...</p>
```

### &#10022; Text wrapping:
To wrap text based on the container width.

*Syntax: add `.text-wrap` class.* 

```html
<p class="text-wrap">...</p>
```

### &#10022; Text overflow:
To avoid wrapping of text and to make overflow out of the container width.

*Syntax: add `.text-nowrap` class.* 

```html
<p class="text-nowrap">...</p>
```

### &#10022; Word break:
It break words when it is long. But word break is not possible in RTL language as same for bootstrap. 

*Syntax: add `.text-break` class.* 

```html
<p class="text-break">...</p>
```

### &#10022; Text transform:
To make text case transformation with bootstrap.

*Syntax:*
- `.text-lowercase` class will transform text into lowered case.
- `.text-uppercase` class will transform text into upper case.
- `.text-capitalize` class will transform text into capitalize.

```html
<p class="text-capitalize">...</p>
```

### &#10022; Font size:
To adjust font size of the text with bootstrap. It sames heading classes in bootstrap. So, if number value of font size class increases, then the font size decreases.

*Syntax:*
- `.fs-{value}` class set font size based on value.
- List of font size values:
	- `1` - Bigger
	- `2` - Big
	- `3` - Medium
	- `4` - Small
	- `5` - Smaller
	- `6` - Smallest

```html
<p class="fs-2">...</p>
```

### &#10022; Font weight:
To adjust font weight of the text with bootstrap. 

*Syntax:*
- `.fw-{value}` class set font weight based on value.
- List of font weight values:
	- `bolder`
	- `bold`
	- `normal`
	- `light`
	- `lighter`

```html
<p class="fw-bold">...</p>
```

### &#10022; Font style:
To adjust font style of the text with bootstrap. 

*Syntax:*
- `.fst-{value}` class set font style based on value.
- List of font style values:
	- `italic`
	- `normal`

```html
<p class="fst-italic">...</p>
```

### &#10022; Line height:
To adjust line height of the text with bootstrap. 

*Syntax:*
- `.lh-{value}` class set line height based on value.
- List of line height values:
	- `1` - set line height to 1.
	- `sm` - set small line height.
	- `base` - set base line height.
	- `lg` - set large line height.

```html
<p class="lh-lg">...</p>
```

### &#10022; Monospace text:
To make text as monospace font stack. 

*Syntax: add `.font-monospace` class.*

```html
<p class="font-monospace">...</p>
```

### &#10022; Text reset:
Text reset will inherit color font the parent element.

*Syntax: add `.text-reset` class.*

```html
<p class="text-warning">
	<!-- Anchor tag inherit the color value from the parent -->
	{text content} <a href="#" class="text-reset">{Link text}</a>
</p>
```

### &#10022; Text decoration:
To decorate text with bootstrap.

*Syntax:*
- `.text-decoration-none` class will removes the any text decoration applied to the text. 
- `.text-decoration-line-through` class will make strike through the text. 
- `.text-decoration-underline` class will add underline to the text. 

```html
<p class="text-decoration-underline"></p>
```

---
[&#8682; To Top](#-text)

[&#10094; Previous Topic](./customization-and-theming.spacing.md) &emsp; [Next Topic &#10095;](./customization-and-theming.vertical-align.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Customization and Theming](./customization-and-theming.md)