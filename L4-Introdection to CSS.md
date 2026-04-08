# 📘 CSS Tables Styling 

---

## 1. 🧩 Introduction to CSS Tables

### 1.1 What are Tables in HTML?

HTML tables (`<table>`) are used to display data in a **tabular format** using:

* `<table>` → Table container
* `<tr>` → Table row
* `<th>` → Table header
* `<td>` → Table data

### 1.2 Why Style Tables with CSS?

Default HTML tables are visually plain. CSS allows:

* 🎯 Enhanced readability
* 📐 Better alignment and spacing
* 🎨 Professional UI design
* 📱 Responsive layouts

---

## 2. 🏗️ Basic Table Structure

### Example HTML Table

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Department</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>25</td>
    <td>IT</td>
  </tr>
</table>
```

---

## 3. ⚙️ CSS Table Properties Overview

CSS provides several properties to control:

* Borders
* Spacing
* Colors
* Alignment
* Layout behavior

---

# 4. 🎨 Styling Tables in CSS

---

## 4.1 🧱 Adjusting Borders

### Properties:

* `border`
* `border-collapse`
* `border-spacing`

### Example:

```css
table, th, td {
  border: 1px solid black;
}

table {
  border-collapse: collapse;
}
```

### Explanation:

* `border-collapse: collapse;` → Merges adjacent borders into a single border
* Without it, borders appear doubled

---

## 4.2 📏 Controlling Spacing

### Properties:

* `padding`
* `border-spacing`

### Example:

```css
th, td {
  padding: 10px;
}

table {
  border-spacing: 5px;
}
```

### Explanation:

* `padding` → Space inside cells
* `border-spacing` → Space between table cells

---

## 4.3 🎨 Applying Colors

### Properties:

* `background-color`
* `color`

### Example:

```css
table {
  background-color: #f2f2f2;
}

th {
  background-color: #4CAF50;
  color: white;
}

tr:nth-child(even) {
  background-color: #dddddd;
}
```

### Explanation:

* `nth-child()` enables **zebra striping**
* Improves readability in large datasets

---

## 4.4 🧭 Text Alignment

### Properties:

* `text-align`
* `vertical-align`

### Example:

```css
th {
  text-align: center;
}

td {
  text-align: left;
  vertical-align: middle;
}
```

### Alignment Options:

* Horizontal: left, right, center, justify
* Vertical: top, middle, bottom

---

## 4.5 📐 Table Width and Layout

### Properties:

* `width`
* `table-layout`

### Example:

```css
table {
  width: 100%;
  table-layout: fixed;
}
```

### Explanation:

* `fixed` → Equal column width
* `auto` → Based on content

---

## 4.6 🧩 Styling Table Borders Individually

```css
th {
  border-bottom: 2px solid black;
}

td {
  border-top: 1px dashed gray;
}
```

---

## 5. 🚀 Advanced Table Styling

---

### 5.1 ✨ Hover Effects

```css
tr:hover {
  background-color: #f5f5f5;
}
```

👉 Enhances interactivity

---

### 5.2 🎯 Striped Tables

```css
tr:nth-child(odd) {
  background-color: #ffffff;
}
```

---

### 5.3 📱 Responsive Tables

```css
table {
  display: block;
  overflow-x: auto;
}
```

---

### 5.4 🏷️ Caption Styling

```css
caption {
  caption-side: top;
  font-weight: bold;
  font-size: 18px;
}
```

---

## 6. 🧪 Complete Practical Example

### HTML:

```html
<table>
  <caption>Student Details</caption>
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Department</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>25</td>
    <td>IT</td>
  </tr>
  <tr>
    <td>Sara</td>
    <td>23</td>
    <td>CSE</td>
  </tr>
</table>
```

### CSS:

```css
table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  border: 1px solid #ddd;
  padding: 10px;
}

th {
  background-color: #4CAF50;
  color: white;
  text-align: center;
}

tr:nth-child(even) {
  background-color: #f2f2f2;
}

tr:hover {
  background-color: #ddd;
}
```

---


## 7. 📚 Exercise Questions

1. Explain the difference between `border-collapse` and `border-spacing`.
2. Design a zebra-striped table with hover effects.
3. Create a responsive table layout.
4. Demonstrate horizontal and vertical alignment in tables.
5. Compare `table-layout: fixed` and `auto`.

---

