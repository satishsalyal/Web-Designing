# 🌐 HTML — Detailed Notes for UG Students

> **Topics:** Working with Text · Lists · Tables · Frames · Hyperlinks · Images · Multimedia · Forms & Controls

---

## 📋 Table of Contents

- [1. Working with Text](#1-working-with-text)
- [2. Working with Lists](#2-working-with-lists)
- [3. Working with Tables](#3-working-with-tables)
- [4. Working with Frames](#4-working-with-frames)
- [5. Working with Hyperlinks](#5-working-with-hyperlinks)
- [6. Working with Images](#6-working-with-images)
- [7. Working with Multimedia](#7-working-with-multimedia)
- [8. Working with Forms and Controls](#8-working-with-forms-and-controls)
- [9. Key Concepts Summary](#9-key-concepts-summary)
- [10. Review Questions](#10-review-questions)

---

## 1. Working with Text

### 1.1 Introduction

HTML provides a rich set of tags to format and display text on a webpage. Text formatting helps improve readability, emphasize important content, and structure information meaningfully.

---

### 1.2 Heading Tags (`<h1>` to `<h6>`)

HTML offers **six levels of headings**. `<h1>` is the largest (most important) and `<h6>` is the smallest (least important).

```html
<h1>This is Heading 1 (Largest)</h1>
<h2>This is Heading 2</h2>
<h3>This is Heading 3</h3>
<h4>This is Heading 4</h4>
<h5>This is Heading 5</h5>
<h6>This is Heading 6 (Smallest)</h6>
```

> 📝 **Note:** Use only **one `<h1>`** per page — it represents the main title. Search engines use headings for indexing.

---

### 1.3 Paragraph Tag (`<p>`)

The `<p>` tag defines a **block of text** as a paragraph. Browsers automatically add space before and after paragraphs.

```html
<p>This is the first paragraph of text.</p>
<p>This is the second paragraph. It starts on a new line.</p>
```

---

### 1.4 Text Formatting Tags

| Tag | Purpose | Example Output |
|-----|---------|----------------|
| `<b>` | Bold text (visual only) | **bold** |
| `<strong>` | Important/bold text (semantic) | **important** |
| `<i>` | Italic text (visual only) | *italic* |
| `<em>` | Emphasized/italic text (semantic) | *emphasized* |
| `<u>` | Underlined text | <u>underline</u> |
| `<s>` | Strikethrough text | ~~strikethrough~~ |
| `<mark>` | Highlighted text | `highlighted` |
| `<sup>` | Superscript | x² |
| `<sub>` | Subscript | H₂O |
| `<small>` | Smaller text | fine print |
| `<big>` | Larger text | larger |
| `<tt>` | Monospace/typewriter text | `code-like` |

```html
<p>HTML stands for <strong>HyperText Markup Language</strong>.</p>
<p>Water is written as H<sub>2</sub>O in chemistry.</p>
<p>Area = πr<sup>2</sup></p>
<p>This text is <mark>highlighted</mark> for attention.</p>
<p><s>Old price: ₹500</s> &nbsp; New price: ₹350</p>
```

---

### 1.5 Line Break and Horizontal Rule

- **`<br>`** — Inserts a single line break (void element, no closing tag needed).
- **`<hr>`** — Inserts a horizontal line/divider across the page.

```html
<p>Line one<br>Line two<br>Line three</p>
<hr>
<p>This content appears below the horizontal rule.</p>
```

---

### 1.6 Preformatted Text (`<pre>`)

The `<pre>` tag displays text **exactly as written** in the HTML — preserving spaces, tabs, and line breaks. Uses a monospace font.

```html
<pre>
  Name   : Ravi Kumar
  Roll   : 101
  Branch : Data Science
</pre>
```

---

### 1.7 Blockquote and Quotation Tags

| Tag | Purpose |
|-----|---------|
| `<blockquote>` | Long quotation — displayed as an indented block |
| `<q>` | Short inline quotation — adds quotation marks automatically |
| `<cite>` | Citation/reference to a work |
| `<abbr>` | Abbreviation with a tooltip |

```html
<blockquote cite="https://www.w3.org">
  The World Wide Web is the universe of network-accessible information.
</blockquote>

<p>As Einstein said: <q>Imagination is more important than knowledge.</q></p>

<p><abbr title="HyperText Markup Language">HTML</abbr> is the language of the web.</p>
```

---

### 1.8 Special Characters (HTML Entities)

Some characters cannot be typed directly in HTML. Use **HTML entities** instead.

| Character | Entity Code | Name |
|-----------|------------|------|
| `<` | `&lt;` | Less than |
| `>` | `&gt;` | Greater than |
| `&` | `&amp;` | Ampersand |
| `"` | `&quot;` | Double quote |
| `©` | `&copy;` | Copyright |
| `®` | `&reg;` | Registered |
| `™` | `&trade;` | Trademark |
| ` ` | `&nbsp;` | Non-breaking space |
| `₹` | `&#8377;` | Indian Rupee |

```html
<p>5 &lt; 10 and 20 &gt; 15</p>
<p>Copyright &copy; 2024 My Website. All rights reserved.</p>
```

---

### 1.9 Text Color and Style (Inline CSS)

While CSS is recommended for styling, inline styles can be applied using the `style` attribute.

```html
<p style="color: blue; font-size: 20px;">This text is blue and larger.</p>
<p style="font-family: Arial; text-align: center;">Centered Arial text.</p>
<p style="background-color: yellow; color: red;">Highlighted red text.</p>
```

---

## 2. Working with Lists

### 2.1 Introduction

HTML supports three types of lists to organize and display content in a structured format:
1. **Unordered Lists** — bullet points
2. **Ordered Lists** — numbered items
3. **Definition Lists** — term-definition pairs

---

### 2.2 Unordered List (`<ul>`)

An unordered list displays items with **bullet points**. Each item is wrapped in `<li>` (list item) tags.

```html
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>
```

**Bullet style using CSS:**

```html
<ul style="list-style-type: disc;">   <!-- Default: filled circle -->
<ul style="list-style-type: circle;"> <!-- Hollow circle -->
<ul style="list-style-type: square;"> <!-- Filled square -->
<ul style="list-style-type: none;">   <!-- No bullet -->
```

---

### 2.3 Ordered List (`<ol>`)

An ordered list displays items with **numbers or letters**. The `type` attribute controls the numbering style.

```html
<ol>
  <li>Open the browser</li>
  <li>Type the URL</li>
  <li>Press Enter</li>
</ol>
```

**`type` attribute values:**

| `type` | Output |
|--------|--------|
| `type="1"` | 1, 2, 3, 4 ... (default) |
| `type="A"` | A, B, C, D ... |
| `type="a"` | a, b, c, d ... |
| `type="I"` | I, II, III, IV ... |
| `type="i"` | i, ii, iii, iv ... |

```html
<ol type="A" start="3">
  <li>First item (starts at C)</li>
  <li>Second item (D)</li>
</ol>
```

> 📝 **Note:** The `start` attribute sets the starting number/letter.

---

### 2.4 Definition List (`<dl>`)

A definition list is used for **glossary-style** content with terms and descriptions.

| Tag | Purpose |
|-----|---------|
| `<dl>` | Definition list container |
| `<dt>` | Definition term |
| `<dd>` | Definition description (indented) |

```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language — used to structure web pages.</dd>

  <dt>CSS</dt>
  <dd>Cascading Style Sheets — used to style web pages.</dd>

  <dt>JavaScript</dt>
  <dd>A programming language used to add interactivity to web pages.</dd>
</dl>
```

---

### 2.5 Nested Lists

Lists can be **nested inside each other** to create multi-level structures.

```html
<ul>
  <li>Frontend Technologies
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
  <li>Backend Technologies
    <ul>
      <li>Python</li>
      <li>Node.js</li>
    </ul>
  </li>
</ul>
```

> 📝 **Note:** You can nest ordered lists inside unordered ones and vice versa.

---

## 3. Working with Tables

### 3.1 Introduction

Tables are used to display **data in rows and columns** — like spreadsheets. HTML tables are created using a set of related tags.

---

### 3.2 Basic Table Structure

| Tag | Purpose |
|-----|---------|
| `<table>` | Defines the table |
| `<tr>` | Table Row |
| `<th>` | Table Header cell (bold + centered by default) |
| `<td>` | Table Data cell |
| `<caption>` | Title/caption for the table |

```html
<table border="1">
  <caption>Student Marks</caption>
  <tr>
    <th>Name</th>
    <th>Subject</th>
    <th>Marks</th>
  </tr>
  <tr>
    <td>Ravi</td>
    <td>HTML</td>
    <td>85</td>
  </tr>
  <tr>
    <td>Priya</td>
    <td>HTML</td>
    <td>92</td>
  </tr>
</table>
```

---

### 3.3 Table Attributes

| Attribute | Tag | Purpose |
|-----------|-----|---------|
| `border` | `<table>` | Sets border width (e.g., `border="1"`) |
| `width` | `<table>` | Sets table width (pixels or %) |
| `cellpadding` | `<table>` | Space inside each cell |
| `cellspacing` | `<table>` | Space between cells |
| `align` | `<table>` / `<td>` | Aligns table or cell content |
| `bgcolor` | `<table>` / `<td>` | Background color |
| `colspan` | `<td>` / `<th>` | Merge cells horizontally |
| `rowspan` | `<td>` / `<th>` | Merge cells vertically |

---

### 3.4 Colspan and Rowspan

**`colspan`** — merges multiple **columns** into one cell.  
**`rowspan`** — merges multiple **rows** into one cell.

```html
<table border="1">
  <tr>
    <th colspan="3">Exam Results — Semester 2</th>  <!-- spans 3 columns -->
  </tr>
  <tr>
    <th>Name</th>
    <th>HTML</th>
    <th>CSS</th>
  </tr>
  <tr>
    <td rowspan="2">Ravi</td>  <!-- spans 2 rows -->
    <td>85</td>
    <td>78</td>
  </tr>
  <tr>
    <td>90</td>
    <td>88</td>
  </tr>
</table>
```

---

### 3.5 Table Sections

For better structure and accessibility, tables can be divided into sections:

| Tag | Purpose |
|-----|---------|
| `<thead>` | Groups header rows |
| `<tbody>` | Groups body/data rows |
| `<tfoot>` | Groups footer rows |

```html
<table border="1">
  <thead>
    <tr><th>Product</th><th>Price</th></tr>
  </thead>
  <tbody>
    <tr><td>Laptop</td><td>₹55,000</td></tr>
    <tr><td>Mouse</td><td>₹500</td></tr>
  </tbody>
  <tfoot>
    <tr><td>Total</td><td>₹55,500</td></tr>
  </tfoot>
</table>
```

---

## 4. Working with Frames

### 4.1 Introduction

Frames allow a browser window to be **divided into multiple sections**, each loading a different HTML document. The main tags used are `<frameset>` and `<frame>`.

> ⚠️ **Important:** Frames (`<frameset>`) are **deprecated in HTML5**. The modern alternative is `<iframe>`. However, frames are still taught for academic purposes.

---

### 4.2 Frameset Tag (`<frameset>`)

The `<frameset>` tag **replaces** the `<body>` tag in a frame-based page. It defines how the window is split.

```html
<!DOCTYPE html>
<html>
<head><title>Frames Example</title></head>
<frameset cols="30%, 70%">
  <frame src="menu.html" name="menuFrame">
  <frame src="content.html" name="contentFrame">
</frameset>
</html>
```

**Splitting the window:**

| Attribute | Purpose | Example |
|-----------|---------|---------|
| `cols` | Split into vertical columns | `cols="25%, 75%"` |
| `rows` | Split into horizontal rows | `rows="100px, *"` |
| `*` | Takes remaining space | `cols="200, *"` |

---

### 4.3 Frame Tag (`<frame>`)

Each `<frame>` tag defines one section within a frameset.

| Attribute | Purpose |
|-----------|---------|
| `src` | URL of the page to load in this frame |
| `name` | Name used for targeting links |
| `scrolling` | `yes`, `no`, or `auto` |
| `noresize` | Prevents user from resizing the frame |
| `frameborder` | `0` (no border) or `1` (border) |

```html
<frameset rows="80px, *">
  <frame src="header.html" noresize scrolling="no">
  <frameset cols="25%, 75%">
    <frame src="sidebar.html" name="sidebar">
    <frame src="main.html" name="main">
  </frameset>
</frameset>
```

---

### 4.4 `<noframes>` Tag

The `<noframes>` tag provides **fallback content** for browsers that do not support frames.

```html
<frameset cols="30%, 70%">
  <frame src="nav.html">
  <frame src="content.html">
  <noframes>
    <body>
      <p>Your browser does not support frames. Please upgrade your browser.</p>
    </body>
  </noframes>
</frameset>
```

---

### 4.5 Inline Frames (`<iframe>`) ⭐ HTML5 Standard

The `<iframe>` (inline frame) embeds another HTML page **within the current page** — without replacing the body. This is the **modern and recommended** approach.

```html
<iframe src="https://www.example.com"
        width="600"
        height="400"
        title="Embedded Page"
        frameborder="0">
</iframe>
```

**Common `<iframe>` attributes:**

| Attribute | Purpose |
|-----------|---------|
| `src` | URL of the page to embed |
| `width` / `height` | Size of the frame |
| `title` | Accessibility label |
| `frameborder` | `0` = no border, `1` = border |
| `scrolling` | `yes`, `no`, `auto` |
| `allowfullscreen` | Allows fullscreen (used for videos) |
| `sandbox` | Restricts frame content for security |

---

## 5. Working with Hyperlinks

### 5.1 Introduction

A **hyperlink** (or simply a link) allows users to navigate from one page to another — either within the same website or to an external website. Links are created using the **anchor tag `<a>`**.

---

### 5.2 Basic Anchor Tag

```html
<a href="URL">Link Text</a>
```

```html
<a href="https://www.google.com">Visit Google</a>
<a href="about.html">About Us</a>
```

---

### 5.3 The `href` Attribute

The `href` (Hypertext REFerence) attribute specifies the **destination** of the link.

| Type | Example | Description |
|------|---------|-------------|
| External URL | `href="https://www.google.com"` | Links to another website |
| Internal page | `href="contact.html"` | Links to a page in the same site |
| Section on same page | `href="#section1"` | Jumps to an ID on the same page |
| Email link | `href="mailto:abc@gmail.com"` | Opens email client |
| Phone link | `href="tel:+919876543210"` | Initiates a phone call (mobile) |
| Download link | `href="file.pdf" download` | Downloads the file |

---

### 5.4 The `target` Attribute

The `target` attribute controls **where** the linked page opens.

| Value | Behaviour |
|-------|-----------|
| `_self` | Opens in the **same tab/window** (default) |
| `_blank` | Opens in a **new tab/window** |
| `_parent` | Opens in the **parent frame** |
| `_top` | Opens in the **full browser window** (breaks out of frames) |
| `framename` | Opens in a **named frame** |

```html
<a href="https://www.wikipedia.org" target="_blank">Open Wikipedia in New Tab</a>
<a href="page2.html" target="_self">Open in Same Tab</a>
```

---

### 5.5 Anchor Links (Bookmarks / Page Jumps)

Used to jump to a **specific section** on the same page. First, assign an `id` to the target element, then link to it using `#id`.

```html
<!-- Step 1: Create the target -->
<h2 id="contact">Contact Us</h2>

<!-- Step 2: Link to it -->
<a href="#contact">Go to Contact Section</a>
```

---

### 5.6 Image as a Hyperlink

An image can be made clickable by wrapping it inside an `<a>` tag.

```html
<a href="https://www.google.com">
  <img src="google-logo.png" alt="Go to Google" width="100">
</a>
```

---

### 5.7 Email and Phone Links

```html
<!-- Email link -->
<a href="mailto:info@college.edu">Send us an Email</a>

<!-- Phone link (for mobile) -->
<a href="tel:+919876543210">Call: +91 9876543210</a>
```

---

## 6. Working with Images

### 6.1 Introduction

Images make web pages visually appealing and informative. HTML uses the `<img>` tag to embed images. It is a **void/self-closing element** — no closing tag required.

---

### 6.2 The `<img>` Tag

```html
<img src="image.jpg" alt="Description of image">
```

**Essential Attributes:**

| Attribute | Purpose |
|-----------|---------|
| `src` | Path to the image file (required) |
| `alt` | Alternate text if image fails to load (required for accessibility) |
| `width` | Width of the image (pixels or %) |
| `height` | Height of the image (pixels or %) |
| `title` | Tooltip text on hover |
| `border` | Border around the image |
| `align` | Alignment: `left`, `right`, `center` (use CSS instead) |

```html
<img src="campus.jpg"
     alt="College Campus Photo"
     width="400"
     height="250"
     title="Our Beautiful Campus">
```

---

### 6.3 Image File Formats

| Format | Extension | Best Used For |
|--------|-----------|---------------|
| JPEG | `.jpg` / `.jpeg` | Photographs, complex images |
| PNG | `.png` | Images with transparency, logos |
| GIF | `.gif` | Simple animations, icons |
| SVG | `.svg` | Scalable vector graphics, logos |
| WebP | `.webp` | Modern format — smaller size, high quality |

---

### 6.4 Image Paths

| Path Type | Example | Description |
|-----------|---------|-------------|
| Relative | `src="images/photo.jpg"` | File within the project folder |
| Absolute | `src="https://site.com/img.png"` | Full URL to external image |
| Same folder | `src="logo.png"` | Image in the same folder as HTML file |
| Parent folder | `src="../images/photo.jpg"` | Go up one folder level |

---

### 6.5 Image with Link

```html
<a href="gallery.html">
  <img src="thumbnail.jpg" alt="View Gallery" width="150">
</a>
```

---

### 6.6 Responsive Images

```html
<!-- Using percentage width for responsiveness -->
<img src="banner.jpg" alt="Banner" style="width: 100%; max-width: 800px;">
```

---

### 6.7 Image Map (`<map>` and `<area>`)

An **image map** makes different areas of a single image clickable.

```html
<img src="india-map.jpg" alt="India Map" usemap="#indiamap" width="500">

<map name="indiamap">
  <area shape="rect"   coords="100,150,200,250" href="delhi.html"   alt="Delhi">
  <area shape="circle" coords="250,300,50"       href="mumbai.html"  alt="Mumbai">
  <area shape="poly"   coords="300,100,350,50,400,100" href="goa.html" alt="Goa">
</map>
```

**Shape types:**

| Shape | `coords` format |
|-------|----------------|
| `rect` | `x1,y1,x2,y2` (top-left and bottom-right corners) |
| `circle` | `cx,cy,radius` (center x, center y, radius) |
| `poly` | `x1,y1,x2,y2,...` (series of points) |

---

## 7. Working with Multimedia

### 7.1 Introduction

HTML5 introduced native support for **audio** and **video** without needing third-party plugins like Flash. Multimedia makes websites more engaging and interactive.

---

### 7.2 Audio Tag (`<audio>`)

The `<audio>` tag embeds sound files directly in a webpage.

```html
<audio controls>
  <source src="music.mp3" type="audio/mpeg">
  <source src="music.ogg" type="audio/ogg">
  Your browser does not support the audio element.
</audio>
```

**Attributes of `<audio>`:**

| Attribute | Purpose |
|-----------|---------|
| `controls` | Shows play/pause/volume controls |
| `autoplay` | Starts playing automatically on page load |
| `loop` | Repeats the audio continuously |
| `muted` | Starts muted |
| `preload` | `auto`, `metadata`, or `none` — how much to preload |

**Supported audio formats:**

| Format | MIME Type | Browser Support |
|--------|-----------|----------------|
| MP3 | `audio/mpeg` | All modern browsers |
| OGG | `audio/ogg` | Firefox, Chrome |
| WAV | `audio/wav` | Most browsers |
| AAC | `audio/aac` | Chrome, Safari, Edge |

---

### 7.3 Video Tag (`<video>`)

The `<video>` tag embeds video files in a webpage.

```html
<video width="640" height="360" controls poster="thumbnail.jpg">
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.webm" type="video/webm">
  Your browser does not support the video element.
</video>
```

**Attributes of `<video>`:**

| Attribute | Purpose |
|-----------|---------|
| `controls` | Shows playback controls |
| `autoplay` | Plays automatically (use with `muted` for autoplay to work in Chrome) |
| `loop` | Repeats video |
| `muted` | Starts without sound |
| `poster` | Image shown before the video plays |
| `width` / `height` | Dimensions of the video player |
| `preload` | `auto`, `metadata`, or `none` |

**Supported video formats:**

| Format | MIME Type | Notes |
|--------|-----------|-------|
| MP4 | `video/mp4` | Widest support |
| WebM | `video/webm` | Open format, Chrome/Firefox |
| OGG | `video/ogg` | Firefox |

---

### 7.4 Embedding YouTube Videos

Use `<iframe>` to embed a YouTube video:

```html
<iframe width="560"
        height="315"
        src="https://www.youtube.com/embed/VIDEO_ID"
        title="YouTube video"
        frameborder="0"
        allowfullscreen>
</iframe>
```

---

### 7.5 The `<source>` Tag

The `<source>` tag provides **multiple formats** of a media file so the browser can pick the one it supports. It is used inside `<audio>` and `<video>`.

```html
<video controls>
  <source src="clip.mp4"  type="video/mp4">
  <source src="clip.webm" type="video/webm">
  <source src="clip.ogv"  type="video/ogg">
  <!-- Fallback message for unsupported browsers -->
  <p>Your browser cannot play this video.</p>
</video>
```

---

### 7.6 The `<object>` and `<embed>` Tags

These older tags were used to embed external content (PDFs, Flash, plugins). Still used occasionally.

```html
<!-- Embed a PDF -->
<object data="document.pdf" type="application/pdf" width="600" height="400">
  <p>PDF cannot be displayed. <a href="document.pdf">Download it here.</a></p>
</object>

<!-- The embed tag (simpler, self-closing) -->
<embed src="document.pdf" type="application/pdf" width="600" height="400">
```

---

## 8. Working with Forms and Controls

### 8.1 Introduction

HTML **forms** are used to **collect input from users**. Form data is sent to a web server for processing. Forms are used for login pages, registration, search boxes, surveys, and much more.

---

### 8.2 The `<form>` Tag

The `<form>` tag creates a container for all form elements.

```html
<form action="submit.php" method="post">
  <!-- form elements go here -->
</form>
```

**Key attributes of `<form>`:**

| Attribute | Purpose |
|-----------|---------|
| `action` | URL where form data is sent on submission |
| `method` | HTTP method: `get` (visible in URL) or `post` (hidden) |
| `enctype` | Encoding type — use `multipart/form-data` for file uploads |
| `name` | Name for the form |
| `autocomplete` | `on` or `off` — browser autocomplete |
| `novalidate` | Disables browser-side validation |

**GET vs POST:**

| Feature | GET | POST |
|---------|-----|------|
| Data visibility | Visible in URL | Hidden in request body |
| Security | Less secure | More secure |
| Data limit | ~2000 chars | No practical limit |
| Use case | Search, filters | Login, registration, payments |

---

### 8.3 The `<input>` Tag

The `<input>` tag is the most versatile form control. The `type` attribute defines what kind of input it creates.

```html
<input type="text" name="username" placeholder="Enter your name">
```

**Input `type` values:**

| Type | Description | Example |
|------|-------------|---------|
| `text` | Single-line text field | Name, city |
| `password` | Masked text field | Password |
| `email` | Email address (with validation) | user@mail.com |
| `number` | Numeric input with arrows | Age, quantity |
| `tel` | Telephone number | +91 98765 43210 |
| `url` | Web address | https://... |
| `date` | Date picker | 2024-01-15 |
| `time` | Time picker | 09:30 AM |
| `datetime-local` | Date and time together | — |
| `month` | Month and year picker | — |
| `range` | Slider for a range | Volume, brightness |
| `color` | Color picker | #FF5733 |
| `checkbox` | Check box (multiple selections) | Hobbies |
| `radio` | Radio button (single selection) | Gender |
| `file` | File upload | Upload photo |
| `hidden` | Hidden data (not shown to user) | Session token |
| `submit` | Submit button | Submit Form |
| `reset` | Reset button | Clear Form |
| `button` | Generic clickable button | — |
| `search` | Search input field | Search... |
| `image` | Image as submit button | — |

---

### 8.4 Common Input Attributes

| Attribute | Purpose |
|-----------|---------|
| `name` | Key used when data is submitted (required) |
| `id` | Unique identifier (used with `<label>`) |
| `value` | Default/initial value |
| `placeholder` | Hint text shown inside the field |
| `required` | Makes the field mandatory |
| `readonly` | Field is visible but not editable |
| `disabled` | Field is greyed out and not submitted |
| `maxlength` | Maximum number of characters allowed |
| `min` / `max` | Min and max values (for number, date) |
| `step` | Step increment (for number, range) |
| `checked` | Pre-checks checkbox or radio button |
| `multiple` | Allows multiple values (email, file) |
| `autofocus` | Field gets focus on page load |
| `pattern` | Regex pattern for validation |
| `size` | Visible width of the input field |

---

### 8.5 Complete Form Example

```html
<form action="register.php" method="post" enctype="multipart/form-data">

  <label for="fname">First Name:</label>
  <input type="text" id="fname" name="firstname" placeholder="Enter first name" required><br><br>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="user@example.com" required><br><br>

  <label for="pwd">Password:</label>
  <input type="password" id="pwd" name="password" minlength="8" required><br><br>

  <label for="dob">Date of Birth:</label>
  <input type="date" id="dob" name="dob"><br><br>

  <label>Gender:</label>
  <input type="radio" name="gender" value="male" id="male">
  <label for="male">Male</label>
  <input type="radio" name="gender" value="female" id="female">
  <label for="female">Female</label><br><br>

  <label>Hobbies:</label>
  <input type="checkbox" name="hobby" value="reading"> Reading
  <input type="checkbox" name="hobby" value="coding">  Coding
  <input type="checkbox" name="hobby" value="sports">  Sports<br><br>

  <label for="country">Country:</label>
  <select id="country" name="country">
    <option value="">-- Select Country --</option>
    <option value="india">India</option>
    <option value="usa">USA</option>
    <option value="uk">UK</option>
  </select><br><br>

  <label for="about">About You:</label><br>
  <textarea id="about" name="about" rows="4" cols="40"
            placeholder="Write something about yourself..."></textarea><br><br>

  <label for="photo">Upload Photo:</label>
  <input type="file" id="photo" name="photo" accept="image/*"><br><br>

  <input type="submit" value="Register">
  <input type="reset" value="Clear Form">

</form>
```

---

### 8.6 The `<textarea>` Tag

A multi-line text input field.

```html
<textarea name="message" rows="5" cols="40" placeholder="Enter your message...">
</textarea>
```

| Attribute | Purpose |
|-----------|---------|
| `rows` | Number of visible lines |
| `cols` | Visible width in characters |
| `placeholder` | Hint text |
| `maxlength` | Maximum characters allowed |
| `readonly` | Makes it read-only |

---

### 8.7 The `<select>` and `<option>` Tags

A dropdown list control.

```html
<select name="branch">
  <option value="">-- Choose Branch --</option>
  <option value="cs"  selected>Computer Science</option>
  <option value="ds">Data Science</option>
  <option value="it">Information Technology</option>
</select>
```

**`<optgroup>` — Grouping options:**

```html
<select name="course">
  <optgroup label="Science">
    <option value="bsc">B.Sc.</option>
    <option value="msc">M.Sc.</option>
  </optgroup>
  <optgroup label="Commerce">
    <option value="bcom">B.Com</option>
    <option value="mcom">M.Com</option>
  </optgroup>
</select>
```

---

### 8.8 The `<label>` Tag

Labels improve **accessibility** by associating text with a form control. Clicking the label focuses the input.

```html
<!-- Method 1: Using 'for' and 'id' -->
<label for="username">Username:</label>
<input type="text" id="username" name="username">

<!-- Method 2: Wrapping the input -->
<label>
  Email:
  <input type="email" name="email">
</label>
```

---

### 8.9 The `<fieldset>` and `<legend>` Tags

`<fieldset>` groups related form elements inside a box. `<legend>` provides a title for the group.

```html
<fieldset>
  <legend>Personal Information</legend>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name"><br><br>
  <label for="age">Age:</label>
  <input type="number" id="age" name="age">
</fieldset>

<fieldset>
  <legend>Login Credentials</legend>
  <label for="uid">Username:</label>
  <input type="text" id="uid" name="uid"><br><br>
  <label for="pass">Password:</label>
  <input type="password" id="pass" name="pass">
</fieldset>
```

---

### 8.10 The `<datalist>` Tag

Provides **autocomplete suggestions** for a text input.

```html
<label for="browser">Favourite Browser:</label>
<input list="browsers" id="browser" name="browser" placeholder="Type to search...">

<datalist id="browsers">
  <option value="Chrome">
  <option value="Firefox">
  <option value="Safari">
  <option value="Edge">
  <option value="Opera">
</datalist>
```

---

### 8.11 HTML5 Form Validation

HTML5 provides **built-in client-side validation** — no JavaScript needed.

```html
<form>
  <!-- Required field -->
  <input type="text" name="name" required placeholder="Name is required">

  <!-- Email format check -->
  <input type="email" name="email" required>

  <!-- Number range -->
  <input type="number" name="age" min="18" max="60">

  <!-- Pattern matching (10-digit phone) -->
  <input type="tel" name="phone" pattern="[0-9]{10}" title="Enter 10-digit number">

  <!-- Minimum length -->
  <input type="password" name="pwd" minlength="8">

  <input type="submit" value="Submit">
</form>
```

---

## 9. Key Concepts Summary

| Topic | Key Tags | Purpose |
|-------|----------|---------|
| **Text** | `<h1>`–`<h6>`, `<p>`, `<b>`, `<i>`, `<strong>`, `<em>`, `<br>`, `<hr>`, `<pre>` | Format and structure text content |
| **Lists** | `<ul>`, `<ol>`, `<li>`, `<dl>`, `<dt>`, `<dd>` | Organize items in bullet/numbered/definition lists |
| **Tables** | `<table>`, `<tr>`, `<th>`, `<td>`, `<caption>`, `<thead>`, `<tbody>`, `<tfoot>` | Display data in rows and columns |
| **Frames** | `<frameset>`, `<frame>`, `<iframe>`, `<noframes>` | Divide window into sections or embed pages |
| **Hyperlinks** | `<a href="...">` | Navigate between pages or sections |
| **Images** | `<img>`, `<map>`, `<area>` | Embed and map images |
| **Multimedia** | `<audio>`, `<video>`, `<source>`, `<embed>`, `<object>` | Embed audio, video, and media |
| **Forms** | `<form>`, `<input>`, `<textarea>`, `<select>`, `<label>`, `<fieldset>` | Collect and submit user input |

---

## 10. Review Questions

### Short Answer Questions

1. What is the difference between `<b>` and `<strong>`? When should each be used?
2. What is the purpose of the `alt` attribute in the `<img>` tag?
3. Differentiate between ordered and unordered lists with examples.
4. What are `colspan` and `rowspan`? Give an example of each.
5. What is the difference between `<frameset>` and `<iframe>`?
6. What does the `target="_blank"` attribute do in a hyperlink?
7. What is the difference between `GET` and `POST` methods in a form?
8. What is the purpose of the `<label>` tag in HTML forms?
9. List any four HTML5 input types with their use cases.
10. What is an image map? Name the tags used to create one.

### Long Answer / Practical Questions

11. Create an HTML page with a **registration form** that includes: name, email, password, date of birth, gender (radio), hobbies (checkboxes), country (dropdown), and a submit button.
12. Design an HTML table showing the **timetable for one week** with proper use of `colspan` and `rowspan`.
13. Write an HTML page that uses **nested lists** to show the curriculum of 3 semesters with subjects under each semester.
14. Create a webpage with a **navigation menu using hyperlinks** where clicking each link loads the content in an iframe.
15. Write an HTML page that **embeds a video** with controls, a poster image, and a fallback message for unsupported browsers.

---

## 📌 Exam Tips

> Keep these handy before your exam!

1. `<img>` and `<br>` are **void elements** — they don't need closing tags.
2. **`<frameset>` replaces `<body>`** — they cannot be used together.
3. Use **`<iframe>`** for embedding pages in HTML5 (frameset is deprecated).
4. In forms, **`name` attribute** is required for data to be submitted — `id` is just for JavaScript/CSS.
5. Always use **`<label>`** with `for="id"` — improves accessibility and usability.
6. Radio buttons with the **same `name`** form a group — only one can be selected.
7. For file uploads, the form **must use `method="post"` and `enctype="multipart/form-data"`**.
8. HTML5 input types (`email`, `date`, `range`, `color`) provide **built-in validation** — no JavaScript needed.
9. The `<source>` tag lets you provide **multiple media formats** for better browser compatibility.
10. `colspan` merges **columns (horizontal)**; `rowspan` merges **rows (vertical)**.

---

<div align="center">

*Detailed Notes — Web Designing (HTML)*
*B.Sc. Data Science & AI · Semester 2*

</div>
