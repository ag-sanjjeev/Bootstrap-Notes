## &#10162; Forms:
Create beautiful forms with form element that looks rich and for better user interaction. Bootstrap offers to create various form elements.

### &#9780; Overview:
1. [Form control](#-form-control)
2. [Form Text](#-form-text)
3. [Select](#-select)
4. [Checkboxes and Radios](#-checkboxes-and-radios)
5. [Range](#-range)
6. [Input group](#-input-group)
7. [Floating labels](#-floating-labels)
8. [Layout](#-layout)
9. [Validation](#-validation)

### &#10022; Form Control:
This will creates beautiful and rich in style textual form input elements such as [`<input>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/input-tag.md) and [`<textarea>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/textarea-tag.md).

*Syntax: add `.form-control` class to the input elements.*

```html
<div>
  <label for="email-address" class="form-label">Email Address</label>
  <input type="email" class="form-control" id="email-address" placeholder="Enter your email">
</div>
```

### &#10022; Sizing of form control:

*Syntax: add `.form-control{-sm|-lg}` class to the input elements.*

```html
<!-- Small sized form control element -->
<input type="email" class="form-control-sm" id="email-address" placeholder="Enter your email">
<!-- Medium sized or Default form control element -->
<input type="email" class="form-control" id="email-address" placeholder="Enter your email">
<!-- Large sized form control element -->
<input type="email" class="form-control-lg" id="email-address" placeholder="Enter your email">
```

### &#10022; Disabled form control:

*Syntax: add `disabled` attribute to the input elements.*

```html
<input type="text" class="form-control" id="user-name" placeholder="Enter your user name" disabled>
```

### &#10022; Readonly form control:

*Syntax: add `readonly` attribute to the input elements.*

```html
<input type="text" class="form-control" id="user-name" placeholder="Enter your user name" readonly>
```

### &#10022; Readonly plain text:

*Syntax: add `.form-control-plaintext` class and `readonly` attribute to the input elements.*

```html
<input type="text" class="form-control-plaintext" id="user-name" placeholder="Enter your user name" readonly>
```

### &#10022; File input form control:

*Syntax: add `.form-control` class to the file input elements.*

```html
<input type="file" class="form-control" id="profile-picture" placeholder="Please choose picture">
```

### &#10022; Color input form control:

*Syntax: add `.form-control-color` class to the input elements with `.form-control` class.*

```html
<input type="color" name="theme-color" class="form-control form-control-color" value="#000000">
```

### &#10022; Datalist form control:

*Syntax: add `.form-control` class to the input elements.*

```html
<label for="search-topic" class="form-label">Search Topic</label>
<input class="form-control" list="search-options" id="search-topic" placeholder="Type to search topic...">
<datalist id="search-options">
  <option value="Latest">
  <option value="News">
  <option value="Technology">
  <option value="Health">
</datalist>
```

---

### &#10022; Form Text:
This is mostly used in forms for informative purpose only. It displays text in block-level or inline-level inside the container.

*Syntax: add `.form-text` class to the element.*

```html
<div>
  <label for="email-address" class="form-label">Email Address</label>
  <input type="email" class="form-control" id="email-address" aria-describedby="emailInfo">
  <div id="emailInfo" class="form-text">Your email address will never share to anyone.</div>
</div>
```

---

### &#10022; Select:
Bootstrap makes beautiful and responsive rich select boxes.

*Syntax: add `.form-select` class to the element.*

```html
<select class="form-select" aria-label="Payment Options">  
  <option value="cash" selected>Cash</option>
  <option value="upi">UPI</option>
  <option value="credit-card">Credit Card</option>
  <option value="paypal">Paypal</option>
</select>
```

### &#10022; Sizing of select element:

*Syntax: add `.form-select{-sm|-lg}` class to the select elements.*

```html
<!-- Small sized form select element -->
<select class="form-select-sm" aria-label="Payment Options">...</select>
<!-- Medium sized or Default form select element -->
<select class="form-select" aria-label="Payment Options">...</select>
<!-- Large sized form select element -->
<select class="form-select-lg" aria-label="Payment Options">...</select>
```

*Multiple and Disabled select element are defined with attribute only.*

---

### &#10022; Checkboxes and Radios:
To make checkboxes and radios are in rich and easy to interact than traditional element.

### &#10022; Checkboxes:

*Syntax:* 
	- Add `.form-check-input` class to the checkboxes elements.
	- Add `.form-check` class to the container.
	- Add `.form-check-label` class to the label element.

```html
<div class="form-check">
  <input type="checkbox" class="form-check-input" value="true" id="agree-terms">
  <label class="form-check-label" for="agree-terms">
    Agree Terms and Conditions
  </label>
</div>
```

*Checked and Disabled state checkboxes are defined by specifying attribute.*

### &#10022; Radios:

*Syntax:* 
	- Add `.form-check-input` class to the radios elements.
	- Add `.form-check` class to the container.
	- Add `.form-check-label` class to the label element.

```html
<div class="form-check">
  <input class="form-check-input" type="radio" name="gender" id="gender-male" value="male">
  <label class="form-check-label" for="gender-male">Male</label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="gender" id="gender-female" value="female">
  <label class="form-check-label" for="gender-female">Female</label>
</div>
<div class="form-check">
  <input class="form-check-input" type="radio" name="gender" id="gender-other" value="other">
  <label class="form-check-label" for="gender-other">Not interested to specify</label>
</div>
```

*Checked and Disabled state radios are defined by specifying attribute.*

### &#10022; Switches:

*Syntax:* 
	- Checkboxes are treated as switches.
	- Add `.form-check-input` class to the checkbox elements.
	- Add `.form-check` and `.form-switch` classes to the container.	
	- Add `.form-check-label` class to the label element.

```html
<div class="form-check form-switch">
  <input type="checkbox" class="form-check-input" id="keep-me-signed">
  <label class="form-check-label" for="keep-me-signed">Keep me signed</label>
</div>
```

*Checked and Disabled state switches are defined by specifying attribute.*

### &#10022; Inline form check elements:
By default `.form-check` elements are arranged and stacked vertically.

*Syntax: add `.form-check-inline` class to the `.form-check` class.*

```html
<div class="form-check form-check-inline">...</div>
<div class="form-check form-check-inline">...</div>
<div class="form-check form-check-inline">...</div>
```

### &#10022; Toggle Buttons:
It can be differentiated by it's color when toggling in bootstrap. If it is active then it will be dark in color, otherwise normal color.

*Syntax:*
	- Add `.btn-check` class to the input elements.
	- Add `.btn-{color}` class to the labels.

```html
<!-- Unchecked or Inactive button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off">
<label class="btn btn-primary" for="select-review">Good</label>

<!-- Checked or Active button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off" checked>
<label class="btn btn-primary" for="select-review">Good</label>

<!-- Disabled button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off" disabled>
<label class="btn btn-primary" for="select-review">Good</label>

<!-- Checked button with Radios -->
<input type="radio" class="btn-check" id="gender-male" autocomplete="off" checked>
<label class="btn btn-primary" for="gender-male">Male</label>
```

### &#10022; Outlined Toggle Buttons:
It can be differentiated by filling background color when toggling in bootstrap. If it is active then it will be filled with background color, otherwise not filled background color.

*Syntax:*
	- Add `.btn-check` class to the input elements.
	- Add `.btn-outline-{color}` class to the labels.

```html
<!-- Unchecked or Inactive button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off">
<label class="btn btn-outline-primary" for="select-review">Good</label>

<!-- Checked or Active button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off" checked>
<label class="btn btn-outline-primary" for="select-review">Good</label>

<!-- Disabled button -->
<input type="checkbox" class="btn-check" id="select-review" autocomplete="off" disabled>
<label class="btn btn-outline-primary" for="select-review">Good</label>

<!-- Checked button with Radios -->
<input type="radio" class="btn-check" id="gender-male" autocomplete="off" checked>
<label class="btn btn-outline-primary" for="gender-male">Male</label>
```

--- 

### &#10022; Range:
To make range input more interactive to the user using bootstrap.

*Syntax: add `.form-range` class to the range input.*

```html
<label for="price-range" class="form-label">Price range</label>
<input type="range" class="form-range" id="price-range" min="100" max="10000" step="1">
```

*Disabled state range inputs are defined by specifying attribute.*

--- 

### &#10022; Input Group:
To make visually grouping a some of the form elements is possible by using bootstrap.

*Syntax: add `.input-group` class to the wrapper or container element.*

```html
<label for="username">Username</label>
<div class="input-group">
  <input type="text" class="form-control" id="username" placeholder="Choose username" aria-label="choose your username" aria-describedby="username-info">
  <span class="input-group-text" id="username-info">@host.com</span>
</div>
```

### &#10022; Wrapping input group:
To avoid wrapping in the input group use bootstrap flex class for nowrap.

*Syntax: add `.flex-nowrap` class to the `.input-group` class.* 

```html
<label for="username">Username</label>
<div class="input-group flex-nowrap">
  ...
</div>
```

### &#10022; Sizing of input group:
To use different size of input group use bootstrap sizing classes.

*Syntax: add `.input-group{-sm|-lg}` class to the `.input-group` class.* 

```html
<!-- Small sized form control element -->
<div class="input-group input-group-sm">...</div>

<!-- Medium sized or Default form control element -->
<div class="input-group">...</div>

<!-- Large sized form control element -->
<div class="input-group input-group-lg">...</div>
```

### &#10022; Input group for checkboxes and radios:
To group checkboxes and radio elements using bootstrap with class.

*Syntax: wrap with `.input-group-text` class to the checkboxes and radios.*

```html
<div class="input-group">
  <div class="input-group-text">
    <input class="form-check-input mt-0" type="checkbox" value="" aria-label="Checkbox for input">
  </div>
  <input type="text" class="form-control" aria-label="Input with checkbox">
</div>
```

### &#10022; Multiple inputs with input group:
To group multiple form elements in a single group.

```html
<div class="input-group">
  <span class="input-group-text">Full name</span>
  <input type="text" class="form-control"  aria-label="First name" placeholder="First name">
  <input type="text" class="form-control"  aria-label="Last name" placeholder="Last name">
</div>
```

### &#10022; Multiple addons with input group:

```html
<div class="input-group">
  <span class="input-group-text">%</span>
  <span class="input-group-text">0.00</span>
  <input type="text" class="form-control" aria-label="Interest in percentage (in two decimal places)">
</div>
```

### &#10022; Buttons addons with input group:

```html
<div class="input-group">
  <input type="text" class="form-control" placeholder="Product name" aria-label="product name" aria-describedby="add-button">
  <button class="btn btn-outline-primary" type="button" id="add-button">Add</button>
</div>
```

### &#10022; Custom forms with input group:

```html
<div class="input-group">
  <label class="input-group-text" for="category">Category</label>
  <select class="form-select" id="category">
      <option value="Latest">Latest</option>
      <option value="News">News</option>
      <option value="Technology">Technology</option>
      <option value="Health">Health</option>
  </select>
</div>
```

---

### &#10022; Floating Labels:
To create beautiful form element with floating label, that will float when user focus.

*Syntax: wrap with `.form-floating` class to the input and label.*

```html
<!-- For input elements -->
<div class="form-floating">
  <input type="email" class="form-control" id="email" placeholder="name@host.com">
  <label for="email">Email address</label>
</div>

<!-- For select elements -->
<div class="form-floating">
  <label for="category">Category</label>
  <select class="form-select" id="category">
      <option value="Latest">Latest</option>
      <option value="News">News</option>
      <option value="Technology">Technology</option>
      <option value="Health">Health</option>
  </select>
</div>

<!-- For textarea elements -->
<div class="form-floating">
  <textarea class="form-control" placeholder="Enter your comments here" id="comments" rows="5"></textarea>
  <label for="comments">Comments</label>
</div>
```

---

### &#10022; Layout:
Create different form layout using bootstrap.

### &#10022; Form grid:
Using bootstrap grid classes `.row` and `.col`.

```html
<div class="row">
  <div class="col-md-6">
    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
  </div>
  <div class="col">
    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
  </div>
</div>
```

### &#10022; Horizontal form:
*Syntax: `.col-form-label` is used to treat the label as column.*

```html
<!-- Small sized form control element -->
<div class="row">
  <label for="email" class="col-sm-3 col-form-label col-form-label-sm">Email</label>
  <div class="col-sm-9">
    <input type="email" class="form-control form-control-sm" id="email">
  </div>
</div>

<!-- Medium sized or Default form control element -->
<div class="row">
  <label for="email" class="col-sm-3 col-form-label">Email</label>
  <div class="col-sm-9">
    <input type="email" class="form-control" id="email">
  </div>
</div>

<!-- Large sized form control element -->
<div class="row">
  <label for="email" class="col-sm-3 col-form-label col-form-label-lg">Email</label>
  <div class="col-sm-9">
    <input type="email" class="form-control form-control-lg" id="email">
  </div>
</div>
```

### &#10022; Auto sizing form elements:

*Syntax: wrap with `.col-auto` class to the input elements.*

```html
<div class="row">
  <div class="col-auto">
    <input type="text" class="form-control" placeholder="First name" aria-label="First name">
  </div>
  <div class="col-auto">
    <input type="text" class="form-control" placeholder="Last name" aria-label="Last name">
  </div>
</div>
```

---

### &#10022; Validation:
To validate form inputs and give valid feedback to the user for those information entered.

Bootstrap scopes `:valid` and `:invalid` pseudo classes styles to the element through the parent (usually [`<form>`](https://github.com/ag-sanjjeev/HTML-Notes/blob/master/tags/form-tag.md)) element with `.was-validate` class.

For server side validation use `.is-valid` and `.is-invalid` classes to the specific form element without `.was-validated` class.

`.was-validated` class will show validation feedback when page loaded by trying to submit action.

`.needs-validation` class will not show validation feedback initially. But it shows when try to submit form.

### &#10022; Client side validation:

```html
<form class="row needs-validation" novalidate>
  <div class="col-md-6">
    <label for="email" class="form-label">Email address</label>
    <input type="email" class="form-control" id="email" required>
    <div class="valid-feedback">
      Email address is valid
    </div>
    <div class="invalid-feedback">
      Please provide a valid email address
    </div>
  </div>
  <div class="col-md-6">
    <label for="password" class="form-label">Password</label>
    <input type="password" class="form-control" id="password" required>
    <div class="valid-feedback">
      Password is strong
    </div>
    <div class="invalid-feedback">
      Your password is weak
    </div>
  </div>
  <button type="submit" class="btn-primary text-center">Login</button>
</form>

<!-- Need to add script for validation -->
<script type="text/javascript">

// It prevents the form being submitted if it is invalid
(function () {
  'use strict'

  // Getting all DOM reference of the form with class name
  var forms = document.querySelectorAll('.needs-validation')

  // Checking each form through a loop
  Array.prototype.slice.call(forms)
    .forEach(function (form) {
      form.addEventListener('submit', function (event) {
        if (!form.checkValidity()) {
          event.preventDefault();
          event.stopPropagation();
        }

        // Adding class if it is in-valid
        form.classList.add('was-validated');
      }, false);
    });
})();

</script>
```

### &#10022; Server side validation:

```html
<form class="row">
  <div class="col-md-6">
    <label for="email" class="form-label">Email address</label>
    <input type="email" class="form-control is-invalid" id="email" required>
    <div class="valid-feedback">
      Email address is valid
    </div>
    <div class="invalid-feedback">
      Please provide a valid email address
    </div>
  </div>
  <div class="col-md-6">
    <label for="password" class="form-label">Password</label>
    <input type="password" class="form-control is-valid" id="password" required>
    <div class="valid-feedback">
      Password is strong
    </div>
    <div class="invalid-feedback">
      Your password is weak
    </div>
  </div>
  <button type="submit" class="btn-primary text-center">Login</button>
</form>
```

### &#10022; Tooltip feedback:
```html
<form class="row">
  <div class="col-md-6">
    ...
    <div class="valid-tooltip">
      Email address is valid
    </div>
    <div class="invalid-tooltip">
      Please provide a valid email address
    </div>
  </div>
  <div class="col-md-6">
    ...
    <div class="valid-tooltip">
      Password is strong
    </div>
    <div class="invalid-tooltip">
      Your password is weak
    </div>
  </div>
  ...
</form>
```

---

[&#8682; To Top](#-forms)

[&#10094; Previous Topic](./components.dropdowns.md) &emsp; [Next Topic &#10095;](./components.list-group.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)