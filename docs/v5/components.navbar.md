## &#10022; Navbar:
Create beautiful and responsive navigation header using bootstrap classes.
- Navbar created with `.navbar` class, responsive collapsive `.navbar-expand-{sm|md|lg|xl|xxl}` class and color schemes. 

```html
<!-- Navbar -->
<nav class="navbar navbar-light bg-light">
  ...
</nav>
```

- Represent Brand in the navigation:

*Syntax: add `.navbar-brand` class*

```html
<!-- As a link -->
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">{Brand name}</a>
  </div>
</nav>

<!-- As a heading -->
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
    <span class="navbar-brand h1">{Brand name}</span>
  </div>
</nav>

<!-- As a image or icon -->
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="{URL/Location}" alt="{Brand logo}">
    </a>
  </div>
</nav>
```

- Adding navigation link items:

*Syntax: add `.nav-link` class*

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <!-- Container -->
  <div class="container-fluid">
    <!-- Navbar brand heading -->
    <a class="navbar-brand" href="#">{Brand name}</a>

    <!-- Navbar toggler when collapsed -->
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu" aria-controls="navMenu" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <!-- Navbar link items collapse container -->
    <div class="collapse navbar-collapse" id="navMenu">

      <!-- Navigation list -->
      <ul class="navbar-nav">

        <!-- Navigation item -->
        <li class="nav-item">

          <!-- Active navigation link item -->
          <a class="nav-link active" aria-current="page" href="#">{Link item}</a>
        </li>
        <li class="nav-item">

          <!-- Navigation link item -->
          <a class="nav-link" href="#">{Link item}</a>
        </li>
        <li class="nav-item">

          <!-- Disabled navigation link item -->
          <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">{Link item}</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

- Navigation link items with dropdown:

*Syntax: add `.dropdown` class to the `.nav-item` class*

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <!-- Container -->
  <div class="container-fluid">
    <!-- Navbar brand heading -->
    <a class="navbar-brand" href="#">...</a>

    <!-- Navbar toggler when collapsed -->
    <button class="navbar-toggler" ...>
      <span class="navbar-toggler-icon"></span>
    </button>

    <!-- Navbar link items collapse container -->
    <div class="collapse navbar-collapse" id="navMenu">

      <!-- Navigation list -->
      <ul class="navbar-nav">

        <!-- Navigation item -->
        <li class="nav-item">...</li>        
        
        <!-- Dropdown navigation item -->
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="dropdownNavigation" role="button" data-bs-toggle="dropdown" aria-expanded="false">{Link item}</a>
          <ul class="dropdown-menu" aria-labelledby="dropdownNavigation">
            <li><a class="dropdown-item" href="#">{Link item}</a></li>
            ...
            ...
          </ul>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

- Navbar text:

*Syntax: add `.navbar-text` class*

```html
<nav class="navbar navbar-light bg-light">
  <div class="container-fluid">
    <span class="navbar-text">{Navbar text}</span>
  </div>
</nav>
```

- Color scheme:

*Syntax:*
  - Add `.navbar-dark` class will treat that background color of navbar in dark. So, that change text colors as light.
  - Add `.navbar-light` class will treat that background color of navbar in light. So, that change text colors as dark.
  - Add `.bg-{primary|secondary|success|warning|danger|info}` background classes with `.navbar-{light|dark} classes to enrich style of the navbar.`

```html
<nav class="navbar navbar-dark bg-success">
  ...
</nav>

<nav class="navbar navbar-light bg-warning">
  ...
</nav>
```

- Fixed top navbar:

*Syntax: add `.fixed-top` class to `.navbar` class.*

```html
<nav class="navbar fixed-top navbar-light bg-info">
  ...
</nav>
```

- Fixed bottom navbar:

*Syntax: add `.fixed-bottom` class to `.navbar` class.*

```html
<nav class="navbar fixed-bottom navbar-light bg-info">
  ...
</nav>
```

- Sticky top navbar:

*Syntax: add `.sticky-top` class to `.navbar` class.*

```html
<nav class="navbar sticky-top navbar-light bg-info">
  ...
</nav>
```

---
[&#8682; To Top](#-navbar)

[&#10094; Previous Topic](./components.modals.md) &emsp; [Next Topic &#10095;](./components.navs-and-tabs.md)

[&#8962; Goto Home Page](../../README.md) &emsp; [&#9776; Goto Components](./components.md)