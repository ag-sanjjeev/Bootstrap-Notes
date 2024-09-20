## &#10022; Toasts:
Bootstrap can create push notification with toast.

*Syntax:*
  - Toast must be initialized before utilize.
  - Toast will be auto hide, to avoid need to specify `autohide:false`.
  - `.toast` class will represent the container as toast message.
  - `.toast-header` class will represent the header of toast.
  - `.toast-body` class will represent the body of toast.

```html
<!-- Toast definition -->
<div class="toast" role="alert" aria-live="assertive" aria-atomic="true">
  <!-- Toast header -->
  <div class="toast-header">
    <!-- Toast title -->
    <strong class="me-auto">{Title}</strong>    
    <!-- Toast close button -->
    <button type="button" class="btn-close" data-bs-dismiss="toast" aria-label="Close"></button>
  </div>
  <!-- Toast body -->
  <div class="toast-body">...</div>
</div>
```

- Toast stacking:

*Syntax: toasts are stacked by wrapper with `.toast-container` class.*

```html
<!-- Toast Container -->
<div class="toast-container">
  <!-- Toasts -->
  <div class="toast">...</div>
  <div class="toast">...</div>
</div>
```

- Colored toasts:

*Syntax: add `.bg-{primary|secondary|success|warning|danger|info}` background color classes.*

```html
<!-- Primary colored toast -->
<div class="toast bg-primary text-light">...</div>
```

- Avoid auto hide toasts:

*Syntax: add `data-bs-autohide="false"` attribute to `.toast` class.*

```html
<!-- Primary colored toast -->
<div class="toast" data-bs-autohide="false">...</div>
```

- Accessing toast via JavaScript:
```javascript
// Enabling toast
var toastList = [].slice.call(document.querySelectorAll('.toast'));
var toastElementList = toastElList.map(function (element) {
  return new bootstrap.Toast(element, option);
});

// Setting options
var toastReference = document.getElementById('{toast-id}');
var toastElement = new bootstrap.Toast(toastReference, {
  animation: true, // It applies CSS fade animation to the toast.
  autohide: false, // It decides auto hide of the toast.
  dealy: 10000 // It decides delay for hide toast
});
```

- Methods to control toast via JavaScript:
  - `show()` - It makes the toast to be visible.
  - `hide()` - It makes the toast to be hidden.
  - `dispose()` - It removes toast from DOM tree.  
  - `getInstance()` - Static method which allows to get the toast instance.
  - `getOrCreateInstance()` - Static method which returns a toast instance or create a new one in case it wasn't initialized yet.

```javascript
var toastReference = document.getElementById('{toast-id}');
var toastElement = bootstrap.Toast.getOrCreateInstance(toastReference);
```

- Events related to scrollspy:
  - `show.bs.toast` - It triggers an event when the show instance method is invoked.
  - `shown.bs.toast` - It triggers an event when the toast gets visible to the user.  
  - `hide.bs.toast` - It triggers an event when the hide instance method is invoked.
  - `hidden.bs.toast` - It triggers an event when the toast gets hidden to the user.  

```javascript
var toastReference = document.getElementById('{toast-id}');
toastElement.addEventListener('show.bs.toast', function () { ... });
```

---
[&#8682; To Top](#-toasts)

[&#10094; Previous Topic](./components.spinners.md) &emsp; [Next Topic &#10095;](./components.tooltips.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)