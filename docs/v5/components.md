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
[&#8682; To Top](#-components)

[&#10094; Previous Topic](./bootstrap-content.md) &emsp; [Next Topic &#10095;](./bootstrap-helpers.md)

[&#8962; Goto Home Page](../../README.md)