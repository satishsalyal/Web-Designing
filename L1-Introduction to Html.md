# 🌐 Unit I — HTML Fundamentals

> **Course:** Web Designing (LIGMDIT 2000) &nbsp;|&nbsp; **Program:** B.Sc. Data Science & AI, Semester 2

---

## 📋 Topics Covered

- [1. What is HTML?](#1-what-is-html)
- [2. HTML Documents](#2-html-documents)
- [3. Basic Structure of an HTML Document](#3-basic-structure-of-an-html-document)
- [4. Creating an HTML Document](#4-creating-an-html-document)
- [5. Key Concepts Summary](#5-key-concepts-summary)
- [6. Common Mistakes to Avoid](#6-common-mistakes-to-avoid)
- [7. Review Questions](#7-review-questions)

---

## 1. What is HTML?

### 1.1 Definition

**HTML** stands for **HyperText Markup Language**. It is the standard language used to create and design web pages and web applications. HTML describes the **structure** and **content** of a web page using a system of elements represented by **tags**.

| Term | Meaning |
|------|---------|
| **HyperText** | The ability to link one document to another through hyperlinks |
| **Markup** | Using special symbols (tags) to annotate text and define its meaning or role |

---

### 1.2 Brief History of HTML

| Version | Year & Key Features |
|---------|---------------------|
| **HTML 1.0** | 1991 — First version by Tim Berners-Lee. Very basic with only text and links. |
| **HTML 2.0** | 1995 — Added forms, tables. Became the first formal standard. |
| **HTML 3.2** | 1997 — Introduced scripting support, improved tables. |
| **HTML 4.01** | 1999 — Added stylesheets (CSS), frames, better accessibility. |
| **XHTML 1.0** | 2000 — Stricter, XML-based version of HTML 4. |
| **HTML5** | 2014 — Current standard. Adds audio, video, canvas, semantic elements. |

---

### 1.3 Key Characteristics of HTML

- 🚫 **Not a Programming Language:** HTML does not have logic, conditions, or loops. It simply defines structure.
- 💻 **Platform Independent:** HTML files can be opened in any web browser on any operating system.
- 🌐 **Interpreted by Browsers:** Web browsers (Chrome, Firefox, Edge) read and render HTML files.
- 🔡 **Case Insensitive:** HTML tags can be written in uppercase or lowercase, though lowercase is preferred.
- 🆓 **Free and Open:** No license is required to write or use HTML.

> 📝 **Note:** HTML alone defines the structure of a page. **CSS** is used for styling, and **JavaScript** is used for behavior/logic.

---

### 1.4 Role of HTML in Web Development

HTML is considered the **backbone** of all web pages. Every webpage you visit — from Google to YouTube — is built using HTML at its core. When a browser receives an HTML file from a web server, it reads the file and displays it as a formatted webpage.

---

## 2. HTML Documents

### 2.1 What is an HTML Document?

An HTML document is a plain text file that contains HTML code. It is saved with the extension **`.html`** or **`.htm`**. When this file is opened in a web browser, the browser reads the HTML tags and renders the content as a visual web page.

---

### 2.2 How HTML Documents Work

The process of displaying an HTML page involves three main steps:

```
1. User types a URL  →  2. Browser requests HTML from server  →  3. Browser renders the page
```

1. The user types a URL (web address) in the browser.
2. The browser sends a request to the web server and receives an HTML document.
3. The browser **parses** (reads) the HTML tags and renders the page visually.

---

### 2.3 HTML Tags — The Building Blocks

HTML uses **tags** to mark up content. A tag is a keyword enclosed in angle brackets. Most tags come in **pairs**: an opening tag and a closing tag.

```html
<tagname> Content goes here </tagname>
    ↑                              ↑
Opening tag              Closing tag (has a forward slash)
```

**Examples:**

```html
<p>This is a paragraph.</p>
<h1>This is a Heading</h1>
<b>This text is bold</b>
```

---

### 2.4 HTML Elements

An **HTML element** refers to everything from the opening tag to the closing tag, including the content in between.

```html
<h1>Welcome to Web Design</h1>
 ↑                          ↑
Opening tag            Closing tag
└──────────── Element ───────────┘
```

---

### 2.5 HTML Attributes

Attributes provide **additional information** about HTML elements. They are always written inside the **opening tag** as name-value pairs.

```html
<a href="https://www.example.com">Click Here</a>
    ↑              ↑
Attribute      Attribute
 name           value
```

**Common Attributes:**

| Attribute | Purpose |
|-----------|---------|
| `href` | Link URL |
| `src` | Image source |
| `alt` | Alternate text for images |
| `id` | Unique identifier |
| `class` | CSS class name |

---

## 3. Basic Structure of an HTML Document

### 3.1 Overview

Every valid HTML document follows a specific **standard structure**. This ensures the browser can correctly interpret and display the content.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title</title>
  </head>
  <body>
    <h1>Welcome to My First Web Page</h1>
    <p>This is a paragraph of text.</p>
  </body>
</html>
```

---

### 3.2 Detailed Explanation of Each Part

#### 3.2.1 `<!DOCTYPE html>`

The **DOCTYPE declaration** is the very first line of an HTML document. It is **not an HTML tag** — it is an instruction to the browser about which version of HTML the page uses.

- In HTML5, the DOCTYPE is simply: `<!DOCTYPE html>`
- It must appear **before** the `<html>` tag.
- It tells the browser to render the page in **standards mode**, preventing display issues.

> 📝 **Note:** Without DOCTYPE, some browsers enter **'Quirks Mode'** and may display the page incorrectly.

---

#### 3.2.2 `<html> ... </html>` — Root Element

The `<html>` tag is the **root element** of an HTML page. All other elements must be placed inside this tag.

```html
<html lang="en">
  ... all page content ...
</html>
```

- **`lang` attribute:** Specifies the language of the document (e.g., `"en"` for English). Helps search engines and assistive technologies.
- Everything — head, body, and all content — sits inside `<html>`.

---

#### 3.2.3 `<head> ... </head>` — Document Head

The `<head>` section contains **meta-information** about the document. This information is **not displayed** on the web page but is used by the browser and search engines.

**Common elements inside `<head>`:**

| Tag | Purpose |
|-----|---------|
| `<title>` | Sets the title shown in the browser tab and bookmarks |
| `<meta charset>` | Defines character encoding (UTF-8 supports all languages) |
| `<meta name="viewport">` | Controls layout on mobile/responsive screens |
| `<meta name="description">` | Provides a description for search engines (SEO) |
| `<link>` | Links external resources, such as CSS stylesheets |
| `<style>` | Embeds internal CSS styles |
| `<script>` | Embeds or links JavaScript code |

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="My first webpage">
  <title>My Web Page</title>
  <link rel="stylesheet" href="style.css">
</head>
```

---

#### 3.2.4 `<body> ... </body>` — Document Body

The `<body>` element contains **all the visible content** of the web page — everything the user sees in the browser window.

```html
<body>
  <h1>This is the Main Heading</h1>
  <p>This is a paragraph. It is visible on the page.</p>
  <img src="photo.jpg" alt="A photo">
  <a href="about.html">Go to About Page</a>
</body>
```

**Key points about `<body>`:**
- There is only **one** `<body>` element per HTML document.
- All headings, paragraphs, lists, images, links, and forms are placed here.
- Content flows **top to bottom** as it appears in the code.

---

### 3.3 Complete Structure Diagram

```
HTML Document
│
├── <!DOCTYPE html>          ← Declaration: tells browser to use HTML5
│
└── <html>                   ← Root element — wraps entire document
    │
    ├── <head>               ← Invisible metadata section
    │   ├── <meta charset>   ← Character encoding declaration
    │   ├── <title>          ← Tab/window title (not shown on page)
    │   └── <link> / <style> ← CSS connection
    │
    └── <body>               ← Visible content begins here
        ├── Headings, Paragraphs   ← Text content visible to user
        ├── Images, Links, Tables  ← Media and navigation
        └── Forms, etc.            ← Interactive elements
```

---

## 4. Creating an HTML Document

### 4.1 Tools Required

Creating an HTML file does not require any special software. You need:

- **Text Editor:** Notepad (Windows), TextEdit (Mac), VS Code, Sublime Text, or Notepad++
- **Web Browser:** Google Chrome, Firefox, Microsoft Edge, or any modern browser

---

### 4.2 Step-by-Step Process

```
Step 1 → Open a text editor (e.g., Notepad)
Step 2 → Type the basic HTML structure
Step 3 → Save the file with .html extension (e.g., index.html)
Step 4 → Open the saved file in a web browser to view the output
```

---

### 4.3 First HTML Page — Complete Example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>My First Web Page</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <h2>About Me</h2>
    <p>My name is Ravi. I am a student of B.Sc. Data Science & AI.</p>
    <p>I am learning <b>HTML</b> in Semester 2.</p>
    <a href="https://www.google.com">Visit Google</a>
  </body>
</html>
```

---

### 4.4 Browser Output Explanation

| HTML Code | What Appears in Browser |
|-----------|------------------------|
| `<h1>Hello, World!</h1>` | Large bold heading: *'Hello, World!'* |
| `<h2>About Me</h2>` | Slightly smaller bold heading: *'About Me'* |
| `<p>My name is Ravi...</p>` | Normal paragraph text |
| `<b>HTML</b>` | The word *'HTML'* appears in **bold** |
| `<a href="...">Visit Google</a>` | Clickable blue underlined hyperlink |

---

## 5. Key Concepts Summary

| Concept | Explanation |
|---------|-------------|
| **HTML** | HyperText Markup Language — standard language for web pages |
| **Tag** | Keyword enclosed in `< >` brackets used to mark up content |
| **Element** | Complete unit: opening tag + content + closing tag |
| **Attribute** | Extra information inside opening tag as `name="value"` pairs |
| **`<!DOCTYPE>`** | Declaration at top of file telling browser the HTML version |
| **`<html>`** | Root element that wraps all content of the document |
| **`<head>`** | Section for invisible metadata (title, charset, CSS links) |
| **`<body>`** | Section for all visible page content |
| **`<title>`** | Sets the text shown in the browser's tab bar |
| **charset UTF-8** | Character encoding that supports all languages globally |

---

## 6. Common Mistakes to Avoid

| ❌ Mistake | ✅ Correct Practice |
|-----------|-------------------|
| Forgetting to close tags | Every `<tag>` must have a `</tag>` (except void elements like `<br>`, `<img>`) |
| Missing DOCTYPE | Always include `<!DOCTYPE html>` at the very top |
| Wrong file extension | Save files as `.html` or `.htm`, not `.txt` |
| Nesting errors | Close inner tags before outer ones |
| Missing quotes in attributes | Always use quotes: `href="url"` not `href=url` |

**Nesting Example:**

```html
❌ WRONG:   <b><i>Text</b></i>   (improper nesting)
✅ CORRECT: <b><i>Text</i></b>   (close inner tag first)

❌ WRONG:   <a href=google.com>   (missing quotes)
✅ CORRECT: <a href="google.com"> (with quotes)
```

---

## 📌 Exam Tips

> Keep these in mind before your exam!

1. Know the full form: **HyperText Markup Language**
2. Memorize the four main structural tags: `<!DOCTYPE>`, `<html>`, `<head>`, `<body>`
3. Be ready to **write a simple HTML page from scratch**
4. Understand the difference between `<head>` *(metadata)* and `<body>` *(visible content)*
5. Practice distinguishing between **Tags**, **Elements**, and **Attributes**

---

## 7. Review Questions

1. What is HTML? Explain its full form and purpose.
2. What is the difference between an HTML **Tag**, **Element**, and **Attribute**?
3. Describe the basic structure of an HTML document with an example.
4. What is the purpose of the `<!DOCTYPE html>` declaration?
5. What information is placed inside the `<head>` section? Why is it not visible on the page?
6. Write a simple HTML page that displays your name, college name, and a link to your college website.

---

<div align="center">

*Unit I Notes — Web Designing (LIGMDIT 2000)*  
*B.Sc. Data Science & AI · Semester 2*

</div>
