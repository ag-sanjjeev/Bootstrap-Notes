## &#10022; Carousel:
Carousel means slider element which make slideshow for the elements to cyclic through it.

*Syntax: add `.carousel` and `.slide` classes with bootstrap data attribute `data-bs-ride="carousel"`*
```html
<div id="{carousel-id}" class="carousel slide" data-bs-ride="carousel">...</div>
```

**Associated classes and card elements:**

- Carousel Inner:
Container for carousel items
```html
<div id="{carousel-id}" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">...</div>
</div>
```
- Carousel Items:
```html
<div id="{carousel-id}" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">...</div>
    <div class="carousel-item">...</div>
    <div class="carousel-item">...</div>
  </div>
</div>
```

- Active Carousel Item:
```html
<div class="carousel-item active">...</div>
```

- Carousel Control:
Add buttons after carousel inner container. 

*Carousel Previous Button: It will be located in the left side of carousel.* 

```html
<!-- Previous Button -->
<button class="carousel-control-prev" type="button" data-bs-target="#{carousel-id}" data-bs-slide="prev">
  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
  <span class="visually-hidden">Previous</span>
</button>
```
*Carousel Next Button: It will be located in the right side of carousel.*
```html
<!-- Next Button -->
<button class="carousel-control-next" type="button" data-bs-target="#{carousel-id}" data-bs-slide="next">
  <span class="carousel-control-next-icon" aria-hidden="true"></span>
  <span class="visually-hidden">Next</span>
</button>
```

- Carousel With Indicator:
To indicate which carousel item is being active or displayed and line up slides in the indicator.
```html
<div class="carousel-indicators">
  <!-- Indicated the active or current slide -->
  <button type="button" data-bs-target="#{carousel-id}" data-bs-slide-to="0" class="active" aria-current="true" aria-label="{slide-label}"></button>

  <!-- All other slides -->
  <button type="button" data-bs-target="#{carousel-id}" data-bs-slide-to="1" aria-label="{slide-label}"></button>
  <button type="button" data-bs-target="#{carousel-id}" data-bs-slide-to="2" aria-label="{slide-label}"></button>
</div>
```

- Carousel Caption:
Carousel item can have carousel caption text.
```html
<div class="carousel-item">  
  <div class="carousel-caption">
    <h3>...</h3>
    <p>...</p>
  </div>
</div>
```

- Carousel Cross Fade Effect:
To make fade in and fade out between slide transition, add `.carousel-fade` class to the `.carousel` class.
```html
<div id="{carousel-id}" class="carousel slide carousel-fade" data-bs-ride="carousel">...</div>
```

- Carousel Slide Interval:
To add interval between each slides or how long the carousel item to be active or displayed by adding bootstrap data attribute `data-bs-interval="{interval-in-milli-seconds}"`.
```html
<div class="carousel-item" data-bs-interval="2000">...</div>
<div class="carousel-item" data-bs-interval="3000">...</div>
```

- Disable Touch Swip:
To use carousel control button rather than touch swip. To disabling touch swip by adding bootstrap data attribute `data-bs-touch="false"`.
```html
<div id="{carousel-id}" class="carousel slide carousel-fade" data-bs-touch="false" data-bs-ride="carousel">...</div>
```

- Carousel Dark Themed:
To apply dark theme for carousel by adding `.carousel-dark` class to the `.carousel` class.
```html
<div id="{carousel-id}" class="carousel carousel-dark slide carousel-fade" data-bs-touch="false" data-bs-ride="carousel">...</div>
```

- Accessing carousel via JavaScript:
```javascript
var carouselReference = document.querySelector('#{carousel-id}');
var carousel = new bootstrap.Carousel(carouselReference);
```

- Add options to carousel via JavaScript:
```javascript
var carouselReference = document.querySelector('#{carousel-id}');
var carousel = new bootstrap.Carousel(carouselReference, {
  interval: 2000, // which sets interval between slides in milli seconds
  keyboard: true, // which sets carousel to be interacted with keyboard navigation
  pause: 'hover', // which sets carousel to be paused on certain events such as hover, mouseenter, touchend, etc, or by simply set boolean value false which never pause.
  ride: false, // which sets carousel to be autoplayed after user manually cycle through next or previous items. or If sets `carousel` value that makes it autoplay when loaded.
  touch: false, // Which sets touch interaction to be disabled or enabled by setting boolean value
  wrap: false // which sets carousel should cycle continuously or have stops at end of the slide.
})
```

- Methods to control carousel via JavaScript:
  - `cycle()` - It makes carousel to cycles through next item from left to right.
  - `pause()` - It stops the carousel being cycling through items.
  - `prev()` -  It makes carousel to cycle through previous item.
  - `next()` -  It makes carousel to cycle through next item.
  - `nextWhenVisible()` - It would not allow to cycle through carousel items when the page or the carousel or its parent is not visible. 
  - `to()` -  Switch to particular carousel item by mentioning the item number.
  - `dispose()` - It removes carousel from DOM tree.
  - `getInstance()` - Static method which allows to get the carousel instance.
  - `getOrCreateInstance()` - Static method which returns a carousel instance or create a new one in case it wasn't initialized yet.

- Events related to carousel:
  - `slide.bs.carousel` - It triggers an event when the slide instance method is invoked.
  - `slid.bs.carousel` - It triggers an event when the carousel has completed its slide transition.
  - Each event has properties such as `direction, relatedTarget, from, to`.
```javascript
var carouselReference = document.querySelector('#{carousel-id}');
carouselReference.addEventListener('slid.bs.carousel', function (event) { ... });
```

---
[&#8682; To Top](#-carousel)

[&#10094; Previous Topic](./components.cards.md) &emsp; [Next Topic &#10095;](./components.collapse.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)