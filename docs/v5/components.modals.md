## &#10022; Modals:
Create beautiful popup modal dialog boxes using bootstrap classes.
- When modal popup dialog box appears in the page. That is placed over everything. 
- Then, bootstrap removes scroll property for the body and applied scroll property to modal boxes. 
- Clicking close button or clicking on backdrop to close modal boxes.
- Bootstrap displays only one modal box at a time.
- This modal boxes positioned as fixed. To focus elements inside modal boxes is done by JavaScript.

```javascript
// To focus elements inside modal boxes
var modalReference = document.getElementById('{modal-id}');
var inputReference = document.getElementById('{input-id}');

modalReference.addEventListener('shown.bs.modal', function () {
  inputReference.focus();
});
```

*Syntax:* 
- Add `.modal` class to the modal container with initial tab index as `-1`.
- Create modal box with `.modal-dialog` class inside modal container.
- Create content area with `.modal-content` class inside `.modal-dialog` class modal box. Which holds all content of the modal.
- Modal boxes may have header. It can be created with `.modal-header` class.
- Modal title created with `.modal-title` class inside modal header.
- Modal close button added inside modal header with `.btn-close` class with `data-bs-dismiss="modal"` data attribute.
- Modal should have a body. That can be created with `.modal-body` class.
- Modal may have footer. That can be created with `.modal-footer` class. That footer mostly used for modal related actions such as save, reset or modal close.

```html
<!-- Modal Definition -->
<div class="modal" tabindex="-1" id="{modal-id}" aria-labelledby="{modal-label}" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">{Modal title}</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">...</div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary">{Button Text}</button>
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">{Button Text}</button>
      </div>
    </div>
  </div>
</div>

<!-- Modal Trigger -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#{modal-id}">{Button Text}</button>
```

- Static backdrop modal:

To make modal should not close when clicking backdrop by setting backdrop to `static`. 

*Syntax: add `data-bs-backdrop="static"` and `data-bs-keyboard="false"` data attributes to the `.modal` class.*
 
```html
<!-- Modal Definition -->
<div class="modal" tabindex="-1" id="{modal-id}" data-bs-backdrop="static" data-bs-keyboard="false" aria-labelledby="{modal-label}" aria-hidden="true">
  ...
</div>

<!-- Modal Trigger -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#{modal-id}">{Button Text}</button>
```

- Long modal boxes:

To make modal popup box as long to fit all content and scroll by completely through modal dialog box.

*Syntax: add `.modal-dialog` class instead of the `.modal` class.*

```html
<!-- Modal Definition -->
<div class="modal-dialog" tabindex="-1" id="{modal-id}" data-bs-backdrop="static" data-bs-keyboard="false" aria-labelledby="{modal-label}" aria-hidden="true">
  ...
</div>
```

- Scrollable long modal boxes:
To make modal popup boxes are to fit inside the page. But it has long content that make scrollable modal body alone.

*Syntax: add `.modal-dialog-scrollable` class to the `.modal-dialog` class.*

```html
<!-- Modal Definition -->
<div class="modal-dialog modal-dialog-scrollable">
  ...
</div>
```

- Vertically centered modal boxes:
To appears modal popup boxes are centered in vertical axis.

*Syntax: add `.modal-dialog-centered` class to the `.modal-dialog` class.*

```html
<!-- Modal Definition -->
<div class="modal-dialog modal-dialog-centered">
  ...
</div>
```

- Toggle between modals:
View modals dialog boxes between one after another by referring target to the modal box.

```html
<!-- Modal 1 Definition -->
<div class="modal fade" id="{first-modal-id}" ...>
  ...
  <button data-bs-target="#{second-modal-id}" ...>...</button>
</div>

<!-- Modal 2 Definition -->
<div class="modal fade" id="{second-modal-id}" ...>
  ...
  <button data-bs-target="#{first-modal-id}" ...>...</button>
</div>

<!-- Modal 1 Trigger -->
<button data-bs-target="#{first-modal-id}">...</button>
```

- Add animations:
To add animation when modal dialog boxes appears and disappears in the page.

*Syntax: add `.fade` class to the `.modal` class.*

```html
<!-- Modal Definition -->
<div class="modal fade" tabindex="-1" id="{modal-id}" aria-labelledby="{modal-label}" aria-hidden="true">
  ...
</div>

<!-- Modal Trigger -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#{modal-id}">{Button Text}</button>
```

- Sizing of modal dialog boxes:

```html
<!-- Small sized modal dialog box -->
<div class="modal-dialog modal-sm">...</div>

<!-- Large sized modal dialog box -->
<div class="modal-dialog modal-lg">...</div>

<!-- Extra large sized modal dialog box -->
<div class="modal-dialog modal-xl">...</div>
```

- Fullscreen modal dialog boxes:
To make modal dialog boxes to be span across entire page on different screen sizes are met. 
	- `.modal-fullscreen` class makes modal boxes are always in fullscreen.
	- `.modal-fullscreen-sm-down`	class makes modal boxes fullscreen, when screen size below the small screen devices, which is defined in bootstrap.
	- `.modal-fullscreen-md-down`	class makes modal boxes fullscreen, when screen size below the medium screen devices, which is defined in bootstrap.
	- `.modal-fullscreen-lg-down`	class makes modal boxes fullscreen, when screen size below the large screen devices, which is defined in bootstrap.
	- `.modal-fullscreen-xl-down`	class makes modal boxes fullscreen, when screen size below the extra large screen devices, which is defined in bootstrap.
	- `.modal-fullscreen-xxl-down`	class makes modal boxes fullscreen, when screen size below the extra extra large screen devices, which is defined in bootstrap.

```html
<!-- Full screen modal definition -->
<div class="modal-dialog modal-fullscreen-md-down">
  ...
</div>
```

- Accessing modal dialog boxes via JavaScript:
```javascript
var modalReference = new bootstrap.Modal(document.getElementById('{modal-id}'), options);

var modalReference = new bootstrap.Modal(document.getElementById('{modal-id}'), {
	backdrop:	true, // it accepts 'static' or	true value that decides closing of modal boxes by clicking outside.
	keyboard:	true, //	Closes the modal when escape key is pressed in the keyboard
	focus: true	// Sets focus on the modal when appears.
});
```

- Methods to control modal dialog boxes via JavaScript:
	- `handleUpdate()` - Get position of modal boxes to re-adjust it.
  - `show()` - It makes modal dialog boxes to be visible.
  - `show(DOMReference)` - It makes modal dialog boxes to be visible with an argument of DOM reference.
  - `toggle()` - It makes modal dialog boxes to toggle between show and hide.
  - `dispose()` - It removes modal dialog boxes from DOM tree.
  - `getInstance()` - Static method which allows to get the modal dialog boxes instance.
  - `getOrCreateInstance()` - Static method which returns a modal dialog boxes instance or create a new one in case it wasn't initialized yet.

- Events related to modal boxes:
  - `show.bs.tab` - It triggers an event when the show instance method is invoked.
  - `shown.bs.tab` - It triggers an event when the modal boxes gets visible to the user.  
  - `hide.bs.tab` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.tab` - It triggers an event when the modal boxes gets hidden to the user.  
  - `hidePrevented.bs.modal` - It triggers an event when the modal boxes prevented to hide, due to the backdrop static or keyboard escape key.  

```javascript
// showing modal dialog boxes via JavaScript
var modalElement = new bootstrap.Modal(document.getElementById('{modal-id}'));
modalElement.show();

var modalToggle = document.getElementById('{modal-toggle-id}');
modalElement.show(modalToggle);

modalElement.addEventListener('hidden.bs.modal', function (event) {...});
```

---
[&#8682; To Top](#-modals)

[&#10094; Previous Topic](./components.list-group.md) &emsp; [Next Topic &#10095;](./components.navbar.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)