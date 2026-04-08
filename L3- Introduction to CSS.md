# 📘 Cascading Style Sheets (CSS)
---

## 1. Concept of CSS

### 1.1 What is CSS?

**Cascading Style Sheets (CSS)** is a stylesheet language used to describe the presentation and layout of HTML documents. It controls how elements are displayed on screen, paper, or other media.

### 1.2 Why CSS?

* 🎯 Separates **content (HTML)** from **presentation (CSS)**
* 🛠 Improves **maintainability and scalability**
* 📱 Enables **responsive design**
* 🔁 Reduces code repetition
* ✨ Enhances user experience

### 1.3 CSS Syntax

```css
selector {
    property: value;
}
```

**Example:**

```css
p {
    color: blue;
    font-size: 16px;
}
```

### 1.4 Types of CSS
Styles can be added to HTML in three primary ways: 
- External CSS: Create a separate file with a .css extension (e.g., style.css) and link it in the HTML <head> using the <link> tag. This is recommended for managing entire websites.
- Internal CSS: Define styles directly within the HTML document inside a <style> tag located in the <head> section.
- Inline CSS: Apply styles directly to a specific HTML element using the style attribute.

#### 🔹 Inline CSS

```html
<p style="color:red;">Hello</p>
```

#### 🔹 Internal CSS

```html
<style>
    p { color: green; }
</style>
```

#### 🔹 External CSS (Recommended)

```html
<link rel="stylesheet" href="style.css">
```

---

## 2. Creating Style Sheets

### 2.1 External Stylesheet Creation

1. Create a file: `style.css`
2. Write CSS rules:

```css
body {
    background-color: lightgray;
}
```

3. Link it in HTML:

```html
<link rel="stylesheet" href="style.css">
```

---

### 2.2 CSS Selectors

Selectors define which elements to style.

#### 📌 Types of Selectors

| Selector Type | Example   | Description       |
| ------------- | --------- | ----------------- |
| Element       | `p`       | Targets all `<p>` |
| Class         | `.box`    | Targets class     |
| ID            | `#header` | Unique element    |
| Grouping      | `h1, p`   | Multiple elements |
| Universal     | `*`       | All elements      |

**Example:**

```css
.box {
    border: 1px solid black;
}
```

---

### 2.3 CSS Cascade and Specificity

* 🧠 Inline > ID > Class > Element
* ⏱ Later rules override earlier ones

---

## 3. CSS Properties

CSS properties define how elements should be styled.

### 3.1 Categories of Properties
CSS properties are categorized into several groups to control the layout and styling of web elements. The primary categories for text, fonts, and backgrounds include:

* Text properties
* Font properties
* Background properties
* Layout properties
* Box model properties

---
---

## 1. ✍️ Text Properties

Text properties are used to format the appearance and layout of text content within an element.

### 🔑 Key Properties

* `color` → Sets the color of the text.
* `text-align` → Aligns text horizontally (e.g., left, right, center, justify).
* `text-decoration` → Adds visual effects like underline, overline, or line-through.
* `text-transform` → Controls capitalization (e.g., uppercase, lowercase, capitalize).
* `text-indent` → Specifies the indentation of the first line of text.
* `letter-spacing` / `word-spacing` → Adjusts the space between characters or words.
* `line-height` → Sets the vertical distance between lines of text.
* `text-shadow` → Adds a shadow effect to text.

---

## 2. 🔤 Font Properties

Font properties define the specific typeface characteristics, such as family, size, and weight.

### 🔑 Key Properties

* `font-family` → Specifies the prioritized list of font families (e.g., "Arial", sans-serif).
* `font-size` → Sets the size of the font (e.g., 16px, 1.2em).
* `font-style` → Defines if the text is normal, italic, or oblique.
* `font-weight` → Sets the thickness of characters (e.g., normal, bold, or numeric values like 700).
* `font-variant` → Converts text to small-caps.
* `font` → A shorthand property for setting style, variant, weight, size, line-height, and family in one declaration.

---

## 3. 🌄 Background Properties

Background properties control the background effects of an element, including colors and images.

### 🔑 Key Properties

* `background-color` → Sets a solid background color.
* `background-image` → Specifies one or more background images.
* `background-repeat` → Determines if/how a background image is repeated (e.g., repeat-x, no-repeat).
* `background-position` → Sets the starting position of a background image.
* `background-size` → Specifies the size of the background image (e.g., cover, contain).
* `background-attachment` → Sets whether a background image scrolls with the rest of the page or is fixed.
* `background` → A shorthand property to set all background values at once.

---

## ✨ Quick Summary

| Category      | Purpose                                   |
| ------------- | ----------------------------------------- |
| ✍️ Text       | Controls layout and formatting of text    |
| 🔤 Fonts      | Defines typography and appearance         |
| 🌄 Background | Manages colors and images behind elements |

---

## 4. CSS Styling

---

## 4.1 🎨 Background Styling

### Properties:

* `background-color`
* `background-image`
* `background-repeat`
* `background-position`
* `background-size`

**Example:**

```css
body {
    background-color: #f0f0f0;
    background-image: url('bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
}
```

### Shorthand Property:

```css
body {
    background: #fff url('bg.jpg') no-repeat center;
}
```

---

## 4.2 ✍️ Text Formatting

### Key Properties:

* `color`
* `text-align`
* `text-decoration`
* `text-transform`
* `line-height`
* `letter-spacing`

**Example:**

```css
h1 {
    color: navy;
    text-align: center;
    text-transform: uppercase;
}
```

```css
p {
    line-height: 1.5;
    letter-spacing: 1px;
}
```

---

## 4.3 🔤 Controlling Fonts

### Font Properties:

* `font-family`
* `font-size`
* `font-style`
* `font-weight`

**Example:**

```css
body {
    font-family: Arial, sans-serif;
    font-size: 16px;
}
```

```css
h2 {
    font-weight: bold;
    font-style: italic;
}
```

### Web-Safe Fonts:

* Arial
* Times New Roman
* Verdana

### 🌐 Google Fonts (External Fonts):

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto" rel="stylesheet">
```

```css
body {
    font-family: 'Roboto', sans-serif;
}
```

---

## 5. 🧪 Practical Example

### HTML:

```html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="style.css">
</head>
<body>

<h1>Welcome to CSS</h1>
<p class="text">This is a styled paragraph.</p>

</body>
</html>
```

### CSS (style.css):

```css
body {
    background-color: lightblue;
    font-family: Arial;
}

h1 {
    color: darkblue;
    text-align: center;
}

.text {
    color: black;
    font-size: 18px;
}


## 8. 📚 Exercise Questions

1. Explain CSS specificity with examples.
2. Differentiate between class and ID selectors.
3. Write CSS to style a webpage with background image and custom font.
4. Demonstrate text formatting properties.
5. Create a responsive webpage using media queries.

---

