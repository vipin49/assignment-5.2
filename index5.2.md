
## 1. Objective

The objective of this assignment is to understand and practice different CSS selectors. This webpage demonstrates element selectors, class selectors, ID selectors, universal selectors, grouping selectors, and CSS cascade and specificity.

## 2. Requirements

- Visual Studio Code
- HTML
- CSS
- Google Chrome
- Chrome DevTools
- Live Server extension (optional)

## 3. Project Folder Structure

Create a folder named `Assignment-5.2` with the following files:

```text
Assignment-5.2/
│
├── index.html
├── style.css
└── Assignment-5.2.md
```

## 4. HTML Code (index.html)

Create a file named `index.html` and paste the following code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>CSS Selectors Practice</title>

    <!-- External CSS File -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>CSS Selectors Practice</h1>
        <p>Learning CSS selectors with practical examples.</p>
    </header>

    <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#courses">Courses</a>
        <a href="#contact">Contact</a>
    </nav>

    <main>

        <!-- ID Selector Example -->
        <section id="home">
            <h2>Welcome to CSS</h2>
            <p>
                CSS stands for Cascading Style Sheets. It is used to style
                HTML elements and make webpages attractive.
            </p>
        </section>

        <!-- Class Selector Example -->
        <section id="about">
            <h2>About CSS Selectors</h2>

            <div class="card">
                <h3>Element Selector</h3>
                <p>Selects HTML elements by their tag names.</p>
            </div>

            <div class="card">
                <h3>Class Selector</h3>
                <p>Selects elements using a class attribute.</p>
            </div>

            <div class="card">
                <h3>ID Selector</h3>
                <p>Selects a specific element using its unique ID.</p>
            </div>
        </section>

        <!-- Grouping Selector Example -->
        <section id="courses">
            <h2>CSS Topics</h2>
            <p class="highlight">HTML provides the structure of a webpage.</p>
            <p class="highlight">CSS controls the appearance of a webpage.</p>
            <p class="highlight">JavaScript adds interactivity to a webpage.</p>
        </section>

        <!-- Cascade and Specificity Example -->
        <section id="specificity">
            <h2>Cascade and Specificity</h2>
            <p class="special-text">
                Observe my color to understand CSS specificity.
            </p>
            <p class="cascade-text">
                Observe my color to understand the CSS cascade.
            </p>
        </section>

        <!-- Contact Section -->
        <section id="contact">
            <h2>Contact Us</h2>
            <p>Email: student@example.com</p>
            <a href="https://www.example.com">Visit Example Website</a>
        </section>

    </main>

    <footer>
        <p>&copy; 2026 CSS Selectors Practice. All rights reserved.</p>
    </footer>

</body>
</html>
```

## 5. CSS Code (style.css)

Create a file named `style.css` in the same folder and paste the following code:

```css
/* 1. Universal Selector */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* General Page Styling */
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #f0f4f8;
    color: #263238;
    line-height: 1.7;
}

/* 2. Element Selector */
h1 {
    font-size: 34px;
}

h2 {
    color: #1565c0;
    margin-bottom: 12px;
}

p {
    font-size: 16px;
    margin-bottom: 12px;
}

/* Header Styling */
header {
    background-color: #1565c0;
    color: white;
    text-align: center;
    padding: 30px 20px;
}

header p {
    margin-top: 8px;
    margin-bottom: 0;
}

/* Navigation Styling */
nav {
    background-color: #0d47a1;
    text-align: center;
    padding: 14px;
}

nav a {
    display: inline-block;
    color: white;
    text-decoration: none;
    padding: 8px 15px;
    margin: 3px;
    border-radius: 5px;
}

nav a:hover {
    background-color: #1976d2;
}

/* Main Content */
main {
    max-width: 1000px;
    margin: 25px auto;
    padding: 0 20px;
}

/* 3. ID Selector */
#home {
    background-color: #e3f2fd;
    border-left: 5px solid #1565c0;
}

/* Common Section Styling */
section {
    background-color: white;
    padding: 25px;
    margin-bottom: 22px;
    border-radius: 10px;
    box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
}

/* 4. Class Selector */
.card {
    background-color: #f8fbff;
    border: 1px solid #bbdefb;
    padding: 18px;
    margin: 12px 0;
    border-radius: 8px;
}

.card h3 {
    color: #0d47a1;
    margin-bottom: 8px;
}

.card p {
    margin-bottom: 0;
}

/* Highlight Class */
.highlight {
    background-color: #e8f5e9;
    padding: 10px;
    border-left: 4px solid #2e7d32;
    border-radius: 4px;
}

/* 5. Grouping Selector */
h3,
.highlight,
#contact a {
    font-family: Arial, Helvetica, sans-serif;
}

/* 6. Cascade and Specificity Example */

/* Element selector: specificity 0-0-1 */
p {
    color: #333333;
}

/* Class selector: specificity 0-1-0 */
.special-text {
    color: green;
}

/* ID selector: specificity 1-0-0 */
#specificity .special-text {
    color: purple;
}

/* Two conflicting rules with equal specificity */
.cascade-text {
    color: red;
}

.cascade-text {
    color: blue;
}

/* Link Styling */
#contact a {
    color: #1565c0;
    font-weight: bold;
    text-decoration: none;
}

#contact a:hover {
    text-decoration: underline;
}

/* Footer Styling */
footer {
    background-color: #263238;
    color: white;
    text-align: center;
    padding: 20px;
}

footer p {
    margin-bottom: 0;
    color: white;
}

/* Responsive Styling */
@media (max-width: 600px) {
    h1 {
        font-size: 26px;
    }

    main {
        padding: 0 12px;
    }

    section {
        padding: 18px;
    }

    nav a {
        padding: 7px 9px;
    }
}
```

## 6. Explanation of CSS Selectors

### A. Universal Selector (`*`)

The universal selector selects all HTML elements.

Example:

```css
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}
```

**Purpose:** It applies common box-sizing and spacing rules to all elements.

### B. Element Selector

An element selector selects HTML elements by their tag names.

Example:

```css
h2 {
    color: #1565c0;
}

p {
    font-size: 16px;
}
```

**Purpose:** It styles all `h2` headings and all paragraphs.

### C. Class Selector (`.`)

A class selector selects elements that have a particular class name.

Example:

```css
.card {
    background-color: #f8fbff;
    padding: 18px;
    border-radius: 8px;
}
```

**Purpose:** It applies the same design to multiple cards using the `class="card"` attribute.

### D. ID Selector (`#`)

An ID selector selects an element using its unique ID.

Example:

```css
#home {
    background-color: #e3f2fd;
}
```

**Purpose:** It gives the Home section a different background color. An ID should be unique within the HTML document.

### E. Grouping Selector (`,`)

A grouping selector applies the same CSS declarations to multiple selectors.

Example:

```css
h3,
.highlight,
#contact a {
    font-family: Arial, Helvetica, sans-serif;
}
```

**Purpose:** It applies the same font family to all three selected groups without repeating the declaration.

## 7. CSS Cascade and Specificity

CSS specificity determines which selector wins when multiple applicable rules set the same property. When specificity is equal and the declarations have the same importance and origin, the later rule wins.

### Example 1: Specificity

```css
p {
    color: #333333;
}

.special-text {
    color: green;
}

#specificity .special-text {
    color: purple;
}
```

The paragraph with `class="special-text"` inside the section with `id="specificity"` will appear **purple** because the ID-and-class selector has greater specificity than the class selector and element selector.

Specificity comparison:

| Selector | Specificity |
|---|---|
| `p` | 0-0-1 |
| `.special-text` | 0-1-0 |
| `#specificity .special-text` | 1-1-0 |

### Example 2: Cascade

```css
.cascade-text {
    color: red;
}

.cascade-text {
    color: blue;
}
```

Both selectors have equal specificity. Therefore, the second rule wins, and the paragraph appears **blue**.

This demonstrates the CSS cascade rule that later declarations win when the relevant priority and specificity are equal.

## 8. Steps to Run the Website

1. Open Visual Studio Code.
2. Create the `Assignment-5.2` folder.
3. Create `index.html` and paste the HTML code.
4. Create `style.css` and paste the CSS code.
5. Save both files using `Ctrl + S`.
6. Ensure that both files are in the same folder.
7. Open `index.html` with Live Server or directly in Google Chrome.
8. Observe the different styles applied to the webpage.

## 9. Testing Using Chrome DevTools

1. Open the webpage in Google Chrome.
2. Right-click the purple paragraph and select **Inspect**.
3. In the Styles panel, find the `#specificity .special-text` rule.
4. Inspect the two `.cascade-text` rules and observe that the blue declaration wins.
5. Temporarily disable a CSS declaration by unchecking its checkbox.
6. Observe how the webpage changes when a declaration is disabled.
7. Check the Console panel if the CSS file does not load.

**Note:** Changes made in DevTools are temporary. Update `style.css` to save permanent changes.

## 10. Expected Output

The webpage should display:

- A blue header with a white heading.
- A dark-blue navigation bar.
- A light-blue Home section styled using an ID selector.
- Three cards styled using the same class selector.
- Headings and paragraphs styled using element selectors.
- Multiple selectors sharing declarations through a grouping selector.
- A purple paragraph demonstrating specificity.
- A blue paragraph demonstrating the cascade rule.
- A dark footer and responsive layout.

## 11. Result

The webpage was successfully created using different CSS selectors. The universal, element, class, ID, and grouping selectors were implemented. Conflicting CSS rules were tested to understand specificity and the cascade. Chrome DevTools was used to inspect and verify the applied styles.

## 12. Submission

Submit the following files:

1. `index.html` — HTML webpage containing multiple elements and sections.
2. `style.css` — CSS file demonstrating all required selectors.
3. `Assignment-5.2.md` — Documentation explaining the selectors and their results.

