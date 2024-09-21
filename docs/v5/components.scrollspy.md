## &#10162; Scrollspy:
Bootstrap can update active state for navigation links and list group items based on the current active in the page using spying on scroll behavior.

*Syntax:*
  - It works on [navs and tabs](./components.navs-and-tabs.md) and [list group](./components.list-group.md) components.
  - It can spying on the element with `position:relative;` only.
  - It requires [`<a>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/a-tag.md) tag with pointing to the element of their id.

```html
<!-- Navbar definition -->
<nav id="{navbar-id}" class="navbar navbar-light bg-light">
  <a class="navbar-brand" href="#">{Brand name}</a>
  <ul class="nav nav-pills">
    <li class="nav-item">
      <a class="nav-link" href="#{section-id}">{Section name}</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#{section-id}">{Section name}</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" href="#{section-id}">{Section name}</a>
    </li>
  </ul>
</nav>

<!-- Scrollspy Initiation -->
<div data-bs-spy="scroll" data-bs-target="#{navbar-id}" data-bs-offset="0">
  <div id="{section-id}">...</div>
  <div id="{section-id}">...</div>
  <div id="{section-id}">...</div>
</div>
```

### &#10022; Scrollspy with list group:

```html
<!-- List group definition -->
<div id="{list-group-id}" class="list-group">
  <a class="list-group-item list-group-item-action" href="#{section-id}">{Section name}</a>
  <a class="list-group-item list-group-item-action" href="#{section-id}">{Section name}</a>
  <a class="list-group-item list-group-item-action" href="#{section-id}">{Section name}</a>
</div>

<!-- Scrollspy Initiation -->
<div data-bs-spy="scroll" data-bs-target="#{navbar-id}" data-bs-offset="0">
  <div id="{section-id}">...</div>
  <div id="{section-id}">...</div>
  <div id="{section-id}">...</div>
</div>
```

### &#10022; Accessing scrollspy via JavaScript:
```javascript
// Enabling scrollspy
var scrollSpy = new bootstrap.ScrollSpy(document.body, {
  target: '#{navbar-id}'
});

// Setting options
var scrollspy = new bootstrap.ScrollSpy(document.body, {
  target: '{element-reference}', // It applies scrollspy on targeted element and accepts string, DOM reference or jQuery object.
  offset: 5, // It add offset for calculating top position of the element when scroll.
  method: 'auto' // If it specified as 'auto' then it apply best method to get position of the element. or it is 'offset' then it will uses  Element.getBoundingClientRect() method for calculating position or it is 'position' then it will uses HTMLElement.offsetTop and HTMLElement.offsetLeft properties to get position of the element.
});
```

### &#10022; Events related to scrollspy:
- `activate.bs.scrollspy` - It triggers an event whenever the new item activated by scrollspy.
  
```javascript
var scrollspyElement = document.querySelector('[data-bs-spy="scroll"]');
scrollspyElement.addEventListener('activate.bs.scrollspy', function () { ... });
```

---
[&#8682; To Top](#-scrollspy)

[&#10094; Previous Topic](./components.progress-bars.md) &emsp; [Next Topic &#10095;](./components.spinners.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)