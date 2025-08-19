# HTML Complete Guide for Interview Preparation

This README covers all essential HTML concepts with practical examples, perfect for machine coding rounds and technical interviews.

## Table of Contents

### HTML Topics
1. [Introducing HTML](#introducing-html)
2. [Basic HTML Workflow](#basic-html-workflow)
3. [Document Structure](#document-structure)
4. [Paragraph Element](#paragraph-element)
5. [HTML Comments](#html-comments)
6. [Headings](#headings)
7. [HTML Lists](#html-lists)
8. [Text Formatting Elements](#text-formatting-elements)
9. [Nesting Elements](#nesting-elements)
10. [Superscript and Subscript](#superscript-and-subscript)
11. [Inline vs Block Elements](#inline-vs-block-elements)
12. [Creating Links](#creating-links)
13. [Images](#images)
14. [Forms and Inputs](#forms-and-inputs)
15. [Form Controls](#form-controls)
16. [Advanced Form Elements](#advanced-form-elements)
17. [Spans and Divs](#spans-and-divs)
18. [Tables](#tables)
19. [Semantic Markup](#semantic-markup)

## Introducing HTML

HTML (HyperText Markup Language) is the standard markup language for creating web pages. It describes the structure of a web page using elements and tags.

### Key Points:
- HTML uses tags to define elements
- Tags are enclosed in angle brackets `< >`
- Most tags have opening and closing pairs
- HTML is not case-sensitive (but lowercase is recommended)

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Hello World!</h1>
</body>
</html>
```

## Basic HTML Workflow

### Development Process:
1. Create an HTML file with `.html` extension
2. Write HTML markup
3. Open in a web browser to view
4. Use developer tools for debugging
5. Validate your HTML

### Essential Tools:
- **Text Editor**: VS Code, Sublime Text, Atom
- **Browser**: Chrome, Firefox, Safari
- **Developer Tools**: F12 in most browsers
- **Mozilla Developer Network (MDN)**: Best resource for HTML documentation

## Document Structure

Every HTML document follows a standard structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document Title</title>
</head>
<body>
    <!-- Content goes here -->
</body>
</html>
```

### Key Elements:
- `<!DOCTYPE html>`: Declares HTML5 document type
- `<html>`: Root element
- `<head>`: Contains metadata
- `<body>`: Contains visible content

## Paragraph Element

The `<p>` tag defines paragraphs of text.

```html
<p>This is a paragraph of text.</p>
<p>This is another paragraph. Paragraphs are block-level elements.</p>
<p>Multiple spaces     and line breaks
   are collapsed into single spaces.</p>
```

### Interview Tip:
Paragraphs automatically add margins and are block-level elements.

## HTML Comments

Comments are not displayed in the browser but help document your code.

```html
<!-- This is a single-line comment -->

<!-- 
This is a 
multi-line comment
Very useful for documentation
-->

<p>This paragraph is visible</p>
<!-- <p>This paragraph is commented out</p> -->
```

## Headings

HTML provides 6 heading levels from `<h1>` to `<h6>`.

```html
<h1>Main Heading (Most Important)</h1>
<h2>Sub Heading</h2>
<h3>Sub-sub Heading</h3>
<h4>Level 4 Heading</h4>
<h5>Level 5 Heading</h5>
<h6>Smallest Heading</h6>
```

### Best Practices:
- Use only one `<h1>` per page
- Don't skip heading levels
- Use headings for structure, not styling

## HTML Lists

HTML supports three types of lists:

### Unordered Lists (Bulleted)
```html
<ul>
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

### Ordered Lists (Numbered)
```html
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>
```

### Description Lists
```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
    <dt>CSS</dt>
    <dd>Cascading Style Sheets</dd>
</dl>
```

## Text Formatting Elements

### Em, Strong, B, and I Elements

```html
<!-- Semantic emphasis -->
<em>Emphasized text (usually italic)</em>
<strong>Important text (usually bold)</strong>

<!-- Visual formatting -->
<i>Italic text</i>
<b>Bold text</b>

<!-- Modern usage -->
<p>This is <strong>very important</strong> information.</p>
<p>The term <em>semantics</em> refers to meaning.</p>
```

### Interview Note:
- `<em>` and `<strong>` are semantic (meaning-based)
- `<i>` and `<b>` are presentational (appearance-based)

## Nesting Elements

Elements can contain other elements:

```html
<p>This paragraph contains <strong>bold text</strong> and <em>italic text</em>.</p>

<ul>
    <li>Item 1 with <a href="#">a link</a></li>
    <li>Item 2 with <strong>bold text</strong></li>
</ul>
```

### Rules:
- Properly close nested elements
- Block elements can contain inline elements
- Inline elements cannot contain block elements (with exceptions)

## Superscript and Subscript

```html
<!-- Mathematical expressions -->
<p>E = mc<sup>2</sup></p>
<p>H<sub>2</sub>O is the chemical formula for water</p>

<!-- Footnotes -->
<p>This statement needs a reference<sup>1</sup></p>
```

## Inline vs Block Elements

### Block Elements
- Take full width available
- Start on new line
- Examples: `<div>`, `<p>`, `<h1>-<h6>`, `<ul>`, `<li>`

### Inline Elements
- Take only necessary width
- Don't start on new line
- Examples: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`

```html
<!-- Block elements -->
<div>This is a block element</div>
<div>This starts on a new line</div>

<!-- Inline elements -->
<span>This is inline</span> <span>This continues on the same line</span>
```

## Creating Links

### Basic Links
```html
<a href="https://www.google.com">Visit Google</a>
<a href="about.html">About Page</a>
<a href="#section1">Jump to Section 1</a>
```

### Other Types of Links
```html
<!-- Email link -->
<a href="mailto:someone@example.com">Send Email</a>

<!-- Phone link -->
<a href="tel:+1234567890">Call Us</a>

<!-- Download link -->
<a href="document.pdf" download>Download PDF</a>

<!-- New tab -->
<a href="https://example.com" target="_blank" rel="noopener">External Link</a>
```

## Images

```html
<!-- Basic image -->
<img src="image.jpg" alt="Description of image">

<!-- Image with dimensions -->
<img src="photo.jpg" alt="A beautiful sunset" width="400" height="300">

<!-- Responsive image -->
<img src="image.jpg" alt="Description" style="max-width: 100%; height: auto;">
```

### Best Practices:
- Always include `alt` attribute for accessibility
- Optimize images for web
- Use appropriate file formats (JPEG, PNG, SVG, WebP)

## Forms and Inputs

### Basic Form Structure
```html
<form action="/submit" method="POST">
    <input type="text" name="username" placeholder="Enter username">
    <input type="password" name="password" placeholder="Enter password">
    <button type="submit">Submit</button>
</form>
```

### Text Inputs and Buttons
```html
<input type="text" placeholder="Your name">
<input type="email" placeholder="your@email.com">
<input type="password" placeholder="Password">
<button type="button">Click Me</button>
<button type="submit">Submit Form</button>
<button type="reset">Reset Form</button>
```

## Form Controls

### Proper Labelling
```html
<!-- Method 1: Using for attribute -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<!-- Method 2: Wrapping input -->
<label>
    Email:
    <input type="email" name="email">
</label>
```

### Various Input Types
```html
<input type="text" placeholder="Text input">
<input type="email" placeholder="Email input">
<input type="password" placeholder="Password">
<input type="number" min="1" max="100">
<input type="date">
<input type="time">
<input type="url" placeholder="https://example.com">
<input type="search" placeholder="Search...">
```

## Advanced Form Elements

### Checkboxes, Textareas, and Range Inputs
```html
<!-- Checkboxes -->
<input type="checkbox" id="agree" name="agree">
<label for="agree">I agree to terms</label>

<!-- Textarea -->
<textarea name="message" rows="4" cols="50" placeholder="Your message"></textarea>

<!-- Range input -->
<label for="volume">Volume:</label>
<input type="range" id="volume" name="volume" min="0" max="100" value="50">
```

### Selects and Radio Button Groupings
```html
<!-- Select dropdown -->
<select name="country">
    <option value="">Choose a country</option>
    <option value="us">United States</option>
    <option value="ca">Canada</option>
    <option value="uk">United Kingdom</option>
</select>

<!-- Radio buttons -->
<fieldset>
    <legend>Choose your favorite color:</legend>
    <input type="radio" id="red" name="color" value="red">
    <label for="red">Red</label>
    
    <input type="radio" id="blue" name="color" value="blue">
    <label for="blue">Blue</label>
    
    <input type="radio" id="green" name="color" value="green">
    <label for="green">Green</label>
</fieldset>
```

## Spans and Divs

### Spans (Inline)
```html
<p>This paragraph has <span style="color: red;">red text</span> in the middle.</p>
<p>Price: <span class="currency">$29.99</span></p>
```

### Divs (Block)
```html
<div class="container">
    <div class="header">
        <h1>Website Title</h1>
    </div>
    <div class="content">
        <p>Main content goes here</p>
    </div>
    <div class="footer">
        <p>&copy; 2024 Website Name</p>
    </div>
</div>
```

## Tables

```html
<table>
    <caption>Monthly Sales Report</caption>
    <thead>
        <tr>
            <th>Month</th>
            <th>Sales</th>
            <th>Growth</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>January</td>
            <td>$10,000</td>
            <td>5%</td>
        </tr>
        <tr>
            <td>February</td>
            <td>$12,000</td>
            <td>20%</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td>Total</td>
            <td>$22,000</td>
            <td>12.5%</td>
        </tr>
    </tfoot>
</table>
```

## Semantic Markup

Semantic HTML provides meaning to your content:

### Semantic Elements
```html
<!DOCTYPE html>
<html>
<head>
    <title>Semantic HTML Example</title>
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <article>
            <header>
                <h1>Article Title</h1>
                <p>Published on <time datetime="2024-01-15">January 15, 2024</time></p>
            </header>
            
            <section>
                <h2>Introduction</h2>
                <p>Article content goes here...</p>
            </section>
            
            <section>
                <h2>Main Content</h2>
                <p>More article content...</p>
            </section>
        </article>

        <aside>
            <h3>Related Articles</h3>
            <ul>
                <li><a href="#">Related Article 1</a></li>
                <li><a href="#">Related Article 2</a></li>
            </ul>
        </aside>
    </main>

    <footer>
        <p>&copy; 2024 Your Website. All rights reserved.</p>
    </footer>
</body>
</html>
```

### Key Semantic Elements:
- `<header>`: Page or section header
- `<nav>`: Navigation links
- `<main>`: Main content area
- `<article>`: Independent content
- `<section>`: Thematic grouping
- `<aside>`: Sidebar content
- `<footer>`: Page or section footer
- `<figure>` and `<figcaption>`: Images with captions
- `<time>`: Dates and times
- `<address>`: Contact information

## Interview Tips

### Common Questions:
1. **Difference between block and inline elements?**
   - Block: Full width, new line, can contain other elements
   - Inline: Content width only, same line, limited nesting

2. **What is semantic HTML?**
   - HTML that provides meaning, not just presentation
   - Better for SEO, accessibility, and maintainability

3. **Form validation attributes?**
   ```html
   <input type="email" required>
   <input type="text" pattern="[A-Za-z]{3}" title="Three letter country code">
   <input type="number" min="18" max="100">
   ```

4. **Accessibility considerations?**
   - Use semantic elements
   - Provide alt text for images
   - Label form controls
   - Use proper heading hierarchy

### Best Practices:
- Always validate your HTML
- Use semantic elements when possible
- Keep your code clean and well-indented
- Include proper meta tags
- Test across different browsers
- Consider accessibility from the start

---

*This guide covers essential HTML concepts for interview preparation. Practice building complete web pages using these elements!*

---

# CSS Complete Guide for Interview Preparation

This section covers essential CSS concepts with practical examples, perfect for interviews and coding rounds.

## Table of Contents

### CSS Topics
20. [Getting Our Starter Code](#getting-our-starter-code)
21. [Working Within Inline Styles](#working-within-inline-styles)
22. [Writing Internal Styles](#writing-internal-styles)
23. [External Styles: The Best Way To Write Styles](#external-styles-the-best-way-to-write-styles)
24. [Quick Note on Codepen](#quick-note-on-codepen)
25. [Anatomy of CSS](#anatomy-of-css)
26. [The Element Selector](#the-element-selector)
27. [CSS Basics Exercise](#css-basics-exercise)
28. [Working with background-color](#working-with-background-color)
29. [Quick Tip: MDN & Comments](#quick-tip-mdn--comments)
30. [Named Colors](#named-colors)
31. [Understanding RGB Colors](#understanding-rgb-colors)
32. [Hexadecimal Colors](#hexadecimal-colors)
33. [RGBA Colors and Opacity](#rgba-colors-and-opacity)
34. [Colors Quiz](#colors-quiz)
35. [CSS Inheritance](#css-inheritance)
36. [CSS Colors Exercise](#css-colors-exercise)
37. [Changing Fonts with Font-Family](#changing-fonts-with-font-family)
38. [Font-size, font-weight, and font-style](#font-size-font-weight-and-font-style)
39. [Changing Text Alignment](#changing-text-alignment)
40. [Line-height, letter-spacing, and word-spacing](#line-height-letter-spacing-and-word-spacing)
41. [Adding Custom Fonts With Google Fonts](#adding-custom-fonts-with-google-fonts)
42. [Styling Text Exercise](#styling-text-exercise)
43. [Creating Text Shadows](#creating-text-shadows)
44. [Our First Mini Project: Cantilever](#our-first-mini-project-cantilever)
45. [Text-transform & text-decoration](#text-transform--text-decoration)
46. [The ID Selector](#the-id-selector)
47. [The Class Selector](#the-class-selector)
48. [Styling Lists](#styling-lists)
49. [Styling Links and :hover Pseudo-Class](#styling-links-and-hover-pseudo-class)
50. [The Font Shorthand Property](#the-font-shorthand-property)
51. [Leafy Seadragon Exercise](#leafy-seadragon-exercise)
52. [The Universal Selector](#the-universal-selector)
53. [The Attribute Selector](#the-attribute-selector)
54. [Grouping Selectors](#grouping-selectors)
55. [Descendant & Child Combinators](#descendant--child-combinators)
56. [Compound Selectors](#compound-selectors)
57. [CSS Selectors Exercise](#css-selectors-exercise)
58. [Introducing The Box Model](#introducing-the-box-model)
59. [Working With Borders](#working-with-borders)
60. [Width, Height, and Percentages](#width-height-and-percentages)
61. [Adding Padding to Elements](#adding-padding-to-elements)
62. [Working With Margins](#working-with-margins)
63. [The Alternate Box Model](#the-alternate-box-model)
64. [The Display Property](#the-display-property)
65. [Display: None](#display-none)
66. [Negative Margin & Margin Auto](#negative-margin--margin-auto)
67. [Margin Collapsing: WTF?](#margin-collapsing-wtf)
68. [A Common Layout Pattern](#a-common-layout-pattern)
69. [Min and Max Width](#min-and-max-width)
70. [Rounding Elements With Border Radius](#rounding-elements-with-border-radius)
71. [Box Shadows](#box-shadows)
72. [Working With Overflow](#working-with-overflow)
73. [Ski Resort Exercise](#ski-resort-exercise)
74. [Introducing Flexbox](#introducing-flexbox)
75. [Display: Flex and Flex Axis](#display-flex-and-flex-axis)
76. [Working With Flex-Direction](#working-with-flex-direction)
77. [Flexbox Exercise 1](#flexbox-exercise-1)
78. [Flex-Wrap](#flex-wrap)
79. [Justify-Content](#justify-content)
80. [Flexbox Exercise 2](#flexbox-exercise-2)
81. [Align-Items](#align-items)
82. [Flexbox Exercise 3](#flexbox-exercise-3)
83. [Align-Content](#align-content)
84. [Flexbox Exercise 4](#flexbox-exercise-4)
85. [Align-Self](#align-self)
86. [Flexbox Exercise 5](#flexbox-exercise-5)
87. [The Flex-Grow Property](#the-flex-grow-property)
88. [Controlling Shrinkage With Flex-Shrink](#controlling-shrinkage-with-flex-shrink)
89. [Flex-Basis: Important & Confusing](#flex-basis-important--confusing)
90. [The Flex Shorthand Property](#the-flex-shorthand-property)
91. [The Order Flex-Item Property](#the-order-flex-item-property)
92. [Flexbox Patterns: Building A Simple Navbar](#flexbox-patterns-building-a-simple-navbar)
93. [Flexbox Patterns: Nested Flex Containers](#flexbox-patterns-nested-flex-containers)
94. [Flexbox Patterns: Centering Content](#flexbox-patterns-centering-content)
95. [Flexbox Patterns: Building A Card Layout](#flexbox-patterns-building-a-card-layout)

---

## Getting Our Starter Code

**Description:**  
Start with a basic HTML file before applying CSS. This is your foundation for styling.

Before writing CSS, you need an HTML file to style. Download or create a basic HTML file:

```html
<!DOCTYPE html>
<html>
<head>
    <title>CSS Starter</title>
</head>
<body>
    <h1>Hello CSS!</h1>
    <p>This is a starter file for CSS practice.</p>
</body>
</html>
```

---

## Working Within Inline Styles

**Description:**  
Inline styles are CSS rules applied directly to an HTML element using the `style` attribute. They override internal and external styles but are not recommended for maintainability.

Inline styles are added directly to HTML elements using the `style` attribute.

```html
<p style="color: blue; font-size: 18px;">This text is blue and larger.</p>
```

**Note:** Inline styles override other styles but are not recommended for large projects.

---

## Writing Internal Styles

**Description:**  
Internal styles are CSS rules placed inside a `<style>` tag within the `<head>` of your HTML. They apply to the whole document but are only available in that file.

Internal styles are placed inside a `<style>` tag in the `<head>` section.

```html
<head>
    <style>
        p {
            color: green;
            font-size: 20px;
        }
    </style>
</head>
```

---

## External Styles: The Best Way To Write Styles

**Description:**  
External styles are written in a separate `.css` file and linked to your HTML. This is the best practice for maintainability and reusability.

External styles are written in a separate `.css` file and linked to your HTML.

**style.css**
```css
body {
    background-color: #f0f0f0;
}
h1 {
    color: #333;
}
```

**Link in HTML:**
```html
<link rel="stylesheet" href="style.css">
```

---

## Quick Note on Codepen

**Description:**  
CodePen is an online playground for HTML, CSS, and JS. Use it to quickly prototype, test, and share code snippets.

[CodePen](https://codepen.io/) is an online code editor for HTML, CSS, and JS. Great for quick experiments and sharing code.

---

## Anatomy of CSS

**Description:**  
A CSS rule consists of a selector (what to style) and a declaration block (how to style it). Each declaration is a property-value pair.

A CSS rule consists of a selector and a declaration block.

```css
selector {
    property: value;
    property2: value2;
}
```

Example:
```css
p {
    color: red;
    font-size: 16px;
}
```

---

## The Element Selector

**Description:**  
Selects all elements of a given type (e.g., `p`, `h1`). Used for broad styling.

Selects all elements of a given type.

```css
h2 {
    color: purple;
}
```

---

## CSS Basics Exercise

**Description:**  
Practice using selectors and properties to change the appearance of elements.

Try changing the color and font size of all `<p>` elements.

```css
p {
    color: navy;
    font-size: 18px;
}
```

---

## Working with background-color

**Description:**  
The `background-color` property sets the background color of an element.

Set the background color of elements.

```css
body {
    background-color: #e0e0e0;
}
div {
    background-color: yellow;
}
```

---

## Quick Tip: MDN & Comments

**Description:**  
MDN is the best reference for CSS. Use comments (`/* ... */`) to document your CSS code.

- Use [MDN Web Docs](https://developer.mozilla.org/) for CSS reference.
- Add comments in CSS with `/* comment */`.

```css
/* This is a CSS comment */
h1 {
    color: teal;
}
```

---

## Named Colors

**Description:**  
CSS supports over 140 named colors (e.g., `red`, `blue`, `tomato`). Use them for quick color assignments.

CSS supports 140+ named colors.

```css
p {
    color: tomato;
    background-color: lightyellow;
}
```

---

## Understanding RGB Colors

**Description:**  
The `rgb()` function defines colors using Red, Green, and Blue values (0-255).

RGB stands for Red, Green, Blue. Each value ranges from 0 to 255.

```css
div {
    background-color: rgb(255, 0, 0); /* Red */
    color: rgb(0, 0, 0); /* Black */
}
```

---

## Hexadecimal Colors

**Description:**  
Hex colors use a `#` followed by 3 or 6 hexadecimal digits to represent color (e.g., `#ff0000` for red).

Hex codes start with `#` and use 6 digits.

```css
body {
    background-color: #ffffff; /* White */
    color: #333333; /* Dark gray */
}
```

---

## RGBA Colors and Opacity

**Description:**  
`rgba()` adds an alpha (opacity) channel to RGB colors. The alpha value ranges from 0 (transparent) to 1 (opaque).

RGBA adds an alpha (opacity) value (0 = transparent, 1 = opaque).

```css
div {
    background-color: rgba(0, 128, 0, 0.5); /* Semi-transparent green */
}
```

---

## Colors Quiz

**Description:**  
Test your understanding of color values and how they render in the browser.

Try to guess the color output for:

```css
p {
    color: #ff6347;
    background: rgb(240, 248, 255);
}
```

---

## CSS Inheritance

**Description:**  
Some CSS properties (like `color`, `font-family`) are inherited by child elements. Others (like `margin`, `padding`) are not.

Some properties are inherited by child elements (e.g., `color`, `font-family`).

```css
body {
    color: darkblue;
}
p {
    /* inherits color from body */
}
```

---

## CSS Colors Exercise

**Description:**  
Practice changing background and text colors using CSS.

Change the background and text color of a div.

```css
div {
    background: #222;
    color: #fff;
}
```

---

## Changing Fonts with Font-Family

**Description:**  
The `font-family` property sets the typeface for text. You can specify multiple fonts as fallbacks.

Set the font for elements.

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

---

## Font-size, font-weight, and font-style

**Description:**  
- `font-size`: Sets the size of the text (e.g., `16px`, `2em`).
- `font-weight`: Sets the thickness (e.g., `normal`, `bold`, `700`).
- `font-style`: Sets style (e.g., `normal`, `italic`, `oblique`).

```css
h1 {
    font-size: 2em;
    font-weight: bold;
    font-style: italic;
}
```

---

## Changing Text Alignment

**Description:**  
The `text-align` property sets the horizontal alignment of text (e.g., `left`, `center`, `right`, `justify`).

```css
p {
    text-align: center;
}
```

---

## Line-height, letter-spacing, and word-spacing

**Description:**  
- `line-height`: Sets the vertical spacing between lines.
- `letter-spacing`: Sets space between letters.
- `word-spacing`: Sets space between words.

```css
p {
    line-height: 1.5;
    letter-spacing: 2px;
    word-spacing: 8px;
}
```

---

## Adding Custom Fonts With Google Fonts

**Description:**  
Import fonts from Google Fonts using a `<link>` tag, then use them in your CSS with `font-family`.

1. Go to [Google Fonts](https://fonts.google.com/)
2. Select a font and copy the `<link>` tag to your HTML `<head>`
3. Use the font in CSS

```html
<link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">
```
```css
body {
    font-family: 'Roboto', sans-serif;
}
```

---

## Styling Text Exercise

**Description:**  
Practice styling headings and paragraphs with color and font-style properties.

Try making all headings blue and all paragraphs italic.

```css
h1, h2, h3, h4, h5, h6 {
    color: blue;
}
p {
    font-style: italic;
}
```

---

## Creating Text Shadows

**Description:**  
The `text-shadow` property adds shadow effects to text. Syntax: `text-shadow: x-offset y-offset blur color;`

```css
h1 {
    text-shadow: 2px 2px 5px gray;
}
```

---

## Our First Mini Project: Cantilever

**Description:**  
Build a simple landing page using headings, paragraphs, and CSS for layout and color. Practice combining multiple CSS properties.

---

## Text-transform & text-decoration

**Description:**  
- `text-transform`: Controls capitalization (`uppercase`, `lowercase`, `capitalize`).
- `text-decoration`: Adds decoration to text (`underline`, `line-through`, `none`).

```css
h2 {
    text-transform: uppercase;
}
a {
    text-decoration: none;
}
```

---

## The ID Selector

**Description:**  
Selects an element by its unique `id` attribute using `#idname`. Used for targeting single elements.

Selects a single element by its unique ID.

```css
#main-title {
    color: orange;
}
```

---

## The Class Selector

**Description:**  
Selects all elements with a given `class` attribute using `.classname`. Used for reusable styles.

Selects all elements with a given class.

```css
.highlight {
    background: yellow;
}
```

---

## Styling Lists

**Description:**  
Customize list appearance with properties like `list-style-type`, `padding`, and `margin`.

```css
ul {
    list-style-type: square;
    padding-left: 20px;
}
```

---

## Styling Links and :hover Pseudo-Class

**Description:**  
Style links with `a {}` and use `a:hover {}` for hover effects. Pseudo-classes allow styling based on user interaction.

```css
a {
    color: blue;
    text-decoration: underline;
}
a:hover {
    color: red;
}
```

---

## The Font Shorthand Property

**Description:**  
The `font` shorthand sets `font-style`, `font-variant`, `font-weight`, `font-size`, `line-height`, and `font-family` in one line.

Set multiple font properties at once.

```css
p {
    font: italic bold 16px/1.5 Arial, sans-serif;
}
```

---

## Leafy Seadragon Exercise

**Description:**  
Practice styling an image and its caption using CSS properties like `border`, `margin`, and `font-style`.

---

## The Universal Selector

**Description:**  
The `*` selector targets all elements. Useful for resetting default styles (e.g., margin, padding).

Selects all elements.

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

---

## The Attribute Selector

**Description:**  
Selects elements based on attribute and value (e.g., `input[type="text"]`). Useful for targeting specific form fields.

Select elements by attribute.

```css
input[type="text"] {
    border: 2px solid green;
}
```

---

## Grouping Selectors

**Description:**  
Apply the same styles to multiple selectors by separating them with commas.

Apply the same styles to multiple selectors.

```css
h1, h2, h3 {
    color: teal;
}
```

---

## Descendant & Child Combinators

**Description:**  
- Descendant (`A B`): Selects all `B` inside `A`.
- Child (`A > B`): Selects direct children `B` of `A`.

```css
/* Descendant */
div p {
    color: purple;
}
/* Child */
ul > li {
    font-weight: bold;
}
```

---

## Compound Selectors

**Description:**  
Combine selectors for more specific targeting (e.g., `.menu li.active`).

Combine selectors for more specific targeting.

```css
ul.menu li.active {
    color: red;
}
```

---

## CSS Selectors Exercise

**Description:**  
Practice writing and combining different types of selectors.

Practice writing selectors for different elements and classes.

---

## Introducing The Box Model

**Description:**  
Every element is a box with `content`, `padding`, `border`, and `margin`. Understanding the box model is key to layout.

Every element is a box: content, padding, border, margin.

```css
div {
    width: 200px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```

---

## Working With Borders

**Description:**  
The `border` property adds a border around elements. You can set width, style, color, and radius.

**Insights:**  
- `border: 1px solid #ccc;` — width = 1px, style = solid, color = #ccc.
- `border-width`, `border-style`, `border-color` can be set individually.
- `border-radius: 8px;` — rounds the corners (see below for more).

```css
p {
    border: 1px solid #ccc;
    border-radius: 8px;
}
```

---

## Width, Height, and Percentages

**Description:**  
Set the size of elements using `width`, `height`, and percentage values for responsive design.

**Insights:**  
- `width: 200px;` — sets width to 200 pixels.
- `height: 100px;` — sets height to 100 pixels.
- `width: 50%;` — sets width to 50% of the parent element.
- `height: auto;` — height adjusts automatically to maintain aspect ratio (commonly used with images).

```css
img {
    width: 50%;
    height: auto;
}
```

---

## Adding Padding to Elements

**Description:**  
The `padding` property adds space inside the border, around the content.

**Insights:**  
- `padding: 10px;` — sets all four sides to 10px.
- `padding: 10px 20px;` — top/bottom = 10px, left/right = 20px.
- `padding: 10px 20px 30px;` — top = 10px, left/right = 20px, bottom = 30px.
- `padding: 10px 20px 30px 40px;` — top = 10px, right = 20px, bottom = 30px, left = 40px (clockwise: top, right, bottom, left).

```css
button {
    padding: 10px 20px;
}
```

---

## Working With Margins

**Description:**  
The `margin` property adds space outside the border, separating elements from each other.

**Insights:**  
- `margin: 10px;` — all sides 10px.
- `margin: 10px 20px;` — top/bottom = 10px, left/right = 20px.
- `margin: 10px 20px 30px;` — top = 10px, left/right = 20px, bottom = 30px.
- `margin: 10px 20px 30px 40px;` — top = 10px, right = 20px, bottom = 30px, left = 40px.
- `margin: auto;` — horizontally centers block elements if width is set.

```css
h2 {
    margin-top: 30px;
    margin-bottom: 10px;
}
```

---

## The Alternate Box Model

**Description:**  
`box-sizing: border-box` includes padding and border in the element's total width and height, making layouts easier.

**Insights:**  
- By default, `width` and `height` only include the content box.
- With `box-sizing: border-box;`, padding and border are included in the width/height, so the element doesn't grow unexpectedly.

```css
* {
    box-sizing: border-box;
}
```

---

## Rounding Elements With Border Radius

**Description:**  
The `border-radius` property rounds the corners of elements.

**Insights:**  
- `border-radius: 10px;` — all corners rounded by 10px.
- `border-radius: 10px 20px;` — top-left/bottom-right = 10px, top-right/bottom-left = 20px.
- `border-radius: 50%;` — makes a perfect circle if width and height are equal.

```css
img {
    border-radius: 50%;
}
```

---

## Box Shadows

**Description:**  
The `box-shadow` property adds shadow effects to elements.

**Insights:**  
- Syntax: `box-shadow: offset-x offset-y blur-radius color;`
- Example: `box-shadow: 2px 2px 8px rgba(0,0,0,0.2);`
  - `2px` right, `2px` down, `8px` blur, color is semi-transparent black.
- Multiple shadows can be comma-separated.

```css
.box {
    box-shadow: 2px 2px 8px rgba(0,0,0,0.2);
}
```

---

## Working With Overflow

**Description:**  
The `overflow` property controls what happens when content overflows its container.

**Insights:**  
- `overflow: visible;` — default, content spills out.
- `overflow: hidden;` — extra content is clipped.
- `overflow: scroll;` — always shows scrollbars.
- `overflow: auto;` — scrollbars appear only if needed.

```css
div {
    width: 200px;
    height: 100px;
    overflow: auto;
}
```

---

## Negative Margin & Margin Auto

**Description:**  
- Negative margins pull elements closer or overlap them.
- `margin: auto` centers elements horizontally (when width is set).

**Insights:**  
- `margin-left: -20px;` — moves the element 20px to the left, possibly overlapping siblings.
- `margin-right: auto;` — used for horizontal centering in flex/grid or with set width.

```css
div {
    margin-left: -20px;
    margin-right: auto;
}
```

---

## Line-height, letter-spacing, and word-spacing

**Description:**  
- `line-height`: Sets the vertical spacing between lines.
- `letter-spacing`: Sets space between letters.
- `word-spacing`: Sets space between words.

**Insights:**  
- `line-height: 1.5;` — 1.5 times the font size.
- `letter-spacing: 2px;` — adds 2px between each letter.
- `word-spacing: 8px;` — adds 8px between each word.

```css
p {
    line-height: 1.5;
    letter-spacing: 2px;
    word-spacing: 8px;
}
```

---

## Font-size, font-weight, and font-style

**Description:**  
- `font-size`: Sets the size of the text (e.g., `16px`, `2em`).
- `font-weight`: Sets the thickness (e.g., `normal`, `bold`, `700`).
- `font-style`: Sets style (e.g., `normal`, `italic`, `oblique`).

**Insights:**  
- `font-size: 2em;` — 2 times the parent element's font size.
- `font-weight: bold;` or `font-weight: 700;` — makes text bold.
- `font-style: italic;` — italicizes text.

```css
h1 {
    font-size: 2em;
    font-weight: bold;
    font-style: italic;
}
```

---

## Text-transform & text-decoration

**Description:**  
- `text-transform`: Controls capitalization (`uppercase`, `lowercase`, `capitalize`).
- `text-decoration`: Adds decoration to text (`underline`, `line-through`, `none`).

**Insights:**  
- `text-transform: uppercase;` — makes all letters uppercase.
- `text-decoration: none;` — removes underline from links.

```css
h2 {
    text-transform: uppercase;
}
a {
    text-decoration: none;
}
```

---

## The Font Shorthand Property

**Description:**  
The `font` shorthand sets `font-style`, `font-variant`, `font-weight`, `font-size`, `line-height`, and `font-family` in one line.

**Insights:**  
- Syntax: `font: [style] [variant] [weight] [size]/[line-height] [family];`
- Example: `font: italic bold 16px/1.5 Arial, sans-serif;`

```css
p {
    font: italic bold 16px/1.5 Arial, sans-serif;
}
```

---

## The Display Property

**Description:**  
The `display` property controls how an element is rendered (`block`, `inline`, `inline-block`, `none`, etc.).

**Insights:**  
- `display: block;` — element starts on a new line, takes full width.
- `display: inline;` — element flows inline, only as wide as content.
- `display: inline-block;` — inline flow, but can set width/height.
- `display: none;` — element is removed from layout.

```css
span {
    display: block;
}
div {
    display: inline-block;
}
```

---

## Display: None

**Description:**  
`display: none` hides an element from the page (it takes up no space).

Hide elements from the page.

```css
.hidden {
    display: none;
}
```

---

## Negative Margin & Margin Auto

**Description:**  
- Negative margins pull elements closer or overlap them.
- `margin: auto` centers elements horizontally (when width is set).

```css
div {
    margin-left: -20px;
    margin-right: auto;
}
```

---

## Margin Collapsing: WTF?

**Description:**  
Vertical margins of adjacent block elements may combine (collapse) into a single margin.

Adjacent vertical margins may combine into one. Test with stacked elements.

---

## A Common Layout Pattern

**Description:**  
Use containers, rows, and columns (often with Flexbox) to create responsive layouts.

Use containers and columns for layout.

```css
.container {
    width: 80%;
    margin: 0 auto;
}
.row {
    display: flex;
}
.col {
    flex: 1;
}
```

---

## Min and Max Width

**Description:**  
- `min-width`/`max-width` set the minimum/maximum width of an element.
- Useful for responsive design.

```css
img {
    min-width: 100px;
    max-width: 400px;
}
```

---

## Rounding Elements With Border Radius

**Description:**  
The `border-radius` property rounds the corners of elements. `50%` makes circles.

```css
img {
    border-radius: 50%;
}
```

---

## Box Shadows

**Description:**  
The `box-shadow` property adds shadow effects to elements. Syntax: `box-shadow: x-offset y-offset blur color;`

```css
.box {
    box-shadow: 2px 2px 8px rgba(0,0,0,0.2);
}
```

---

## Working With Overflow

**Description:**  
The `overflow` property controls what happens when content overflows its container (`visible`, `hidden`, `scroll`, `auto`).

```css
div {
    width: 200px;
    height: 100px;
    overflow: auto;
}
```

---

## Ski Resort Exercise

**Description:**  
Apply all learned CSS concepts to build a visually appealing card or section for a ski resort.

Build a styled card or section for a ski resort using all the above CSS concepts.

---

## The Sibling Combinator

**Description:**  
The sibling combinator (`A + B` or `A ~ B`) selects elements that are siblings (share the same parent).

**Insights:**  
- `A + B` selects the first `B` immediately after `A`.
- `A ~ B` selects all `B` siblings after `A`.

```css
h2 + p {
    color: orange; /* Styles the first <p> after an <h2> */
}
h2 ~ p {
    color: green; /* Styles all <p> after an <h2> */
}
```

---

## Working With Pseudo-Classes

**Description:**  
Pseudo-classes select elements based on their state or position.

**Insights:**  
- `:hover` — when mouse is over an element.
- `:active` — when element is being activated (e.g., clicked).
- `:focus` — when element is focused (e.g., input).
- `:nth-child(n)` — selects the nth child.
- `:first-child`, `:last-child` — select first/last child.

```css
a:hover {
    color: red;
}
li:nth-child(odd) {
    background: #eee;
}
input:focus {
    border-color: blue;
}
```

---

## Styling Pseudo-Elements

**Description:**  
Pseudo-elements style specific parts of elements.

**Insights:**  
- `::before` and `::after` — insert content before/after element content.
- `::first-line` — styles the first line of text.
- `::first-letter` — styles the first letter.

```css
p::first-line {
    font-weight: bold;
}
p::first-letter {
    font-size: 2em;
}
button::after {
    content: " →";
}
```

---

## CSS Selectors Pt. 2 Exercise

**Description:**  
Practice using sibling combinators, pseudo-classes, and pseudo-elements to style elements in various scenarios.

---

## The Basics of Specificity

**Description:**  
Specificity determines which CSS rule applies when multiple rules target the same element.

**Insights:**  
- Inline styles > IDs > Classes/attributes/pseudo-classes > Elements/pseudo-elements.
- More specific selectors override less specific ones.

---

## Inline Styles and Specificity

**Description:**  
Inline styles (using the `style` attribute) have the highest specificity (except for `!important`).

**Insights:**  
- Inline styles override external and internal CSS unless `!important` is used elsewhere.

---

## Calculating Specificity Values

**Description:**  
Specificity is calculated as a score:  
- Inline styles: 1000  
- ID selectors: 100  
- Class/attribute/pseudo-class: 10  
- Element/pseudo-element: 1

**Insights:**  
- Add up the values for each selector in a rule to determine which wins.

---

## !important and The Cascade

**Description:**  
The `!important` flag forces a CSS rule to override any other, regardless of specificity.

**Insights:**  
- Use sparingly; can make debugging harder.
- Example: `color: red !important;`

---

## Absolute Units: Pixels, Centimeters, and More!

**Description:**  
Absolute units are fixed and not relative to anything else.

**Insights:**  
- `px` (pixels), `cm` (centimeters), `mm` (millimeters), `in` (inches), `pt` (points), `pc` (picas).
- `px` is most common for screens.

```css
div {
    width: 200px;
    height: 50mm;
}
```

---

## Working With Percentages

**Description:**  
Percentages are relative to the parent element's size.

**Insights:**  
- `width: 50%;` — 50% of the parent’s width.
- `font-size: 120%;` — 120% of the parent’s font size.

---

## The Joy of Rem Units

**Description:**  
`rem` units are relative to the root (`<html>`) element's font size.

**Insights:**  
- `1rem` = root font size (default 16px in browsers).
- Useful for consistent, scalable layouts.

```css
html { font-size: 16px; }
h1 { font-size: 2rem; } /* 32px */
```

---

## Understanding The Em Unit

**Description:**  
`em` units are relative to the font size of the current element.

**Insights:**  
- `1em` = current element’s font size.
- Stacks with nested elements (can compound).

```css
div { font-size: 20px; }
span { font-size: 2em; } /* 40px if inside div */
```

---

## Vw and Vh Units

**Description:**  
`vw` and `vh` are relative to the viewport’s width and height.

**Insights:**  
- `1vw` = 1% of viewport width.
- `1vh` = 1% of viewport height.

```css
div {
    width: 50vw;
    height: 30vh;
}
```

---

## CSS Units Quiz

**Description:**  
Test your knowledge of CSS units and when to use each.

---

## Which Units Should You Use?

**Description:**  
Choose units based on context:
- Use `rem`/`em` for scalable text.
- Use `%`, `vw`, `vh` for responsive layouts.
- Use `px` for precise, fixed sizing.

---

## Working With Floats

**Description:**  
The `float` property moves elements to the left or right, allowing text and inline elements to wrap around.

**Insights:**  
- `float: left;` or `float: right;`
- Use `clear: both;` to prevent wrapping.

```css
img {
    float: left;
    margin-right: 10px;
}
.clearfix::after {
    content: "";
    display: table;
    clear: both;
}
```

---

## Working With Background Images

**Description:**  
The `background-image` property sets an image as the background of an element.

**Insights:**  
- Use `url('image.jpg')` as the value.
- Can combine with background color.

```css
div {
    background-image: url('bg.jpg');
    background-color: #eee;
}
```

---

## Controlling Background-Repeat

**Description:**  
The `background-repeat` property controls if/how a background image repeats.

**Insights:**  
- `repeat` (default), `no-repeat`, `repeat-x`, `repeat-y`.

```css
div {
    background-repeat: no-repeat;
}
```

---

## Sizing Our Background

**Description:**  
The `background-size` property controls the size of the background image.

**Insights:**  
- `cover` — fills the element, may crop.
- `contain` — fits the image inside the element.
- Or use specific sizes (e.g., `100px 200px`).

```css
div {
    background-size: cover;
}
```

---

## Positioning Background

**Description:**  
The `background-position` property sets the starting position of a background image.

**Insights:**  
- Values: `left`, `center`, `right`, `top`, `bottom`, or coordinates (`50% 50%`).

```css
div {
    background-position: center center;
}
```

---

## Working With Background-Clip

**Description:**  
The `background-clip` property defines how far the background extends within the element.

**Insights:**  
- `border-box`, `padding-box`, `content-box`.

```css
div {
    background-clip: padding-box;
}
```

---

## Background Exercise

**Description:**  
Practice using background properties to create visually appealing sections.

---

## An Important Note About Gradients!

**Description:**  
Gradients are generated images, not actual image files. They are created with CSS functions.

---

## Creating Linear Gradients

**Description:**  
The `linear-gradient()` function creates a smooth transition between colors along a straight line.

**Insights:**  
- Syntax: `background: linear-gradient(direction, color1, color2, ...);`
- Example: `to right`, `to bottom`, or angles.

```css
div {
    background: linear-gradient(to right, red, yellow);
}
```

---

## Radial, Conic, and Repeating Gradients

**Description:**  
- `radial-gradient()` — radiates from a center point.
- `conic-gradient()` — sweeps around a center point.
- `repeating-linear-gradient()` — repeats a linear gradient pattern.

```css
div {
    background: radial-gradient(circle, red, yellow);
}
```

---

## The Background Shorthand Property

**Description:**  
The `background` shorthand sets multiple background properties in one line.

**Insights:**  
- Order: color, image, position/size, repeat, origin, clip, attachment.

```css
div {
    background: #fff url('bg.jpg') no-repeat center/cover;
}
```

---

## Fancy CSS Filters

**Description:**  
The `filter` property applies graphical effects like blur, brightness, contrast, grayscale, etc.

**Insights:**  
- Example: `filter: blur(5px) brightness(0.8);`

```css
img {
    filter: grayscale(100%) blur(2px);
}
```

---

## Introducing Positioning

**Description:**  
The `position` property controls how an element is positioned in the document.

**Insights:**  
- Values: `static` (default), `relative`, `absolute`, `fixed`, `sticky`.

---

## Relative Positioning

**Description:**  
`position: relative` moves an element relative to its normal position.

**Insights:**  
- Use `top`, `right`, `bottom`, `left` to offset.

```css
div {
    position: relative;
    top: 10px;
    left: 20px;
}
```

---

## Controlling Layers With Z-Index

**Description:**  
The `z-index` property controls the stack order of positioned elements.

**Insights:**  
- Higher `z-index` appears above lower.
- Only works on positioned elements (`relative`, `absolute`, `fixed`, `sticky`).

```css
div {
    position: absolute;
    z-index: 10;
}
```

---

## Absolute Positioning Pt 1 & 2

**Description:**  
`position: absolute` removes the element from normal flow and positions it relative to the nearest positioned ancestor.

**Insights:**  
- Use `top`, `right`, `bottom`, `left` for placement.
- If no ancestor is positioned, it uses the viewport.

```css
.child {
    position: absolute;
    top: 0;
    right: 0;
}
```

---

## Creating A Button Badge

**Description:**  
Combine absolute positioning and z-index to create notification badges on buttons.

---

## Fixed Positioning

**Description:**  
`position: fixed` positions the element relative to the viewport. It stays in place when scrolling.

```css
nav {
    position: fixed;
    top: 0;
    width: 100%;
}
```

---

## Positioning Exercises

**Description:**  
Practice using relative, absolute, and fixed positioning to create layouts and UI elements.

---

## Introducing Transitions

**Description:**  
Transitions animate changes to CSS properties smoothly over time.

**Insights:**  
- Use `transition-property`, `transition-duration`, `transition-timing-function`, `transition-delay`.

---

## The Basic Transition Syntax

**Description:**  
The `transition` shorthand property sets which properties to animate, how long, and how.

**Insights:**  
- Syntax: `transition: property duration timing-function delay;`

```css
button {
    transition: background 0.3s ease;
}
```

---

## Working With Multiple Transitions

**Description:**  
You can animate multiple properties by separating them with commas.

```css
button {
    transition: background 0.3s, color 0.2s;
}
```

---

## Transition Timing Functions

**Description:**  
Controls the speed curve of the transition.

**Insights:**  
- Common values: `ease`, `linear`, `ease-in`, `ease-out`, `cubic-bezier(...)`.

---

## Transition Delays

**Description:**  
Delays the start of a transition.

**Insights:**  
- `transition-delay: 0.5s;` — waits half a second before starting.

---

## Understanding Animation Performance

**Description:**  
Some CSS properties are more performance-friendly to animate (like `transform` and `opacity`). Avoid animating layout properties for smoother performance.

---

## Introducing Transforms

**Description:**  
The `transform` property applies 2D or 3D transformations to elements.

**Insights:**  
- `translate`, `scale`, `rotate`, `skew`, etc.

```css
div {
    transform: rotate(15deg) scale(1.2);
}
```

---

## Other Types of Transformations

**Description:**  
Explore more transform functions:  
- `scaleX`, `scaleY`, `skewX`, `skewY`, `translateX`, `translateY`, `perspective`, etc.

---

## Transform Origin

**Description:**  
The `transform-origin` property sets the point around which a transformation is applied.

**Insights:**  
- Default is `50% 50%` (center).
- Can use keywords or percentages.

```css
div {
    transform-origin: left top;
}
```

---

## Building Fancy Button Hover Effects

**Description:**  
Combine transitions, transforms, and pseudo-elements to create interactive and animated button effects.

---

## Introducing Flexbox

**Description:**  
Flexbox is a CSS layout model that makes it easy to design flexible and efficient layouts, distributing space and aligning items in a container.

**Insights:**  
- Flexbox is ideal for 1D layouts (rows or columns).
- Parent container becomes a flex container with `display: flex;`.

---

## Display: Flex and Flex Axis

**Description:**  
The `display: flex;` property turns an element into a flex container, enabling flexbox layout for its children.

**Insights:**  
- Main axis: defined by `flex-direction` (default is row, left to right).
- Cross axis: perpendicular to main axis.

```css
.container {
    display: flex;
}
```

---

## Working With Flex-Direction

**Description:**  
The `flex-direction` property sets the direction of the main axis.

**Insights:**  
- `row` (default): left to right.
- `row-reverse`: right to left.
- `column`: top to bottom.
- `column-reverse`: bottom to top.

```css
.container {
    flex-direction: column;
}
```

---

## Flexbox Exercise 1

**Description:**  
Practice changing the direction of flex items using `flex-direction`.

---

## Flex-Wrap

**Description:**  
The `flex-wrap` property controls whether flex items wrap onto multiple lines.

**Insights:**  
- `nowrap` (default): all items in one line.
- `wrap`: items wrap onto new lines.
- `wrap-reverse`: wrap in reverse order.

```css
.container {
    flex-wrap: wrap;
}
```

---

## Justify-Content

**Description:**  
The `justify-content` property aligns items along the main axis.

**Insights:**  
- `flex-start` (default), `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

```css
.container {
    justify-content: center;
}
```

---

## Flexbox Exercise 2

**Description:**  
Practice aligning items along the main axis using `justify-content`.

---

## Align-Items

**Description:**  
The `align-items` property aligns items along the cross axis.

**Insights:**  
- `stretch` (default), `flex-start`, `flex-end`, `center`, `baseline`.

```css
.container {
    align-items: flex-end;
}
```

---

## Flexbox Exercise 3

**Description:**  
Practice aligning items along the cross axis using `align-items`.

---

## Align-Content

**Description:**  
The `align-content` property aligns multiple lines of flex items along the cross axis (when wrapping).

**Insights:**  
- Only affects containers with multiple lines.
- Values: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch` (default).

```css
.container {
    flex-wrap: wrap;
    align-content: space-between;
}
```

---

## Flexbox Exercise 4

**Description:**  
Practice using `align-content` with wrapped flex items.

---

## Align-Self

**Description:**  
The `align-self` property allows a single flex item to override the container's `align-items` value.

**Insights:**  
- Values: `auto` (default), `flex-start`, `flex-end`, `center`, `baseline`, `stretch`.

```css
.item {
    align-self: center;
}
```

---

## Flexbox Exercise 5

**Description:**  
Practice overriding alignment for individual flex items using `align-self`.

---

## The Flex-Grow Property

**Description:**  
The `flex-grow` property defines how much a flex item will grow relative to the rest.

**Insights:**  
- `flex-grow: 1;` — item will grow to fill available space.
- If all items have `flex-grow: 1`, space is distributed equally.

```css
.item {
    flex-grow: 2;
}
```

---

## Controlling Shrinkage With Flex-Shrink

**Description:**  
The `flex-shrink` property defines how much a flex item will shrink relative to others when space is tight.

**Insights:**  
- `flex-shrink: 0;` — item will not shrink.
- Default is `1` (items shrink as needed).

```css
.item {
    flex-shrink: 0;
}
```

---

## Flex-Basis: Important & Confusing

**Description:**  
The `flex-basis` property sets the initial main size of a flex item before space is distributed.

**Insights:**  
- Can be set in px, %, etc.
- Overrides `width` or `height` on the main axis.

```css
.item {
    flex-basis: 200px;
}
```

---

## The Flex Shorthand Property

**Description:**  
The `flex` shorthand sets `flex-grow`, `flex-shrink`, and `flex-basis` in one line.

**Insights:**  
- Syntax: `flex: [grow] [shrink] [basis];`
- Example: `flex: 1 0 100px;`

```css
.item {
    flex: 2 1 150px;
}
```

---

## The Order Flex-Item Property

**Description:**  
The `order` property controls the order in which flex items appear in the flex container.

**Insights:**  
- Default is `0`. Lower values appear first.

```css
.item {
    order: 2;
}
```

---

## Flexbox Patterns: Building A Simple Navbar

**Description:**  
Use flexbox to create a horizontal navigation bar with evenly spaced links.

---

## Flexbox Patterns: Nested Flex Containers

**Description:**  
Nest flex containers inside each other for complex layouts (e.g., sidebar + main content).

---

## Flexbox Patterns: Centering Content

**Description:**  
Center content both vertically and horizontally using flexbox.

**Insights:**  
- Use `justify-content: center; align-items: center;` on the container.

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

---

## Flexbox Patterns: Building A Card Layout

**Description:**  
Use flexbox to create responsive card layouts with equal height and spacing.

---

