## &#10162; Accordion:
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

### &#10022; Accordion Expand:
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

### &#10022; Flush Accordion:
To remove the default background-color, some borders, and some rounded borders. By adding `.accordion-flush` class to the `.accordion` classs.

*Syntax:*
```html
<div class="accordion accordion-flush" id="{accordion-id-name}">
...
</div>
```

---
[&#8682; To Top](#-accordion)

[&#10094; Previous Topic](./components.md) &emsp; [Next Topic &#10095;](./components.alerts.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)