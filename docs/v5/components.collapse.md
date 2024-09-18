## &#10022; Collapse:
Collapse means toggle the content to be visible or hidden by collapsing the container.

*Syntax:*
  - add `.collapse` class to define
  - The container has `.collapsing` class defines it in transition state
  - The container has `.collapse.show` classes defines to show the content.

This collapsible content can be toggled by two way:
  - Anchor Tag with `href`
  - Button with `data-bs-target`

**Collapse Controls:**
```html
<a class="btn btn-primary" data-bs-toggle="collapse" href="#{collapse-id}" role="button" aria-expanded="false" aria-controls="{collapse-id}">{Button Text}</a>
```
```html
<button class="btn btn-primary" type="button" data-bs-toggle="collapse" data-bs-target="#{collapse-id}" aria-expanded="false" aria-controls="{collapse-id}">{Button Text}</button>
```
**Collapse Target:**
```html
<div class="collapse" id="{collapse-id}">...</div>
```

*Multiple Collapse Control can target a single collapse content to toggle.*

- Accessing collapse via JavaScript::
```javascript
var collapseElements = [].slice.call(document.querySelectorAll('.collapse'));
var collapseList = collapseElements.map(function (element) {
  return new bootstrap.Collapse(element);
});
```

- Add options to collapse via JavaScript:
```javascript
var collapseElement = document.getElementById('{collapse-id}')
var collapseObject = new bootstrap.Collapse(collapseElement, {
  parent: false, // If it specified with DOM reference that will mimic as accordion collapse that hides if the parent has shown another collapse. If it false that default toggle option enabled
  toggle: false // It will toggles the element on invocation based on boolean value
});
```

- Methods to control collapse via JavaScript:
  - `toggle()` - It makes collapse to be either visible or hidden.
  - `show()` - It makes collapse content to be visible.
  - `hide()` -  It makes collapse content to be hide.  
  - `dispose()` - It removes collapse from DOM tree.
  - `getInstance()` - Static method which allows to get the collapse instance.
  - `getOrCreateInstance()` - Static method which returns a collapse instance or create a new one in case it wasn't initialized yet.

- Events related to collapse:
  - `show.bs.collapse` - It triggers an event when the show instance method is invoked.
  - `shown.bs.collapse` - It triggers an event when the collapse content gets visible to the user.  - `hide.bs.collapse` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.collapse` - It triggers an event when the collapse content gets hidden to the user.  

```javascript
var collapseElement = document.getElementById('{collapse-id}')
collapseElement.addEventListener('show.bs.collapse', function () { ... });
```

---
[&#8682; To Top](#-collapse)

[&#10094; Previous Topic](./components.carousel.md) &emsp; [Next Topic &#10095;](./components.dropdowns.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)