## &#10022; Dropdowns:
Dropdowns are list, that are toggle-able to overlay on next parent to display links or list items.

*Syntax:*
  - add `.dropdown` class to container
  - add `.dropdown-toggle` class to the button to toggle the container
  - add `.dropdown-menu` class to the toggle-able container

```html
<div class="dropdown">
  <button class="btn btn-primary dropdown-toggle" type="button" id="{button-id}" data-bs-toggle="dropdown" aria-expanded="false">{Button Text}</button>
  <ul class="dropdown-menu" aria-labelledby="{button-id}">
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
  </ul>
</div>
```

- Split button dropdown toggle by button group:
  *Add `.dropdown-toggle-split` class to the `.dropdown-toggle` class.*

```html
<div class="btn-group">
  <button type="button" class="btn btn-primary">{Button Text}</button>
  <button type="button" class="btn btn-primary dropdown-toggle dropdown-toggle-split" data-bs-toggle="dropdown" aria-expanded="false">
    <span class="visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
  </ul>
</div>
```

- Dropdown divider:
```html
<li><hr class="dropdown-divider"></li>
``` 

- Dark Dropdown:
```html
<div class="dropdown">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="{button-id}" data-bs-toggle="dropdown" aria-expanded="false">{Button Text}</button>
  <ul class="dropdown-menu dropdown-menu-dark" aria-labelledby="{button-id}">
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
  </ul>
</div>
```

- Navigation Dropdown:
  *Add dropdown with `.nav-item` class to implement dropdown in navigation menu.*

```html
<li class="nav-item dropdown">
  <a class="nav-link dropdown-toggle" href="#" id="{nav-item-button-id}" role="button" data-bs-toggle="dropdown" aria-expanded="false">{Nav Button Text}</a>
  <ul class="dropdown-menu" aria-labelledby="{nav-item-button-id}">
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
    <li><a class="dropdown-item" href="#">{link or list item}</a></li>
  </ul>
</li>
```

- Drop up direction dropdown:
  *Add `.dropup` class to the `.btn-group` class wrapper.*
```html
<div class="btn-group dropup">
  ...
</div>
```

- Drop Right direction dropdown:
  *Add `.dropend` class to the `.btn-group` class wrapper.*
```html
<div class="btn-group dropend">
  ...
</div>
```

- Drop Left direction dropdown:
  *Add `.dropstart` class to the `.btn-group` class wrapper.*
```html
<div class="btn-group dropstart">
  ...
</div>
```

- Active dropdown item:
  *Add `.active` class to the `.dropdown-item` class.*
```html
<ul class="dropdown-menu">
  ...
  <li><a class="dropdown-item active" href="#" aria-current="true">{link or list item}</a></li>
  ...
</ul>
```

- Disabled dropdown item:
  *Add `.disabled` class to the `.dropdown-item` class.*
```html
<ul class="dropdown-menu">
  ...
  <li><a class="dropdown-item disabled" href="#" tabindex="-1" aria-disabled="true">{link or list item}</a></li>
  ...
</ul>
```

- Dropdown menu alignment:
  *Add `.dropdown-menu-end` class to the `.dropdown-menu` class for right alignment. But default is left alignment to force left alignment `.dropdown-menu-start` class. This direction is mirrored when RTL usage.*
```html
<ul class="dropdown-menu dropdown-menu-end">
  ...
  ...
  ...
</ul>
```

- Responsive dropdown menu alignment:
  *Disable dynamic positioning by adding `data-bs-display="static"` to the dropdown button and Add `.dropdown-menu-{sm|md|lg|xl|xxl}-end` classes for different screen sizes.*

```html
<!-- Dropdown menu will be right aligned when large screen. Actually it will left aligned when small screens -->
<ul class="dropdown-menu dropdown-menu-lg-end">
  ...
  ...
  ...
</ul>
```

- Dropdown offset:
  *Add `data-bs-offset="{skidding},{distance}"` attribute to the dropdown button. That will apply offset to the dropdown menu.*
```html
<button type="button" class="btn btn-primary dropdown-toggle" id="{button-id}" data-bs-toggle="dropdown" aria-expanded="false" data-bs-offset="5,25">{Button Text}</button>
```

- Autoclose dropdown:
  - Add `data-bs-auto-close="{value}"` attribute to the dropdown button. 
  - If the value is `true`, then the dropdown menu close by clicking the list item or outside the menu. 
  - If the value is `false`, then it will not close until click that toggle again.
  - If the value is `inside`, then it will close when click inside the menu or toggle the button.
  - If the value is `outside`, then it will close when click outside the menu or toggle the button.
```html
<button class="btn btn-primary dropdown-toggle" type="button" id="{button-id}" data-bs-toggle="dropdown" data-bs-auto-close="true" aria-expanded="false">{Button Text}</button>
```

- Accessing dropdown via JavaScript:
```javascript
var dropdownElements = [].slice.call(document.querySelectorAll('.dropdown-toggle'));
var dropdownList = dropdownElements.map(function (element) {
  return new bootstrap.Dropdown(element);
});
```

- Add options to dropdown via JavaScript:
```javascript
var dropdownReference = document.querySelector('#{dropdown-id}');
var dropdown = new bootstrap.Carousel(dropdownReference, {
  boundary: 'clippingParents', // which sets boundary of dropdown menu. By default is string value of 'clippingParents' or DOM reference.
  reference: 'toggle', // which sets the reference element of the dropdown menu. By default is string value of 'toggle' or 'parent' or DOM reference or object that has `getBoundingClientRect`.
  display: 'dynamic', // which sets the position by default as 'dynamic', but it can be set to 'static' positioning.
  offset: [5, 25], // which sets offset for dropdown menu that first argument is skidding value and second is distance value
  autoClose: true, // Which sets autoclose behavior to the dropdown menu. By default is true and other possible values are false, inside, outside.
  popperConfig: null // which sets the default popper configuration. Which accepts null or object or function.
});
```


- Methods to control collapse via JavaScript:
  - `toggle()` - It toggles the given dropdown menu to be either visible or hidden.
  - `show()` - It makes dropdown menu to be visible.
  - `hide()` -  It makes dropdown menu to be hide.  
  - `update()` - It updates position of dropdown menu elements.
  - `dispose()` - It removes dropdown from DOM tree.
  - `getInstance()` - Static method which allows to get the dropdown instance.
  - `getOrCreateInstance()` - Static method which returns a dropdown instance or create a new one in case it wasn't initialized yet.

- Events related to collapse:
  - `show.bs.dropdown` - It triggers an event when the show instance method is invoked.
  - `shown.bs.dropdown` - It triggers an event when the dropdown menu gets visible to the user.  
  - `hide.bs.dropdown` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.dropdown` - It triggers an event when the dropdown menu gets hidden to the user.  

```javascript
var dropdownElement = document.getElementById('{dropdown-id}')
dropdownElement.addEventListener('show.bs.dropdown', function () { ... });
```

---
[&#8682; To Top](#-dropdowns)

[&#10094; Previous Topic](./components.collapse.md) &emsp; [Next Topic &#10095;](./components.forms.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)