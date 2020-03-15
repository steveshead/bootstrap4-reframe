# Bootstrap4 - Reframe

Reframe is a test template built from my first wireframe built in Figma.  I liked it enough to create this theme from it. Below are some functions to help you get the best use of this theme. The theme includes smooth scroll and scrollspy, and the ability to customize Bootstrap 4 defaults. View the [demo](https://steveshead.github.io/bootstrap4-reframe) site [here](https://steveshead.github.io/bootstrap4-reframe).

### Nabar - change color on scroll
When you scroll down the page the navigation changes from transparent to whatever color you have set to "primary".  To change the background color upon scroll simply change "bg-primary" in lines 6 and 8 of assets/js/custom.js to the bootstrap color you want to use.  For instance, bg-warning.


### Smooth Scroll
The 'smoothscroll' code is included in assets/js/custom.js - You'll need to add ```data-smooth="#anchor"``` and ```href="#anchor"``` to your nav links if you add new menu items.  You'll also need to add an ID tag to the section you want smooth scroll to scroll to.

**Menu example**:
```html
  <li class="nav-item">
    <a class="nav-link" data-smooth="#anchor" href="#anchor">Anchor</a>
  </li>
```

**ID example**:
```html
<section id="anchor">
```


### Scroll Spy
Utils.js is included in bootstrap.js, so to use scrollspy add the following to your "body" tag.  Adjust the data-offset to where you want the link to activate. Note it is already added to this theme.

```html
<body id="home" data-spy="scroll" data-target="#navbarColor01" data-offset="90">
```

The data target is the ID of your nav menu, and the data offset is the distance from the anchor point.  You can adjust as needed.


### Replace the favicon
Create your custom favicon [here](https://www.favicon-generator.org/).  Then with the code generated replace the code below in your index.html, and replace the favicon images in assets/img/favicons with yours.

```html
<link rel="apple-touch-icon" sizes="57x57" href="assets/img/favicons/apple-icon-57x57.png">
<link rel="apple-touch-icon" sizes="60x60" href="assets/img/favicons/apple-icon-60x60.png">
<link rel="apple-touch-icon" sizes="72x72" href="assets/img/favicons/apple-icon-72x72.png">
<link rel="apple-touch-icon" sizes="76x76" href="assets/img/favicons/apple-icon-76x76.png">
<link rel="apple-touch-icon" sizes="114x114" href="assets/img/favicons/apple-icon-114x114.png">
<link rel="apple-touch-icon" sizes="120x120" href="assets/img/favicons/apple-icon-120x120.png">
<link rel="apple-touch-icon" sizes="144x144" href="assets/img/favicons/apple-icon-144x144.png">
<link rel="apple-touch-icon" sizes="152x152" href="assets/img/favicons/apple-icon-152x152.png">
<link rel="apple-touch-icon" sizes="180x180" href="assets/img/favicons/apple-icon-180x180.png">
<link rel="icon" type="image/png" sizes="192x192" href="assets/img/favicons/android-icon-192x192.png">
<link rel="icon" type="image/png" sizes="32x32" href="assets/img/favicons/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="96x96" href="assets/img/favicons/favicon-96x96.png">
<link rel="icon" type="image/png" sizes="16x16" href="assets/img/favicons/favicon-16x16.png">
<link rel="manifest" href="assets/img/favicons/manifest.json">
<meta name="msapplication-TileColor" content="#ffffff">
<meta name="msapplication-TileImage" content="assets/img/favicons/ms-icon-144x144.png">
```

### Customize Bootstrap 4
This theme also includes a custom scss file in assets/scss/custom.scss such that you can override the default bootstrap 4 settings. You will need to set your code editor to compile assets/scss/custom.scss to assets/css/custom.css in this theme if you want to change any of the configurable Bootstrap 4 defaults.  If you are overriding bootstrap defaults you will be able to view the changes in the included custom.html file.

Here are some examples of overriding Bootstrap (using custom.scss).

```scss
// override bootstrap default theme colors, and, add a custom color.
$theme-colors: (
  "primary": #375a7f,
  "secondary": #444,
  "success": #00bc8c,
  "info": #3498DB,
  "warning": #F39C12,
  "danger": #E74C3C,
  "custom": #ff7034,
);

// increase the default spacing
$spacer:1.25rem;

// adjust the default heading font weight
$headings-font-weight:300;

// adjust the default font weights
$font-weight-light:200;
$font-weight-normal:300;
$font-weight-bold:500;

// adjust the default font size
$font-size-base:1.2rem;

// add more spacers
$spacer: 1rem !default;
$spacers: (
    6: ($spacer * 4),
    7: ($spacer * 5),
    8: ($spacer * 7.50),
    9: ($spacer * 10)
  );

// set the button border radius
$btn-border-radius:2px;

// change the hyperlink color
$link-color: #00bc8c;

// remove underline from hyperlinks
$link-hover-decoration: none;
```

If you're not comfortable writing scss you can add your css to style.css in the root of this template.

View the [demo](https://steveshead.github.io/bootstrap4-reframe) site [here](https://steveshead.github.io/bootstrap4-reframe).
