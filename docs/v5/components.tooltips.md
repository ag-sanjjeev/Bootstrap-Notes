## &#10162; Tooltips:
Bootstrap can create beautiful tooltips with popperJs.

*Syntax:*
  - Tooltips must be initialized before utilize.
  - Tooltips must be hidden before removing element from DOM.
  - Add `data-bs-toggle="tooltip"` data attribute to defining tooltip on an element.

```javascript
// Tooltips are Initialized via JavaScript
var tooltipsList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'));
var tooltipsElements = tooltipsList.map(function (element) {
  return new bootstrap.Tooltip(element);
});
```

```html
<!-- Tooltip definition -->
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="top" title="{Tooltip message}">{Button text}</button>
```

### &#10022; Placement of tooltip:

*Syntax: add `data-bs-placement="{top|right|bottom|left}"` data attribute to the tooltip.*

```html
<!-- Top placement of tooltip -->
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="top" title="{Tooltip message}">{Button text}</button>

<!-- Right placement of tooltip -->
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="right" title="{Tooltip message}">{Button text}</button>

<!-- Bottom placement of tooltip -->
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="bottom" title="{Tooltip message}">{Button text}</button>

<!-- Left placement of tooltip -->
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-placement="left" title="{Tooltip message}">{Button text}</button>
```

### &#10022; Custom HTML tooltip message:

*Syntax: add `data-bs-html="true"` data attribute to the element.*

```html
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-html="true" title="This is <b>important</b> message">{Button text}</button>
```

### &#10022; Disabled tooltip:

```html
<span class="d-inline-block" tabindex="0" data-bs-toggle="tooltip" title="{Tooltip message}">
  <button class="btn btn-primary" type="button" disabled>{Button text}</button>
</span>
```

### &#10022; Accessing tooltip via JavaScript:
```javascript
// Enabling tooltip
var elementReference = document.getElementById('{tooltip-id}');
var tooltipElement = new bootstrap.Tooltip(elementReference, options);

// Setting options
var tooltipElement = new bootstrap.Tooltip(elementReference, {
  animation: true, // It applies CSS fade animation to the tooltip.
  container: false, // It appends the tooltip to specific elements. If container: 'body' then it will trigger near to the element and it accepts DOM reference to append to it.
  delay: 100, // It adds some delay to the tooltip from toggle. It accepts milli-seconds in number or object in this format delay: {"show" : 100, "hide": 200}.
  html: 'html-code', // It inserts HTML content to the tooltip. To avoid set false.
  placement: 'auto|top|right|bottom|left', // Or it can accepts function to determine the placement.
  selector: false, // If selector is specified then it will be delegated to it.
  template: 'tooltip-html-code', // To modify default tooltip style with template.
  title: 'tooltip-title', // It sets the title for tooltip or it accepts DOM reference or function.
  trigger: 'hover|click|focus|manual', // It sets the trigger event for tooltip and multiple event can be attached by space separated.
  fallbackPlacements: ['top', 'right', 'bottom', 'left'], // defines fallback placements in an array.
  boundary: 'clippingParents', // It sets overflow constraint boundary of tooltip. By default, it is 'clippingParents' and accepts DOM reference.
  customClass: 'class-name', // It adds custom CSS classes to the tooltip with space separated.
  sanitize: true, // It sanitizes the title and content if the template is given.
  allowList: object, // It sets allowed attribute and tags for tooltip.
  sanitizeFn: null, // To define custom sanitize function or to set null for it.
  offset: [10, 20], // It sets offset for tooltip and it accepts string or array or function.
  popperConfig: null // It overwrites the bootstrap default configuration for popper. It accepts null or object or function.
});
```

### &#10022; Methods to control tooltip via JavaScript:
- `show()` - It makes the tooltip to be visible.
- `hide()` - It makes the tooltip to be hidden.
- `toggle()` - It toggles the state of the tooltip either show or hide.
- `dispose()` - It removes tooltip from DOM tree.
- `enable()` - It enables tooltip for the element. By default it is enabled if defined.
- `disable()` - It removes tooltip ability for the element.
- `toggleEnabled()` - It toggles the tooltip ability for the element if enabled then it disabled and vice versa.
- `update()` - It updates the position of tooltip.
- `getInstance()` - Static method which allows to get the tooltip instance.
- `getOrCreateInstance()` - Static method which returns a tooltip instance or create a new one in case it wasn't initialized yet.

```javascript
var elementReference = document.getElementById('{tooltip-id}');
var tooltipElement = bootstrap.Tooltip.getOrCreateInstance(elementReference);
```

### &#10022; Events related to tooltip:
- `show.bs.tooltip` - It triggers an event when the show instance method is invoked.
- `shown.bs.tooltip` - It triggers an event when the tooltip gets visible to the user.  
- `hide.bs.tooltip` - It triggers an event when the hide instance method is invoked.
- `hidden.bs.tooltip` - It triggers an event when the tooltip gets hidden to the user.  
- `inserted.bs.tooltip` - It triggers an event after the `show.bs.tooltip` event when the tooltip template is added to the DOM.  

```javascript
var elementReference = document.getElementById('{tooltip-id}');
elementReference.addEventListener('show.bs.tooltip', function () { ... });
```

---
[&#8682; To Top](#-tooltips)

[&#10094; Previous Topic](./components.toasts.md) &emsp; [Next Topic &#10095;](./bootstrap-helpers.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)