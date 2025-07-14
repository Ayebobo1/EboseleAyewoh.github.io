# Portfolio Website API Documentation

## Table of Contents
1. [Project Overview](#project-overview)
2. [File Structure](#file-structure)
3. [CSS Framework & Components](#css-framework--components)
4. [JavaScript APIs](#javascript-apis)
5. [HTML Components](#html-components)
6. [Usage Examples](#usage-examples)
7. [Responsive Design](#responsive-design)
8. [Customization Guide](#customization-guide)

## Project Overview

This is a responsive portfolio website built using HTML5 UP's "Massively" template. It features a modern, article-oriented design with parallax background effects, smooth scrolling, and mobile-responsive navigation.

**Key Features:**
- Parallax scrolling background
- Responsive grid system
- Mobile navigation panel
- Smooth scroll effects
- Form components
- Icon integration (Font Awesome)
- Cross-browser compatibility

## File Structure

```
/
├── index.html              # Main homepage
├── elements.html           # UI components reference
├── generic.html           # Generic page template
├── assets/
│   ├── css/
│   │   ├── main.css       # Main stylesheet (4689 lines)
│   │   ├── noscript.css   # Non-JavaScript fallback styles
│   │   └── fontawesome-all.min.css # Font Awesome icons
│   ├── js/
│   │   ├── main.js        # Core JavaScript functionality
│   │   ├── util.js        # Utility functions
│   │   ├── jquery.min.js  # jQuery library
│   │   ├── jquery.scrollex.min.js # Scroll effects
│   │   ├── jquery.scrolly.min.js  # Smooth scrolling
│   │   ├── browser.min.js # Browser detection
│   │   └── breakpoints.min.js # Responsive breakpoints
│   ├── sass/              # SASS source files (if available)
│   └── webfonts/          # Font files
├── images/                # Image assets
├── README.txt            # Project information
└── LICENSE.txt           # License information
```

## CSS Framework & Components

### Responsive Grid System

The framework includes a comprehensive 12-column grid system with responsive breakpoints:

#### Breakpoints
- **Default**: 1681px and above
- **xlarge**: 1281px - 1680px
- **large**: 981px - 1280px  
- **medium**: 737px - 980px
- **small**: 481px - 736px
- **xsmall**: 361px - 480px
- **xxsmall**: 360px and below

#### Grid Classes

```html
<!-- Basic grid structure -->
<div class="row">
    <div class="col-6">Half width</div>
    <div class="col-6">Half width</div>
</div>

<!-- Responsive columns -->
<div class="row">
    <div class="col-12 col-6-medium col-4-large">
        Responsive column
    </div>
</div>
```

**Available Column Classes:**
- `.col-1` through `.col-12` - Basic column widths
- `.col-{size}-{breakpoint}` - Responsive columns (e.g., `.col-6-medium`)
- `.off-{size}` - Column offsets
- `.off-{size}-{breakpoint}` - Responsive offsets

**Row Modifiers:**
- `.gtr-0`, `.gtr-25`, `.gtr-50`, `.gtr-150`, `.gtr-200` - Gutter spacing
- `.gtr-uniform` - Uniform bottom margin
- `.aln-left`, `.aln-center`, `.aln-right` - Horizontal alignment
- `.aln-top`, `.aln-middle`, `.aln-bottom` - Vertical alignment

### Typography Components

#### Headings
```html
<h1>Main heading (3em/3.5em)</h1>
<h2>Secondary heading (2.25em/2.75em)</h2>
<h3>Tertiary heading (1.75em)</h3>
<h4>Quaternary heading (1.1em)</h4>
<h5>Small heading (0.9em)</h5>
<h6>Tiny heading (0.8em)</h6>
```

#### Text Formatting
```html
<p>Regular paragraph text</p>
<strong>Bold text</strong>
<em>Italic text</em>
<code>Inline code</code>
<sup>Superscript</sup>
<sub>Subscript</sub>
<u>Underlined text</u>
```

#### Headers with Subtitles
```html
<header>
    <h2>Heading with Subtitle</h2>
    <p>Subtitle text goes here</p>
</header>

<header class="major">
    <h1>Major Header</h1>
    <p>Major header subtitle</p>
</header>
```

### Button Components

#### Basic Buttons
```html
<!-- Standard buttons -->
<a href="#" class="button">Default Button</a>
<a href="#" class="button primary">Primary Button</a>

<!-- Button sizes -->
<a href="#" class="button small">Small Button</a>
<a href="#" class="button">Default Button</a>
<a href="#" class="button large">Large Button</a>

<!-- Button styles -->
<a href="#" class="button fit">Full Width Button</a>
<a href="#" class="button icon solid fa-download">Icon Button</a>
<span class="button disabled">Disabled Button</span>
```

#### Action Lists
```html
<ul class="actions">
    <li><a href="#" class="button primary">Primary</a></li>
    <li><a href="#" class="button">Default</a></li>
</ul>

<!-- Stacked actions -->
<ul class="actions stacked">
    <li><a href="#" class="button primary">First Action</a></li>
    <li><a href="#" class="button">Second Action</a></li>
</ul>

<!-- Fit actions -->
<ul class="actions fit">
    <li><a href="#" class="button">Button 1</a></li>
    <li><a href="#" class="button">Button 2</a></li>
</ul>
```

### Form Components

#### Input Fields
```html
<input type="text" name="name" placeholder="Name" />
<input type="email" name="email" placeholder="Email" />
<input type="tel" name="phone" placeholder="Phone" />
<input type="password" name="password" placeholder="Password" />
```

#### Select Dropdown
```html
<select name="category">
    <option value="">- Category -</option>
    <option value="1">Option 1</option>
    <option value="2">Option 2</option>
</select>
```

#### Radio Buttons
```html
<input type="radio" id="option1" name="group" checked>
<label for="option1">Option 1</label>

<input type="radio" id="option2" name="group">
<label for="option2">Option 2</label>
```

#### Checkboxes
```html
<input type="checkbox" id="checkbox1" name="checkbox1">
<label for="checkbox1">Checkbox Label</label>
```

#### Textarea
```html
<textarea name="message" placeholder="Your message" rows="6"></textarea>
```

#### Complete Form Example
```html
<form method="post" action="#">
    <div class="row gtr-uniform">
        <div class="col-6 col-12-xsmall">
            <input type="text" name="name" placeholder="Name" />
        </div>
        <div class="col-6 col-12-xsmall">
            <input type="email" name="email" placeholder="Email" />
        </div>
        <div class="col-12">
            <select name="category">
                <option value="">- Category -</option>
                <option value="1">Manufacturing</option>
                <option value="2">Shipping</option>
            </select>
        </div>
        <div class="col-12">
            <textarea name="message" placeholder="Message" rows="6"></textarea>
        </div>
        <div class="col-12">
            <ul class="actions">
                <li><input type="submit" value="Send Message" class="primary" /></li>
                <li><input type="reset" value="Reset" /></li>
            </ul>
        </div>
    </div>
</form>
```

### List Components

#### Basic Lists
```html
<!-- Unordered list -->
<ul>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
</ul>

<!-- Alternate style -->
<ul class="alt">
    <li>Alternate styled item 1</li>
    <li>Alternate styled item 2</li>
</ul>

<!-- Ordered list -->
<ol>
    <li>Numbered item 1</li>
    <li>Numbered item 2</li>
</ol>
```

#### Icon Lists
```html
<ul class="icons">
    <li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
    <li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
    <li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
</ul>

<!-- Alternate icon style -->
<ul class="icons alt">
    <li><a href="#" class="icon brands alt fa-linkedin"><span class="label">LinkedIn</span></a></li>
</ul>
```

#### Definition Lists
```html
<dl>
    <dt>Term 1</dt>
    <dd>Definition for term 1</dd>
    <dt>Term 2</dt>
    <dd>Definition for term 2</dd>
</dl>
```

### Table Components

#### Basic Table
```html
<div class="table-wrapper">
    <table>
        <thead>
            <tr>
                <th>Header 1</th>
                <th>Header 2</th>
                <th>Header 3</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Data 1</td>
                <td>Data 2</td>
                <td>Data 3</td>
            </tr>
        </tbody>
        <tfoot>
            <tr>
                <td colspan="2">Footer</td>
                <td>Total</td>
            </tr>
        </tfoot>
    </table>
</div>
```

#### Alternate Table Style
```html
<div class="table-wrapper">
    <table class="alt">
        <!-- Table content with alternate styling -->
    </table>
</div>
```

### Image Components

#### Basic Images
```html
<!-- Fit image -->
<span class="image fit">
    <img src="images/pic01.jpg" alt="Description" />
</span>

<!-- Left aligned image -->
<span class="image left">
    <img src="images/pic02.jpg" alt="Description" />
</span>

<!-- Right aligned image -->
<span class="image right">
    <img src="images/pic03.jpg" alt="Description" />
</span>

<!-- Main image -->
<span class="image main">
    <img src="images/pic04.jpg" alt="Description" />
</span>
```

#### Image Grid
```html
<div class="box alt">
    <div class="row gtr-50 gtr-uniform">
        <div class="col-4">
            <span class="image fit">
                <img src="images/pic01.jpg" alt="" />
            </span>
        </div>
        <div class="col-4">
            <span class="image fit">
                <img src="images/pic02.jpg" alt="" />
            </span>
        </div>
        <div class="col-4">
            <span class="image fit">
                <img src="images/pic03.jpg" alt="" />
            </span>
        </div>
    </div>
</div>
```

### Box Component

```html
<div class="box">
    <p>Content inside a styled box container.</p>
</div>

<div class="box alt">
    <p>Content inside an alternate styled box.</p>
</div>
```

### Pagination Component

```html
<ul class="pagination">
    <li><a href="#" class="previous">Prev</a></li>
    <li><a href="#" class="page active">1</a></li>
    <li><a href="#" class="page">2</a></li>
    <li><a href="#" class="page">3</a></li>
    <li><span class="extra">&hellip;</span></li>
    <li><a href="#" class="page">8</a></li>
    <li><a href="#" class="page">9</a></li>
    <li><a href="#" class="page">10</a></li>
    <li><a href="#" class="next">Next</a></li>
</ul>
```

## JavaScript APIs

### Core Functions (main.js)

#### Parallax Effect API
```javascript
/**
 * Applies parallax scrolling to an element's background image
 * @param {number} intensity - Parallax intensity (default: 0.25)
 * @returns {jQuery} jQuery object for chaining
 */
$.fn._parallax(intensity)
```

**Usage:**
```javascript
// Apply default parallax effect
$('#background-element')._parallax();

// Apply custom intensity
$('#background-element')._parallax(0.5);

// Multiple elements
$('.parallax-elements')._parallax(0.75);
```

**Example:**
```javascript
// Enable parallax on wrapper with custom intensity
$('#wrapper')._parallax(0.925);
```

### Utility Functions (util.js)

#### Navigation List Generator
```javascript
/**
 * Generate an indented list of links from a nav
 * Meant for use with panel()
 * @returns {string} HTML string of navigation links
 */
$.fn.navList()
```

**Usage:**
```javascript
// Convert navigation to flat list
var navHTML = $('#nav').navList();
```

#### Panel API
```javascript
/**
 * Panel-ify an element
 * @param {object} userConfig - Configuration options
 * @returns {jQuery} jQuery object
 */
$.fn.panel(userConfig)
```

**Configuration Options:**
```javascript
{
    delay: 0,                    // Animation delay in ms
    hideOnClick: false,          // Hide panel when clicking links
    hideOnEscape: false,         // Hide panel on Escape key
    hideOnSwipe: false,          // Hide panel on swipe gesture
    resetScroll: false,          // Reset scroll position on hide
    resetForms: false,           // Reset forms on hide
    side: null,                  // Panel side: 'left', 'right', 'top', 'bottom'
    target: $this,               // Target element for class toggling
    visibleClass: 'visible'      // CSS class to add when visible
}
```

**Usage:**
```javascript
// Basic panel
$('#myPanel').panel({
    side: 'right',
    hideOnClick: true,
    hideOnEscape: true
});

// Mobile navigation panel
$('#navPanel').panel({
    delay: 500,
    hideOnClick: true,
    hideOnSwipe: true,
    resetScroll: true,
    side: 'right',
    target: $('body'),
    visibleClass: 'is-navPanel-visible'
});
```

#### Placeholder API
```javascript
/**
 * Add placeholder support for older browsers
 * @returns {jQuery} jQuery object
 */
$.fn.placeholder()
```

**Usage:**
```javascript
// Enable placeholder fallback
$('input[placeholder]').placeholder();
```

### Scroll Effects

#### Scrollex (jquery.scrollex.min.js)
```javascript
/**
 * Advanced scroll effects
 * @param {object} options - Scrollex configuration
 * @returns {jQuery} jQuery object
 */
$.fn.scrollex(options)
```

**Usage:**
```javascript
// Basic scroll trigger
$('#element').scrollex({
    enter: function() {
        // Element enters viewport
        $(this).addClass('visible');
    },
    leave: function() {
        // Element leaves viewport
        $(this).removeClass('visible');
    }
});

// Advanced configuration
$('#main').scrollex({
    mode: 'bottom',
    top: '25vh',
    bottom: '-50vh',
    enter: function() {
        $('#intro').addClass('hidden');
    },
    leave: function() {
        $('#intro').removeClass('hidden');
    }
});
```

#### Scrolly (jquery.scrolly.min.js)
```javascript
/**
 * Smooth scrolling for anchor links
 * @param {object} options - Scrolly configuration
 * @returns {jQuery} jQuery object
 */
$.fn.scrolly(options)
```

**Usage:**
```javascript
// Enable smooth scrolling
$('.scrolly').scrolly();

// Custom configuration
$('.smooth-scroll').scrolly({
    speed: 1000,
    offset: 100
});
```

### Breakpoint Management

#### Breakpoints API
```javascript
// Define breakpoints
breakpoints({
    default:   ['1681px',   null       ],
    xlarge:    ['1281px',   '1680px'   ],
    large:     ['981px',    '1280px'   ],
    medium:    ['737px',    '980px'    ],
    small:     ['481px',    '736px'    ],
    xsmall:    ['361px',    '480px'    ],
    xxsmall:   [null,       '360px'    ]
});

// Breakpoint event handlers
breakpoints.on('>large', function() {
    // Code for screens larger than large breakpoint
});

breakpoints.on('<=medium', function() {
    // Code for screens medium and smaller
});
```

## HTML Components

### Page Structure

#### Basic Page Template
```html
<!DOCTYPE HTML>
<html>
<head>
    <title>Page Title</title>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no" />
    <link rel="stylesheet" href="assets/css/main.css" />
    <noscript><link rel="stylesheet" href="assets/css/noscript.css" /></noscript>
</head>
<body class="is-preload">
    <!-- Wrapper -->
    <div id="wrapper" class="fade-in">
        
        <!-- Intro (optional) -->
        <div id="intro">
            <h1>Site Title</h1>
            <p>Site description</p>
            <ul class="actions">
                <li><a href="#header" class="button icon solid solo fa-arrow-down scrolly">Continue</a></li>
            </ul>
        </div>
        
        <!-- Header -->
        <header id="header">
            <a href="index.html" class="logo">Logo</a>
        </header>
        
        <!-- Nav -->
        <nav id="nav">
            <ul class="links">
                <li class="active"><a href="index.html">Home</a></li>
                <li><a href="generic.html">Generic</a></li>
                <li><a href="elements.html">Elements</a></li>
            </ul>
            <ul class="icons">
                <li><a href="#" class="icon brands fa-twitter"><span class="label">Twitter</span></a></li>
                <li><a href="#" class="icon brands fa-facebook-f"><span class="label">Facebook</span></a></li>
                <li><a href="#" class="icon brands fa-instagram"><span class="label">Instagram</span></a></li>
                <li><a href="#" class="icon brands fa-github"><span class="label">GitHub</span></a></li>
            </ul>
        </nav>
        
        <!-- Main Content -->
        <div id="main">
            <!-- Page content goes here -->
        </div>
        
        <!-- Footer -->
        <footer id="footer">
            <!-- Footer content -->
        </footer>
        
        <!-- Copyright -->
        <div id="copyright">
            <ul><li>&copy; Your Name</li><li>Design: <a href="https://html5up.net">HTML5 UP</a></li></ul>
        </div>
        
    </div>
    
    <!-- Scripts -->
    <script src="assets/js/jquery.min.js"></script>
    <script src="assets/js/jquery.scrollex.min.js"></script>
    <script src="assets/js/jquery.scrolly.min.js"></script>
    <script src="assets/js/browser.min.js"></script>
    <script src="assets/js/breakpoints.min.js"></script>
    <script src="assets/js/util.js"></script>
    <script src="assets/js/main.js"></script>
</body>
</html>
```

### Article Components

#### Featured Post
```html
<article class="post featured">
    <header class="major">
        <span class="date">April 25, 2017</span>
        <h2><a href="#">Featured Article Title</a></h2>
        <p>Article subtitle or excerpt</p>
    </header>
    <a href="#" class="image main">
        <img src="images/pic01.jpg" alt="" />
    </a>
    <p>Article content goes here...</p>
    <ul class="actions special">
        <li><a href="#" class="button large">Full Story</a></li>
    </ul>
</article>
```

#### Regular Post
```html
<article>
    <header>
        <span class="date">April 24, 2017</span>
        <h2><a href="#">Article Title</a></h2>
    </header>
    <a href="#" class="image fit">
        <img src="images/pic02.jpg" alt="" />
    </a>
    <p>Article excerpt...</p>
    <ul class="actions special">
        <li><a href="#" class="button">Full Story</a></li>
    </ul>
</article>
```

#### Posts Grid
```html
<section class="posts">
    <article>
        <!-- Post content -->
    </article>
    <article>
        <!-- Post content -->
    </article>
    <!-- More articles... -->
</section>
```

### Footer Components

#### Contact Form Footer
```html
<footer id="footer">
    <section>
        <form method="post" action="#">
            <div class="fields">
                <div class="field">
                    <label for="name">Name</label>
                    <input type="text" name="name" id="name" />
                </div>
                <div class="field">
                    <label for="email">Email</label>
                    <input type="text" name="email" id="email" />
                </div>
                <div class="field">
                    <label for="message">Message</label>
                    <textarea name="message" id="message" rows="3"></textarea>
                </div>
            </div>
            <ul class="actions">
                <li><input type="submit" value="Send Message" /></li>
            </ul>
        </form>
    </section>
    
    <section class="split contact">
        <section class="alt">
            <h3>Address</h3>
            <p>1234 Somewhere Road #87257<br />
            Nashville, TN 00000-0000</p>
        </section>
        <section>
            <h3>Phone</h3>
            <p><a href="#">(000) 000-0000</a></p>
        </section>
        <section>
            <h3>Email</h3>
            <p><a href="#">info@untitled.tld</a></p>
        </section>
        <section>
            <h3>Social</h3>
            <ul class="icons alt">
                <li><a href="#" class="icon brands alt fa-twitter"><span class="label">Twitter</span></a></li>
                <li><a href="#" class="icon brands alt fa-facebook-f"><span class="label">Facebook</span></a></li>
                <li><a href="#" class="icon brands alt fa-instagram"><span class="label">Instagram</span></a></li>
                <li><a href="#" class="icon brands alt fa-github"><span class="label">GitHub</span></a></li>
            </ul>
        </section>
    </section>
</footer>
```

## Usage Examples

### Creating a New Page

1. **Copy the basic template** from `generic.html`
2. **Update the title** and meta information
3. **Modify the navigation** to highlight the active page
4. **Add your content** inside `#main`
5. **Update footer information** as needed

### Adding a New Project Card

```html
<article>
    <header>
        <h2><a href="project-link.html">Project Title</a></h2>
    </header>
    <a href="project-link.html" class="image fit">
        <img src="images/project-image.jpg" alt="Project Description" />
    </a>
    <p>Brief project description...</p>
    <ul class="actions special">
        <li><a href="project-link.html" class="button">View Project</a></li>
    </ul>
</article>
```

### Implementing Parallax Background

1. **Add background image** to your element:
```css
#wrapper {
    background-image: url('images/bg.jpg');
    background-size: cover;
    background-position: center;
}
```

2. **Enable parallax effect**:
```javascript
$('#wrapper')._parallax(0.925);
```

### Creating a Contact Form

```html
<form method="post" action="contact-handler.php">
    <div class="row gtr-uniform">
        <div class="col-6 col-12-xsmall">
            <input type="text" name="name" placeholder="Name" required />
        </div>
        <div class="col-6 col-12-xsmall">
            <input type="email" name="email" placeholder="Email" required />
        </div>
        <div class="col-12">
            <select name="subject" required>
                <option value="">- Subject -</option>
                <option value="general">General Inquiry</option>
                <option value="support">Support</option>
                <option value="business">Business</option>
            </select>
        </div>
        <div class="col-12">
            <textarea name="message" placeholder="Message" rows="6" required></textarea>
        </div>
        <div class="col-12">
            <ul class="actions">
                <li><input type="submit" value="Send Message" class="primary" /></li>
                <li><input type="reset" value="Reset" /></li>
            </ul>
        </div>
    </div>
</form>
```

### Adding Social Media Links

```html
<ul class="icons alt">
    <li><a href="https://twitter.com/yourusername" class="icon brands alt fa-twitter" target="_blank">
        <span class="label">Twitter</span></a></li>
    <li><a href="https://facebook.com/yourusername" class="icon brands alt fa-facebook-f" target="_blank">
        <span class="label">Facebook</span></a></li>
    <li><a href="https://instagram.com/yourusername" class="icon brands alt fa-instagram" target="_blank">
        <span class="label">Instagram</span></a></li>
    <li><a href="https://github.com/yourusername" class="icon brands alt fa-github" target="_blank">
        <span class="label">GitHub</span></a></li>
    <li><a href="https://linkedin.com/in/yourusername" class="icon brands alt fa-linkedin" target="_blank">
        <span class="label">LinkedIn</span></a></li>
</ul>
```

## Responsive Design

### Mobile Navigation

The template automatically creates a mobile navigation panel that appears on smaller screens. The navigation is converted using the `navList()` function and displayed in a slide-out panel.

### Responsive Images

All images should be wrapped in appropriate containers for responsive behavior:

```html
<!-- For full-width images -->
<span class="image fit">
    <img src="image.jpg" alt="Description" />
</span>

<!-- For content images with text wrapping -->
<span class="image left">
    <img src="image.jpg" alt="Description" />
</span>
```

### Responsive Text

Text automatically scales with screen size, but you can control visibility with responsive classes:

```html
<!-- Hide on small screens -->
<p class="hide-small">This text is hidden on small screens</p>

<!-- Show only on mobile -->
<p class="show-mobile">This text only appears on mobile</p>
```

## Customization Guide

### Changing Colors

Main color variables are defined in the CSS. Key color classes include:

- **Primary color**: Used for `.button.primary`, active states
- **Accent color**: Used for links, highlights
- **Background colors**: Main backgrounds, overlays
- **Text colors**: Body text, headings, muted text

### Customizing Fonts

The template uses Google Fonts by default:
- **Headings**: Source Sans Pro (900 weight)
- **Body text**: Merriweather (300, 700 weights)

To change fonts, modify the `@import` statement in `main.css`:

```css
@import url("https://fonts.googleapis.com/css?family=Your+Font+Family");
```

### Adding Custom JavaScript

Add custom JavaScript after the main scripts:

```html
<script src="assets/js/main.js"></script>
<script>
    // Your custom JavaScript here
    $(document).ready(function() {
        // Custom initialization code
    });
</script>
```

### Performance Optimization

1. **Optimize images**: Use WebP format when possible
2. **Minify CSS/JS**: Combine and minify custom additions
3. **Lazy loading**: Implement lazy loading for images
4. **CDN**: Use CDN for jQuery and Font Awesome if preferred

### Browser Support

The template supports:
- **Modern browsers**: Chrome, Firefox, Safari, Edge
- **Mobile browsers**: iOS Safari, Chrome Mobile, Samsung Internet
- **Legacy support**: IE11+ (with polyfills)

### Accessibility Features

The template includes:
- **Semantic HTML**: Proper heading hierarchy, landmarks
- **Keyboard navigation**: All interactive elements are keyboard accessible
- **Screen reader support**: Proper labels and ARIA attributes
- **Focus management**: Visible focus indicators
- **Color contrast**: WCAG AA compliant color ratios

### SEO Optimization

For better SEO:
1. **Add meta descriptions** to each page
2. **Use structured data** for articles/projects
3. **Optimize image alt text**
4. **Implement proper heading hierarchy**
5. **Add Open Graph meta tags** for social sharing

This documentation covers all the major APIs, components, and usage patterns for the portfolio website template. The framework is designed to be flexible and extensible while maintaining a consistent visual design and user experience across different devices and screen sizes.