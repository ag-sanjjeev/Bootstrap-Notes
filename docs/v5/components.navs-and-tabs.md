## &#10162; Navs and Tabs:
Create beautiful and responsive navigation and tabbable panes using bootstrap classes.

*Syntax:*
  - `.nav` class to represent the navigation for tabbable panes.
  - `.nav-item` class to represent the navigation item.
  - `.nav-link` class to represent the link item.
  - `.active` class to represent the current or active navigation item.
  - `.disabled` class to represent the disabled navigation item.

```html
<ul class="nav">
  <li class="nav-item">
    <a class="nav-link active" aria-current="page" href="#">{Link item}</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">{Link item}</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">{Link item}</a>
  </li>
</ul>
```
### &#10022; Create navigation menu with navs:

```html
<nav class="nav">  
  <a class="nav-link active" aria-current="page" href="#">{Link item}</a>
  <a class="nav-link" href="#">{Link item}</a>    
  <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">{Link item}</a>  
</nav>
```

### &#10022; Horizontal alignment:

```html
<!-- Center aligned navs -->
<nav class="nav justify-content-center">
...
</nav>

<!-- Right aligned navs -->
<nav class="nav justify-content-end">
...
</nav>
```

### &#10022; Vertical alignment:

```html
<nav class="nav flex-column">
...
</nav>
```

### &#10022; Tabs:

*Syntax: add `.nav-tabs` class to `.nav` class.*

```html
<ul class="nav nav-tabs">
  ...
</ul>
```

### &#10022; Pills:

*Syntax: add `.nav-pills` class to `.nav` class.*

```html
<ul class="nav nav-pills">
  ...
</ul>
```

### &#10022; Fill nav items:

*Syntax: add `.nav-fill` class to `.nav` class.*

```html
<ul class="nav nav-pills nav-fill">
  ...
</ul>
```

### &#10022; Justify nav items:

*Syntax: add `.nav-justified` class to `.nav` class.*

```html
<ul class="nav nav-pills nav-justified">
  ...
</ul>
```

### &#10022; Nav item with dropdown:

```html
<ul class="nav">
  <li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#" role="button" aria-expanded="false">{Link item}</a>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">{Dropdown item}</a></li>
      ...
      ...      
    </ul>
  </li>
</ul>
```

### &#10022; Link nav items to tabbable panes:

```html
<ul class="nav">
  <!-- Active nav link for active tabbable pane -->
  <li class="nav-item">
    <button class="nav-link active" id="{button-id}" data-bs-toggle="tab" data-bs-target="#{tab-id}" type="button" role="tab" aria-controls="{tab-name}" aria-selected="true">{Button text}</button>
  </li>
  <!-- nav link for tabbable pane -->
  <li class="nav-item">
    <button class="nav-link" id="{button-id}" data-bs-toggle="tab" data-bs-target="#{tab-id}" type="button" role="tab" aria-controls="{tab-name}" aria-selected="false">{Button Text}</button>
  </li>
  ....
</ul>
<div class="tab-content" id="{tab-content-id}">
  <!-- Active tabbable pane -->
  <div class="tab-pane fade show active" id="{tab-id}" role="tabpanel" aria-labelledby="{tab-name}">...</div>
  <!-- Tabbable pane -->
  <div class="tab-pane fade" id="{tab-id}" role="tabpanel" aria-labelledby="{tab-name}">...</div>
  ...  
</div>
```

### &#10022; Accessing tabbable panes via JavaScript:
```javascript
var navLinkList = [].slice.call(document.querySelectorAll('{nav-id} a'));
navLinkList.forEach(function (linkItem) {
  var tabPane = new bootstrap.Tab(linkItem);

  linkItem.addEventListener('click', function (event) {
    event.preventDefault();
    linkItem.show();
  });
});
```

### &#10022; Accessing individual tab panes via JavaScript
```javascript
var navLink = document.querySelector('{nav-id} a[href="#{tab-id}"]');
bootstrap.Tab.getInstance(navLink).show();
```

### &#10022; Methods to control tab panes via JavaScript:
- `show()` - It makes the associated tabbable panes to be visible.
- `dispose()` - It removes tabbable panes from DOM tree.
- `getInstance()` - Static method which allows to get the tabbable pane instance.
- `getOrCreateInstance()` - Static method which returns a tabbable pane instance or create a new one in case it wasn't initialized yet.

### &#10022; Events related to modal boxes:
- `show.bs.tab` - It triggers an event when the show instance method is invoked.
- `shown.bs.tab` - It triggers an event when the tabbable pane gets visible to the user.  
- `hide.bs.tab` - It triggers an event when the hide instance method is invoked.
- `hidden.bs.tab` - It triggers an event when the tabbable pane gets hidden to the user.  

```javascript
var navLink = document.querySelector('{nav-id} a');
navLink.addEventListener('shown.bs.tab', function (event) {
  event.target // new active tab
  event.relatedTarget // previously activated tab
});
```

---
[&#8682; To Top](#-navs-and-tabs)

[&#10094; Previous Topic](./components.navbar.md) &emsp; [Next Topic &#10095;](./components.offcanvas.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)