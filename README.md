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

## Getting Our Starter Code

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

Inline styles are added directly to HTML elements using the `style` attribute.

```html
<p style="color: blue; font-size: 18px;">This text is blue and larger.</p>
```

**Note:** Inline styles override other styles but are not recommended for large projects.

---

## Writing Internal Styles

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

[CodePen](https://codepen.io/) is an online code editor for HTML, CSS, and JS. Great for quick experiments and sharing code.

---

## Anatomy of CSS

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

Selects all elements of a given type.

```css
h2 {
    color: purple;
}
```

---

## CSS Basics Exercise

Try changing the color and font size of all `<p>` elements.

```css
p {
    color: navy;
    font-size: 18px;
}
```

---

## Working with background-color

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

CSS supports 140+ named colors.

```css
p {
    color: tomato;
    background-color: lightyellow;
}
```

---

## Understanding RGB Colors

RGB stands for Red, Green, Blue. Each value ranges from 0 to 255.

```css
div {
    background-color: rgb(255, 0, 0); /* Red */
    color: rgb(0, 0, 0); /* Black */
}
```

---

## Hexadecimal Colors

Hex codes start with `#` and use 6 digits.

```css
body {
    background-color: #ffffff; /* White */
    color: #333333; /* Dark gray */
}
```

---

## RGBA Colors and Opacity

RGBA adds an alpha (opacity) value (0 = transparent, 1 = opaque).

```css
div {
    background-color: rgba(0, 128, 0, 0.5); /* Semi-transparent green */
}
```

---

## Colors Quiz

Try to guess the color output for:

```css
p {
    color: #ff6347;
    background: rgb(240, 248, 255);
}
```

---

## CSS Inheritance

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

Change the background and text color of a div.

```css
div {
    background: #222;
    color: #fff;
}
```

---

## Changing Fonts with Font-Family

Set the font for elements.

```css
body {
    font-family: Arial, Helvetica, sans-serif;
}
```

---

## Font-size, font-weight, and font-style

```css
h1 {
    font-size: 2em;
    font-weight: bold;
    font-style: italic;
}
```

---

## Changing Text Alignment

```css
p {
    text-align: center;
}
```

---

## Line-height, letter-spacing, and word-spacing

```css
p {
    line-height: 1.5;
    letter-spacing: 2px;
    word-spacing: 8px;
}
```

---

## Adding Custom Fonts With Google Fonts

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

```css
h1 {
    text-shadow: 2px 2px 5px gray;
}
```

---

## Our First Mini Project: Cantilever

Build a simple landing page using headings, paragraphs, and CSS for layout and color.

---

## Text-transform & text-decoration

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

Selects a single element by its unique ID.

```css
#main-title {
    color: orange;
}
```

---

## The Class Selector

Selects all elements with a given class.

```css
.highlight {
    background: yellow;
}
```

---

## Styling Lists

```css
ul {
    list-style-type: square;
    padding-left: 20px;
}
```

---

## Styling Links and :hover Pseudo-Class

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

Set multiple font properties at once.

```css
p {
    font: italic bold 16px/1.5 Arial, sans-serif;
}
```

---

## Leafy Seadragon Exercise

Style an image and caption using CSS.

---

## The Universal Selector

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

Select elements by attribute.

```css
input[type="text"] {
    border: 2px solid green;
}
```

---

## Grouping Selectors

Apply the same styles to multiple selectors.

```css
h1, h2, h3 {
    color: teal;
}
```

---

## Descendant & Child Combinators

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

Combine selectors for more specific targeting.

```css
ul.menu li.active {
    color: red;
}
```

---

## CSS Selectors Exercise

Practice writing selectors for different elements and classes.

---

## Introducing The Box Model

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

```css
p {
    border: 1px solid #ccc;
    border-radius: 8px;
}
```

---

## Width, Height, and Percentages

```css
img {
    width: 50%;
    height: auto;
}
```

---

## Adding Padding to Elements

```css
button {
    padding: 10px 20px;
}
```

---

## Working With Margins

```css
h2 {
    margin-top: 30px;
    margin-bottom: 10px;
}
```

---

## The Alternate Box Model

Use `box-sizing: border-box` to include padding and border in width/height.

```css
* {
    box-sizing: border-box;
}
```

---

## The Display Property

Control how elements are displayed.

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

Hide elements from the page.

```css
.hidden {
    display: none;
}
```

---

## Negative Margin & Margin Auto

```css
div {
    margin-left: -20px;
    margin-right: auto;
}
```

---

## Margin Collapsing: WTF?

Adjacent vertical margins may combine into one. Test with stacked elements.

---

## A Common Layout Pattern

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

```css
img {
    min-width: 100px;
    max-width: 400px;
}
```

---

## Rounding Elements With Border Radius

```css
img {
    border-radius: 50%;
}
```

---

## Box Shadows

```css
.box {
    box-shadow: 2px 2px 8px rgba(0,0,0,0.2);
}
```

---

## Working With Overflow

```css
div {
    width: 200px;
    height: 100px;
    overflow: auto;
}
```

---

## Ski Resort Exercise

Build a styled card or section for a ski resort using all the above CSS concepts.

---

