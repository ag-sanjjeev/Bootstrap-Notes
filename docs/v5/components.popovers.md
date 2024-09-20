## &#10022; Popovers:
Create beautiful positioned overlay toast next the elements using bootstrap with popperJs.

```javascript
// Enable popovers with reference to data attribute throughout the webpages
var popverList = [].slice.call(document.querySelectorAll('[data-bs-toggle="popover"]'));
var popoverElements = popoverTriggerList.map(function (element) {
  return new bootstrap.Popover(element);
});

// Enable popovers with DOM reference
let popoverElement = new bootstrap.Popover(document.querySelector('{popover-reference}'), {
  container: 'body'
});
```

*Syntax:*
  - Add `data-bs-toggle="popover"` attribute to the element.
  - Add `title="{title for popover}"` attribute to the element for popover title.
  - Add `data-bs-content="{content}"` attribute to the element for popover message.

```html
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="{Popover title}" data-bs-content="{Popover message}">{Button text}</button>
```

- Direction of popovers:

*Syntax:*
  - `data-bs-placement="{top|right|bottom|left}"` attribute to the element.

```html
<!-- Popover to the top side of the element -->
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="{Popover title}" data-bs-content="{Popover message}" data-bs-placement="top">{Button text}</button>

<!-- Popover to the left side of the element -->
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="{Popover title}" data-bs-content="{Popover message}" data-bs-placement="left">{Button text}</button>

<!-- Popover to the bottom side of the element -->
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="{Popover title}" data-bs-content="{Popover message}" data-bs-placement="bottom">{Button text}</button>

<!-- Popover to the left side of the element -->
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="{Popover title}" data-bs-content="{Popover message}" data-bs-placement="left">{Button text}</button>

```

- Dismiss on click:

*Syntax:* 
  - Use [`<a>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/a-tag.md) tag rather than [`<button>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/button-tag.md) tag.
  - Add `tabindex="{index}"` attribute to the element. 
  - Add `data-bs-trigger="focus"` attribute to the element.

```html
<a role="button" class="btn btn-primary" tabindex="0" data-bs-toggle="popover" data-bs-trigger="focus" title="{Popover title}" data-bs-content="{Popover message}">{Link text}</a>
```

- Disabled popovers:

*Syntax: add `disabled` attribute to popover button.*

```html
<span class="d-inline-block" tabindex="0" data-bs-toggle="popover" data-bs-trigger="hover focus" title="{Popover title}" data-bs-content="{Popover message}">
  <button class="btn btn-primary" type="button" disabled>{Button text}</button>
</span>
```

- Accessing popovers via JavaScript:
```javascript
// Enabling popovers
var elementReference = document.getElementById('{element-id}');
var popoverElement = new bootstrap.Popover(elementReference, options);

// Setting options
var popoverElement = new bootstrap.Popover(elementReference, {
  animation: true, // Setting CSS fade animation when toggles.
  container: false, // It appends the popover to specific elements. If container: 'body' then it will trigger near to the element and it accepts DOM reference to append to it.
  content: 'message', // It sets the content to popover body by setting string or DOM reference or function.
  delay: 100, // It adds some delay to the popover from toggle. It accepts milli-seconds in number or object in this format delay: {"show" : 100, "hide": 200}.
  html: 'html-code', // It inserts HTML content to the popover. To avoid set false.
  placement: 'auto|top|right|bottom|left', // Or it can accepts function to determine the placement.
  selector: false, // If selector is specified then it will be delegated to it.
  template: 'popover-html-code', // To modify default popover style with template.
  title: 'popover-title', // It sets the title for popover or it accepts DOM reference or function.
  trigger: 'hover|click|focus|manual', // It sets the trigger event for popover and multiple event can be attached by space separated.
  fallbackPlacements: ['top', 'right', 'bottom', 'left'], // defines fallback placements in an array.
  boundary: 'clippingParents', // It sets overflow constraint boundary of popover. By default, it is 'clippingParents' and accepts DOM reference.
  customClass: 'class-name', // It adds custom CSS classes to the popover.
  sanitize: true, // It sanitizes the title and content if the template is given.
  allowList: object, // It sets allowed attribute and tags for popover.
  sanitizeFn: null, // To define custom sanitize function or to set null for it.
  offset: [10, 20], // It sets offset for popover and it accepts string or array or function.
  popperConfig: null // It overwrites the bootstrap default configuration for popper. It accepts null or object or function. 
});
```

- Methods to control popover via JavaScript:
  - `show()` - It makes the popover to be visible.
  - `hide()` - It makes the popover to be hidden.
  - `toggle()` - It toggles the state of the popover either show or hide.
  - `dispose()` - It removes popover from DOM tree.
  - `enable()` - It enables popover for the element. By default it is enabled if defined.
  - `disable()` - It removes popover ability for the element.
  - `toggleEnabled()` - It toggles the popover ability for the element if enabled then it disabled and vice versa.
  - `update()` - It updates the position of popover.
  - `getInstance()` - Static method which allows to get the popover instance.
  - `getOrCreateInstance()` - Static method which returns a popover instance or create a new one in case it wasn't initialized yet.

- Events related to popover:
  - `show.bs.popover` - It triggers an event when the show instance method is invoked.
  - `shown.bs.popover` - It triggers an event when the popover gets visible to the user.  
  - `hide.bs.popover` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.popover` - It triggers an event when the popover gets hidden to the user.  
  - `inserted.bs.popover` - It triggers an event after the `show.bs.popover` event when the popover template is added to the DOM.  

```javascript
var popoverElement = document.getElementById('{popover-id}');
popoverElement.addEventListener('show.bs.popover', function (event) { ... });
```


---
[&#8682; To Top](#-popovers)

[&#10094; Previous Topic](./components.pagination.md) &emsp; [Next Topic &#10095;](./components.progress-bars.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)