## &#10022; Alerts:
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
[&#8682; To Top](#-alerts)

[&#10094; Previous Topic](./components.accordion.md) &emsp; [Next Topic &#10095;](./components.badge.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)