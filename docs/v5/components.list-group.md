## &#10022; List Group:
Create beautiful list items, series of contents and custom groups of items. Bootstrap offers to create various types of list groups.

*Syntax:* 
	- Add `.list-group` class to the container.
	- Add `.list-group-item` class to the list items.

```html
<ul class="list-group">
  <li class="list-group-item">{List item}</li>  
  <li class="list-group-item">{List item}</li>  
  <li class="list-group-item">{List item}</li>  
</ul>
```

- Active List Items:
To make list item become active using bootstrap class.

*Syntax: add `.active` class to the `.list-group-item` class.*

```html
<ul class="list-group">
  <li class="list-group-item active">{List item}</li>  
  ...
</ul>
```

- Disabled List Items:
To make list item become disabled using bootstrap class.

*Syntax: add `.disabled` class to the `.list-group-item` class.*

```html
<ul class="list-group">
  <li class="list-group-item disabled" aria-disabled="true">{List item}</li>  
  ...
</ul>
```

- Link or Button List Items:
To treat link or button elements as a list item using bootstrap class.

*Syntax: add `.list-group-item-action` class to the `.list-group-item` class.*

```html
<ul class="list-group">
  <a href="{URL/Location}" class="list-group-item list-group-item-action">{List item}</a>
  ...
</ul>
```

- Flush List Items:
To make list item without some borders and rounded corners using bootstrap class.

*Syntax: add `.list-group-flush` class to the `.list-group` class.*

```html
<ul class="list-group list-group-flush">
  <li href="{URL/Location}" class="list-group-item">{List item}</li>
  ...
</ul>
```

- Numbered List Items:
To make list item to be a numbered or ordered list item using bootstrap class.

*Syntax: add `.list-group-numbered` class to the `.list-group` class.*

```html
<ul class="list-group list-group-numbered">
  <li href="{URL/Location}" class="list-group-item">{List item}</li>
  ...
</ul>
```

- Horizontal List Items:
To make list item arranged in horizontal axis using bootstrap class.

*Syntax: add `.list-group-numbered` class to the `.list-group` class.*

```html
<!-- Small sized horizontal list group -->
<ul class="list-group list-group-horizontal-sm">...</ul>

<!-- Default horizontal list group -->
<ul class="list-group list-group-horizontal">...</ul>

<!-- Medium sized horizontal list group -->
<ul class="list-group list-group-horizontal-md">...</ul>

<!-- Large sized horizontal list group -->
<ul class="list-group list-group-horizontal-lg">...</ul>

<!-- Extra Large sized horizontal list group -->
<ul class="list-group list-group-horizontal-xl">...</ul>

<!-- Extra Extra Large sized horizontal list group -->
<ul class="list-group list-group-horizontal-xxl">...</ul>
```

- Colored List Items:
Various colored list item can be created with adding bootstrap classes such as `.list-group-item-{primary|secondary|success|danger|warning|info|light|dark}`.

```html
<ul class="list-group">
	<li class="list-group-item list-group-item-primary">{list item}</li>
</ul>
```

- List group with Tab:
To attach action to the list item for revealing content from respective tabbable panes.

```html
<div class="row">
  <div class="col-4">
    <div class="list-group" id="{list-group-id}" role="tablist">
    	<!-- Active action list item to tab content -->
      <a class="list-group-item list-group-item-action active" id="{list-item-id}" data-bs-toggle="list" href="#{tab-id}" role="tab" aria-controls="{tab-id}">{list item}</a>
      <!-- Inactive action list item to tab content -->
      <a class="list-group-item list-group-item-action" id="{list-item-id}" data-bs-toggle="list" href="#{tab-id}" role="tab" aria-controls="{tab-id}">{list item}</a>
    </div>
  </div>
  <div class="col-8">
    <div class="tab-content" id="{tab-content-id}">
    	<!-- Active tab pane that reference to the list item -->
      <div class="tab-pane fade show active" id="{tab-id}" role="tabpanel" aria-labelledby="{list-item-id}">...</div>
    	<!-- Inactive tab pane that reference to the list item -->
      <div class="tab-pane fade" id="{tab-id}" role="tabpanel" aria-labelledby="{list-item-id}">...</div>      
    </div>
  </div>
</div>

<!-- Need to activate individual tab panes -->
<script type="text/javascript">

var listItems = [].slice.call(document.querySelectorAll('{list-group-id} a'))
listItems.forEach(function (element) {
  let tabReference = new bootstrap.Tab(element);

  tabReference.addEventListener('click', function (event) {
    event.preventDefault();
    tabReference.show();
  });
});
</script>

<!-- Show individual tab panes -->
<script type="text/javascript">
var listItem = document.querySelector('{list-item-id}')
bootstrap.Tab.getInstance(listItem).show();
</script>
```

- List group with Tabs without JavaScript:
It can be attached tabbable panes to the list items with `data-bs-toggle="list"` data attributes and `href="{tab-id}"` attribute.

```html
<div role="tabpanel">
  <!-- List group -->
  <div class="list-group" id="myList" role="tablist">
    <a class="list-group-item list-group-item-action active" data-bs-toggle="list" href="{tab-id}" role="tab">{list item}</a>
    <a class="list-group-item list-group-item-action" data-bs-toggle="list" href="{tab-id}" role="tab">{list item}</a>
    ...
    ...
  </div>

  <!-- Tab panes -->
  <div class="tab-content">
    <div class="tab-pane active" id="{tab-id}" role="tabpanel">...</div>
    <div class="tab-pane" id="{tab-id}" role="tabpanel">...</div>
    ...
    ...
  </div>
</div>
```

- Accessing list group via JavaScript:
```javascript
var listItemElements = [].slice.call(document.querySelectorAll('{list-group-id} a'));
var listItems = listItemElements.map(function (element) {
  return new bootstrap.Tab(element);
});
```

- Methods to control tabbable panes via JavaScript:
  - `show()` - It makes tabbable panes to be visible.
  - `dispose()` - It removes tabbable panes from DOM tree.
  - `getInstance()` - Static method which allows to get the tabbable panes instance.
  - `getOrCreateInstance()` - Static method which returns a tabbable panes instance or create a new one in case it wasn't initialized yet.

- Events related to tabbable panes:
  - `show.bs.tab` - It triggers an event when the show instance method is invoked.
  - `shown.bs.tab` - It triggers an event when the tabbable pane gets visible to the user.  
  - `hide.bs.tab` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.tab` - It triggers an event when the tabbable pane gets hidden to the user.  

```javascript
var listItemElements = document.querySelectorAll('{list-group-id} a');
listItemElements.forEach(function(element) {
  element.addEventListener('shown.bs.tab', function (event) {
    event.target // new active tab
    event.relatedTarget // previously activated tab
  });
}
```

---
[&#8682; To Top](#-list-group)

[&#10094; Previous Topic](./components.forms.md) &emsp; [Next Topic &#10095;](./components.modals.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)