# BOOTSTRAP 5 NOTES

This repository contains Bootstrap 5 topics and their notes to learn as a beginner.

*Refer the below contents, To kick start the learning of Bootstrap. which gives you __step by step__ approach to the concepts.*
\
&nbsp;

## Prerequisites
Before diving into Bootstrap, ensure you have a strong foundation in:
1. [HTML](https://github.com/ag-sanjjeev/HTML-Notes): Understand the structure and elements of web pages.
2. [CSS](https://github.com/ag-sanjjeev/CSS-Notes): Grasp styling and layout concepts.
3. [JavaScript](https://github.com/ag-sanjjeev/JavaScript-Notes): Have a good understanding of core JavaScript concepts like variables, functions, objects, and DOM manipulation.

## &#9776; CONTENTS 
1. [Introduction](./introduction.md)
    - [Downloading Bootstrap](./introduction.md#-downloading-bootstrap)
    - [Linking Bootstrap](./introduction.md#-linking-bootstrap)
    - [Structure of Bootstrap Page](./introduction.md#-structure-of-bootstrap-page)
2. [Bootstrap Layouts:](./docs/v5/bootstrap-layouts.md)
    - [Breakpoints](./docs/v5/bootstrap-layouts.md#-breakpoints)
    - [Containers](./docs/v5/bootstrap-layouts.md#-containers)
    - [Grid](./docs/v5/bootstrap-layouts.md#-grid)
    - [Rows](./docs/v5/bootstrap-layouts.md#-rows)
    - [Columns](./docs/v5/bootstrap-layouts.md#-columns)
    - [Columns Alignment](./docs/v5/bootstrap-layouts.md#-columns-alignment)
    - [Columns Order](./docs/v5/bootstrap-layouts.md#-columns-order)
    - [Gutters](./docs/v5/bootstrap-layouts.md#-gutters)
    - [Nesting and offsets](./docs/v5/bootstrap-layouts.md#-nesting-and-offsets)
    - [Utilities](./docs/v5/bootstrap-layouts.md#-utilities)
    - [Z Index](./docs/v5/bootstrap-layouts.md#-z-index)
3. [Bootstrap Content:](./docs/v5/bootstrap-content.md)
    - [Reboot](./docs/v5/bootstrap-content.md#-reboot)
    - [Typography](./docs/v5/bootstrap-content.md#-typography)
    - [Images](./docs/v5/bootstrap-content.md#-images)
    - [Tables](./docs/v5/bootstrap-content.md#-tables)
    - [Figures](./docs/v5/bootstrap-content.md#-figures)
5. [Components:](./docs/v5/components.md)
    - [Accordion](./docs/v5/components.accordion.md)
    - [Alerts](./docs/v5/components.alerts.md)
    - [Badge](./docs/v5/components.badge.md)
    - [Breadcrumb](./docs/v5/components.breadcrumb.md)
    - [Buttons](./docs/v5/components.buttons.md)
    - [Button group](./docs/v5/components.button-group.md)
    - [Close button](./docs/v5/components.close-button.md)
    - [Cards](./docs/v5/components.cards.md)
    - [Carousel](./docs/v5/components.carousel.md)
    - [Collapse](./docs/v5/components.collapse.md)
    - [Dropdowns](./docs/v5/components.dropdowns.md)
    - [Forms](./docs/v5/components.forms.md)
      - [Form control](./docs/v5/components.forms.md#-form-control)
      - [Form Text](./docs/v5/components.forms.md#-form-text)
      - [Select](./docs/v5/components.forms.md#-select)
      - [Checkboxes and Radios](./docs/v5/components.forms.md#-checkboxes-and-radios)
      - [Range](./docs/v5/components.forms.md#-range)
      - [Input group](./docs/v5/components.forms.md#-input-group)
      - [Floating labels](./docs/v5/components.forms.md#-floating-labels)
      - [Layout](./docs/v5/components.forms.md#-layout)
      - [Validation](./docs/v5/components.forms.md#-validation)
    - [List group](./docs/v5/components.forms.md#-list-group)
    - [Modals](./docs/v5/components.forms.md#-modals)
    - [Navbar](./docs/v5/components.forms.md#-navbar)
    - [Navs and tabs](./docs/v5/components.forms.md#-navs-and-tabs)
    - [Offcanvas](./docs/v5/components.forms.md#-offcanvas)
    - [Pagination](./docs/v5/components.forms.md#-pagination)
    - [Popovers](./docs/v5/components.forms.md#-popovers)
    - [Progress bars](./docs/v5/components.forms.md#-progress-bars)
    - [Scrollspy](./docs/v5/components.forms.md#-scrollspy)
    - [Spinners](./docs/v5/components.forms.md#-spinners)
    - [Toasts](./docs/v5/components.forms.md#-toasts)
    - [Tooltips](./docs/v5/components.forms.md#-tooltips)
6. [Bootstrap Helpers](#-bootstrap-helpers)
    - [Clearfix](#-clearfix)
    - [Colored links](#-colored-links)
    - [Ratio](#-ratio)
    - [Position](#-position)
    - [Visually hidden](#-visually-hidden)
    - [Stretched link](#-stretched-link)
    - [Text truncation](#-text-truncation)
7. [Customization and Theming:](#-customization-and-theming)
    - [Variables](#-variables)  
    - [Mixins](#-mixins)  
    - [Utilities:](#-utilities)
      - [API](#-api)
      - [Background](#-background)
      - [Borders](#-borders)
      - [Colors](#-colors)
      - [Display](#-display)
      - [Flex](#-flex)
      - [Float](#-float)
      - [Interactions](#-interactions)
      - [Overflow](#-overflow)
      - [Position](#-position)
      - [Shadows](#-shadows)
      - [Sizing](#-sizing)
      - [Spacing](#-spacing)
      - [Text](#-text)
      - [Vertical align](#-vertical-align)
      - [Visibility](#-visibility)
8. [JavaScript Integration:](#-javascript-integration)
    - [jQuery Integration](#-jquery-integration)
    - [Bootstrap JavaScript Plugins](#-bootstrap-javascript-plugins)
9. [Responsive Design:](#-responsive-design)
    - [Media Queries](#-media-queries)  
    - [Responsive Utilities](#-responsive-utilities)
10. [Advanced Topics:](#-advanced-topics)
    - [Custom Components](#-custom-components)
    - [Sass Integration](#-sass-integration)
    - [Bootstrap Ecosystem](#-bootstrap-ecosystem)

---

By following this roadmap and consistently practicing, you can learn a basic fundamentals in Bootstrap and build mobile first responsive web pages.

## &#9873; Contribution
Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request. Make sure to follow the existing coding style and provide clear documentation for your changes.

## &#9873; License
This reference licensed under the [MIT license](LICENSE). Feel free to use, modify, and distribute it as per the terms of the license.

## &#9873; Contact
If you have any questions or need further assistance, please feel free to reach me at [Email](mailto:resulttext)


Thanks for reviewing this reference notes!