## &#10162; Components:

### &#9780; Overview:
1. [Accordion](#-accordion)
2. [Alerts](#-alerts)
3. [Badge](#-badge)
4. [Breadcrumb](#-breadcrumb)
5. [Buttons](#-buttons)
6. [Button group](#-button-group)
7. [Close button](#-close-button)
8. [Cards](#-cards)
9. [Carousel](#-carousel)
10. [Collapse](#-collapse)
11. [Dropdowns](#-dropdowns)
12. [Forms](#-forms)
    - [Overview](#-overview)
    - [Form control](#-form-control)
    - [Select](#-select)
    - [Checkboxs and Radios](#-checkboxs-and-radios)
    - [Range](#-range)
    - [Input group](#-input-group)
    - [Floating labels](#-floating-labels)
    - [Layout](#-layout)
    - [Validation](#-validation)
13. [List group](#-list-group)
14. [Modals](#-modals)
15. [Navbar](#-navbar)
16. [Navs and tabs](#-navs-and-tabs)
17. [Offcanvas](#-offcanvas)
18. [Pagination](#-pagination)
19. [Popovers](#-popovers)
20. [Progress bars](#-progress-bars)
21. [Scrollspy](#-scrollspy)
22. [Spinners](#-spinners)
23. [Toasts](#-toasts)
24. [Tooltips](#-tooltips)

### &#10022; Accordion:
It is easy to create a collapsible component that allows users to expand or collapse sections of content using bootstrap.

*Syntax:*
```html
<!-- Accordion Wrapper -->
<div class="accordion" id="{accordion-id-name}">
...
</div>

<!-- Accordion Wrapper Contains Accordion Items -->
<div class="accordion-item">
...
</div>

<!-- Each Accordion Items should have Accordion Heading and Collapse container-->
<h2 class="accordion-header" id="{heading-id}"> ... </h2>

<div id="{collapse-id}" class="accordion-collapse collapse" aria-labelledby="{heading-id}" data-bs-parent="#{accordion-id-name}"> ... </div>
      

<!-- Each Accordion Heading should have Title as Collapsible Button. That button targets the data-bs-target attribute value reference -->
<button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#{collapse-id}" aria-expanded="false" aria-controls="{collapse-id}">
  {Accordion Heading}
</button>

<!-- Each Accordion Collapse Content should have Accordion Body -->
<div class="accordion-body"> ... </div>
```

To make content of accordion is expanded by made these changes.
```html
<!-- Made Changes in button -->
<button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#{collapse-id}" aria-expanded="true" aria-controls="{collapse-id}">
  {Accordion Heading}
</button>

<!-- Made Changes in Collapse Container -->
<div id="{collapse-id}" class="accordion-collapse collapse show" aria-labelledby="{heading-id}" data-bs-parent="#accordionExample">
...
</div>
```

```html
<div class="accordion" id="accordion">
  <!-- Accordion Item 1 -->
  <div class="accordion-item">
    <h2 class="accordion-header" id="heading1">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapse1" aria-expanded="true" aria-controls="collapse1">
        {Accordion Heading 1}
      </button>
    </h2>
    <div id="collapse1" class="accordion-collapse collapse show" aria-labelledby="heading1" data-bs-parent="#accordion">
      <div class="accordion-body">...</div>
    </div>
  </div>

  <!-- Accordion Item 2 -->
  <!-- Same as everything in Item 1. But changes in button and accordion body -->
  <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapse2" aria-expanded="false" aria-controls="collapse2">
    {Accordion Heading 2}
  </button>
  ...
  <div id="collapse2" class="accordion-collapse collapse" aria-labelledby="heading2" data-bs-parent="#accordion">
    <div class="accordion-body">...</div>
  </div>
```

- Flush Accordion:
To remove the default background-color, some borders, and some rounded borders. By adding `.accordion-flush` class to the `.accordion` classs.

*Syntax:*
```html
<div class="accordion accordion-flush" id="{accordion-id-name}">
...
</div>
```

---

### &#10022; Alerts:
It is a alternative and replacement for native browser alert boxes using bootstrap.

*Syntax:*
```html
<div class="alert alert-{color-scheme}" role="alert">
  {Alert Content}
</div>
```

- The color schemes for alert boxes are `.alert-primary`, `.alert-secondary`, `.alert-success`, `.alert-danger`, `.alert-warning`, `.alert-info`, `.alert-light`, `.alert-dark`.

```html
<div class="alert alert-primary" role="alert">
  {Alert Content}
</div>
```

- To add links in the alert boxes rather than the traditional links.
```html
<div class="alert alert-primary" role="alert">
  ... <a href="#" class="alert-link">an example link</a> ...
</div>
```

- To add alert heading with additional content.
```html
<div class="alert alert-danger" role="alert">
  <h4 class="alert-heading">{Alert Heading}</h4>
  <p>{additional content }</p>
</div>
```

- To add icons to the alert boxes.
```html
<div class="alert alert-danger" role="alert">
  <h4 class="alert-heading"> {icon} {Alert Heading}</h4>
  <p>{additional content }</p>
</div>
```

- To create dismissing alert boxes with some transitions. Make sure that bootstrap JavaScript plugin is linked.
```html
<div class="alert alert-danger alert-dismissible fade show" role="alert">
  {content}
  <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
</div>
```

- Methods related to alerts
To create an alert instance with the alert constructor.
```javascript
var alertReference = document.getElementById('alert-id');
var bsAlert = new bootstrap.Alert(alertReference);

bsAlert.close(); // Closes an alert by removing it from the DOM
bsAlert.dispose(); // Destroys an element's alert. (Removes from the DOM tree)

bsAlert = bootstrap.Alert.getInstance(alertReference); // to get alert instance
bsAlert.close(); 

bsAlert = bootstrap.Alert.getOrCreateInstance(alertReference); // get alert object or create instance if not created yet
```

- Events related Alerts
To get events of alerts such as close and closed events.
```javascript
// close.bs.alert - It triggers immediately when the close instance method is called.
// closed.bs.alert - It triggers when the alert has been closed and transitions have completed.
var alertReference = document.getElementById('alert-id');
alertReference.addEventListener('closed.bs.alert', function () {
  ...
});
```

---

### &#10022; Badge:
Create beautiful label element that looks like rectangle rounded badge. Bootstrap offers to create various types of badge.

*Syntax: add `.badge` class to the element*

```html
<span class="badge bg-primary">{Label Content}</span>
```

- Various badges can be created with adding background classes such as `bg-primary, bg-secondary, bg-success, bg-danger, bg-warning, bg-info, bg-light, bg-dark`.

- Create rounded pills with badge by adding `.rounded-pill` class.
```html
<span class="badge rounded-pill bg-success">{Label Content}</span>
```

---

### &#10022; Breadcrumb:
Breadcrumbs are used for indicating navigation tree or order or the page, Where you are in the current page. Bootstrap makes Breadcrumb looks rich and nice.

*Syntax: add `.breadcrumb` class*

```html
<nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Blog</a></li>
    <li class="breadcrumb-item active" aria-current="page">Article Name</li>
  </ol>
</nav>
``` 

- To add custom dividers for breadcrumbs
```html
<nav style="--bs-breadcrumb-divider: '>';" aria-label="breadcrumb">
  <ol class="breadcrumb">
    ...
  </ol>
</nav>
```

---

### &#10022; Buttons:
Bootstrap can make buttons that looks beautiful and nice.

*Syntax: add `.btn` class*
```html
<button type="{...}" class="btn btn-primary">{Button Text}</button>
```

- To create different buttons by adding `btn-primary, btn-secondary, btn-success, btn-danger, btn-warning, btn-info, btn-light, btn-dark` classes.

- To style button as anchor link.
```html
<button type="button" class="btn btn-link">Link</button>
```

- To create outline based buttons by adding `btn-outline-primary, btn-outline-secondary, btn-outline-success, btn-outline-danger, btn-outline-warning, btn-outline-info, btn-outline-light, btn-outline-dark` classes.

```html
<button type="button" class="btn btn-outline-primary">{Button Text}</button>
```

- To make buttons as larger in size by adding `.btn-lg` class with `.btn` class.
```html
<button type="button" class="btn btn-primary btn-lg">{Button Text}</button>
```

- To make buttons as smaller in size by adding `.btn-sm` class with `.btn` class. 
```html
<button type="button" class="btn btn-primary btn-sm">{Button Text}</button>
```

- To make buttons as disabled stage by adding attribute `disabled` or class `.disabled` to the button. And additionally set tabindex and ARIA attribute.
```html
<button type="button" class="btn btn-primary" disabled>{Button Text}</button>
<button type="button" class="btn btn-primary disabled">{Button Text}</button>

<!-- ARIA Attribute and Tabindex -->

<button type="button" class="btn btn-primary disabled" tabindex="-1" role="button" aria-disabled="true">{Button Text}</button>
```

- To make button being in active state by adding `.active` class.
```html
<button type="button" class="btn btn-primary active">{Button Text}</button>
```

- Methods related buttons:
  - `toggle()` -  Toggles push state. That makes button to be appeared as being active.
  - `dispose()` - Destroys a button element. (Removes from the DOM tree).
  - `getInstance()` -  Static method which allows to get the button instance.
  - `getOrCreateInstance()` Static method which returns a button instance or create a new one in case it wasn't initialized yet.
```javascript
var button = document.getElementById('{button-id}')
var bsButton = new bootstrap.Button(button);
bsButton.toggle();
```

---

### &#10022; Button Group:
Bootstrap can make series of buttons as group.

*Syntax: add `.btn-group` class*
```html
<div class="btn-group" role="group" aria-label="{Button Group Label}">
  <button type="button" class="btn btn-primary">{Button Text}</button>
  <button type="button" class="btn btn-primary">{Button Text}</button>
  <button type="button" class="btn btn-primary">{Button Text}</button>
</div>
```

- To make buttons as larger in size in the group by adding `.btn-group-lg` class to the `.btn-group` class.
```html
<div class="btn-group btn-group-lg" role="group" aria-label="...">...</div>
```

- To make buttons as smaller in size in the group by adding `.btn-group-sm` class to the `.btn-group` class.
```html
<div class="btn-group btn-group-sm" role="group" aria-label="...">...</div>
```

- To make buttons are stacked vertically in the button group by adding `.btn-group-vertical` class.
```html
<div class="btn-group-vertical">...</div>
```

---

### &#10022; Close Button:
Bootstrap can make button to be treated as close button for alerts, models and etc.,

*Syntax: add `.btn-close` class*
```html
<button type="button" class="btn-close" aria-label="Close"></button>
```

- Disabled Close Button:
```html
<button type="button" class="btn-close" aria-label="Close" disabled></button>
```

- White Colored Close Button for Dark Background:
```html
<button type="button" class="btn-close btn-close-white" aria-label="Close"></button>
```

---

### &#10022; Cards:
Card means the container for the group of elements to make their looks like real world card shapes.

*Syntax: add `.card` class*
```html
<div class="card">...</div>
```

**Associated classes and card elements:**
- Card Header:
```html
<div class="card-header">...</div>
```
- Card Title:
```html
<h3 class="card-title">...</h3>
```

- Card Body:
```html
<div class="card-body">...</div>
```

- Card Text:
```html
<p class="card-text">...</p>
```

- Card Footer:
```html
<div class="card-footer">...</div>
```

- Card Link:
```html
<a href="#" class="card-link">...</a>
```

- Card Image Top:
```html
<img src="..." class="card-img-top" alt="...">
```

- Card Image Bottom:
```html
<img src="..." class="card-img-bottom" alt="...">
```

- Card Image Overlay:
```html
<div class="card-img-overlay" style="background: url(...)">
  <h5 class="card-title">...</h5>
  <p class="card-text">...</p>
  <a href="#" class="card-link">...</a>
</div>
```

- Card Group:
```html
<div class="card-group">...</div>
```

- Change Background color of card with bootstrap background classes.
```html
<div class="card bg-primary">...</div>
```

- Change Border color of card with bootstrap border classes.
```html
<div class="card border-primary">...</div>
```

---
[&#8682; To Top](#-components)

[&#10094; Previous Topic](./bootstrap-content.md) &emsp; [Next Topic &#10095;](./bootstrap-helpers.md)

[&#8962; Goto Home Page](../../README.md)