## &#10162; Offcanvas:
Create beautiful and responsive sidebar in the webpage using bootstrap offcanvas. It is similar to modal popup boxes but differs in placements.

*Syntax:*
  - `.offcanvas` class to represent the offcanvas container and to be hidden. 
  - `.offcanvas` class with `.show` class to represent the offcanvas to be visible. 
  - `.offcanvas-{start|end|top|bottom}` class to represent the offcanvas placement.
  - `.offcanvas-header` class to represent the header for offcanvas.
  - `.offcanvas-title` class to represent the title for offcanvas.
  - `.offcanvas-body` class to represent the body of the offcanvas.
  - `data-bs-dismiss="offcanvas"` data attribute to close offcanvas.

```html
<!-- Open offcanvas via link with href  -->
<a class="btn btn-primary" data-bs-toggle="offcanvas" href="#{offcanvas-id}" role="button" aria-controls="{offcanvas-id}">{Link text}</a>

<!-- Open offcanvas via button with data attribute -->
<button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#{offcanvas-id}" aria-controls="{offcanvas-id}">{Button text}</button>

<!-- Offcanvas definition -->
<div class="offcanvas offcanvas-start" tabindex="-1" id="{offcanvas-id}" aria-labelledby="{offcanvas label}">
  <!-- Offcanvas header -->
  <div class="offcanvas-header">

    <!-- Offcanvas title -->
    <h5 class="offcanvas-title" id="{offcanvas-title-id}">{Offcanvas title}</h5>
    
    <!-- Offcanvas close button -->
    <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
  </div>

  <!-- Offcanvas body -->
  <div class="offcanvas-body">
    ...
  </div>
</div>
```

### &#10022; Offcanvas body scrolling:

```html
<div class="offcanvas offcanvas-start" data-bs-scroll="true" tabindex="-1" id="{offcanvas-id}" aria-labelledby="{offcanvas-label}">
...
</div>  
```

### &#10022; Offcanvas backdrop:

```html
<div class="offcanvas offcanvas-start" data-bs-backdrop="true" tabindex="-1"  id="{offcanvas-id}" aria-labelledby="{offcanvas-label}">
...
</div>
```

### &#10022; Accessing offcanvas via JavaScript:
```javascript
var offcanvasList = [].slice.call(document.querySelectorAll('.offcanvas'));
var offcanvasElements = offcanvasList.map(function (element) {
  return new bootstrap.Offcanvas(element);
});

var offcanvasReference = document.getElementById('{offcanvas-id}');
var offcanvasElement = new bootstrap.Offcanvas(offcanvasReference, {
  backdrop: true, // Apply a backdrop while offcanvas is open
  keyboard: true, //  Closes the offcanvas when escape key is pressed in the keyboard
  scroll: true // Allows to scroll when offcanvas is open
});
```

### &#10022; Methods to control offcanvas via JavaScript:
- `show()` - It makes the offcanvas to be visible.
- `hide()` - It makes the offcanvas to be hidden.
- `toggle()` - It toggles the state of the offcanvas either show or hide.
- `dispose()` - It removes offcanvas from DOM tree.
- `getInstance()` - Static method which allows to get the offcanvas instance.
- `getOrCreateInstance()` - Static method which returns a offcanvas instance or create a new one in case it wasn't initialized yet.

### &#10022; Events related to offcanvas:
- `show.bs.offcanvas` - It triggers an event when the show instance method is invoked.
- `shown.bs.offcanvas` - It triggers an event when the offcanvas gets visible to the user.  
- `hide.bs.offcanvas` - It triggers an event when the hide instance method is invoked.
- `hidden.bs.offcanvas` - It triggers an event when the offcanvas gets hidden to the user.  

```javascript
var offcanvasReference = document.getElementById('{offcanvas-id}');
offcanvasReference.addEventListener('show.bs.offcanvas', function () { ... });
```

---
[&#8682; To Top](#-offcanvas)

[&#10094; Previous Topic](./components.navs-and-tabs.md) &emsp; [Next Topic &#10095;](./components.pagination.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)