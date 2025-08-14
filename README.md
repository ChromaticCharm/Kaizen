# HTML Tutorial | By ChromaticCharm

HTML (HyperText Markup Language) is the standard language used to structure web content. It defines the meaning and structure of documents on the Web. Every web page is built from HTML elements – tags like `<h1>`, `<p>`, `<a>`, etc. – which browsers interpret to display text, images, links, and multimedia. This tutorial covers key HTML topics from basics to advanced, with simple explanations and code examples to illustrate each concept.

## Introduction

HTML stands for **HyperText Markup Language**. It provides the skeleton of a webpage: text content wrapped in tags that tell the browser how to display and organize information. For example, `<p>Hello World</p>` creates a paragraph. The basic HTML page structure includes a doctype declaration and `<html>`, `<head>`, and `<body>` elements. A minimal HTML document looks like:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>Main Heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

Here, `<title>` sets the browser tab title, and `<h1>`, `<p>` mark a heading and a paragraph, respectively. Always start with `<!DOCTYPE html>` to tell browsers you are using HTML5.

## HTML Editors

To write HTML, you need a text editor. Options range from simple text editors (Notepad, TextEdit) to code-oriented editors (VS Code, Sublime Text, Atom) which offer syntax highlighting and auto-completion. Beginners often use **Visual Studio Code** or **Notepad++** for ease of use. Web-based editors (like [CodePen](https://codepen.io) or [JSFiddle](https://jsfiddle.net)) allow instant HTML editing and preview in a browser. Choose one you are comfortable with; modern editors save files with a `.html` extension.

## Basic HTML Structure

Every HTML file begins with a doctype and an `<html>` element encompassing the page. Inside `<html>`, a `<head>` element contains metadata (like `<title>`, character encoding, linked CSS/JS), and a `<body>` contains the visible content. For example:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Page</title>
    <meta charset="UTF-8">
  </head>
  <body>
    <h1>Welcome!</h1>
    <p>This is my first webpage.</p>
  </body>
</html>
```

* **`<!DOCTYPE html>`** declares the document as HTML5.
* **`<html>`** is the root element.
* **`<head>`** includes the page `<title>`, metadata (`<meta charset="UTF-8">` sets character encoding), and links to stylesheets or scripts.
* **`<body>`** holds the content that displays in the browser.

## HTML Elements and Attributes

An **HTML element** consists of a *start tag*, *content*, and an *end tag* (e.g., `<p>content</p>`). Some elements are *void* (empty) and self-close, like `<img>` or `<br>`. Elements can have **attributes**, which provide additional information in the start tag. Attributes are written as `name="value"` pairs. For example `<a href="https://example.com" target="_blank">Link</a>` has `href` and `target` attributes. In general, “attributes provide additional information about an element, placed inside the element’s opening tag.” Each attribute name must be unique on that element, and values are quoted. A tag can have multiple attributes separated by spaces.

## Headings

HTML provides six heading levels, `<h1>` through `<h6>`, to structure content. `<h1>` is the top-level heading (often the page title), and `<h6>` is the least important. By default, headings are **block-level** elements (they start on a new line). For example:

```html
<h1>Main Title</h1>
<h2>Subsection</h2>
<h3>Sub-subsection</h3>
```

Search engines and accessibility tools use headings to understand page structure, so use them semantically. `<h1>` should generally appear once per page, then use `<h2>` for major sections, `<h3>` for subsections, etc..

## Paragraphs

The `<p>` element defines a paragraph of text. Browsers automatically add some vertical space before and after each `<p>`, separating paragraphs with blank lines. Example:

```html
<p>This is the first paragraph of text. It appears on its own line in the browser.</p>
<p>This is a second paragraph, which will be separated from the first by some space.</p>
```

Each `<p>` must have a closing tag `</p>`, except in some cases where an HTML parser can infer it. Paragraphs are **block-level**, so they start on a new line and fill the width of their container.

## Text Styles and Formatting

HTML offers tags to style text semantically or for emphasis. Some common tags:

* `<strong>` or `<b>`: bold text. (`<strong>` also indicates importance.)
* `<em>` or `<i>`: italic text. (`<em>` implies emphasis.)
* `<u>`: underline (less used nowadays).
* `<small>`: smaller text.
* `<mark>`: highlighted text.
* `<sup>` and `<sub>`: superscript and subscript (for footnotes, formulas).

For example:

```html
<p>This is <strong>important</strong> and this is <em>emphasized</em>.</p>
```

**Note:** Use these tags for meaning, not purely for appearance. Use CSS for general styling whenever possible (see “HTML CSS” below).

## Quotations

To include quotes or citations:

* `<blockquote>`: for long (block) quotes. Browsers usually indent it.
* `<q>`: for short, inline quotes. Browsers usually add quotation marks.
* `<abbr title="...">`: to mark an abbreviation or acronym, with a title.

Example:

```html
<blockquote cite="https://example.com">
  This is a long quotation from another source.
</blockquote>
<p>Albert Einstein once said, <q>The important thing is not to stop questioning.</q></p>
```

The `<blockquote>` tag can include a `cite` attribute to reference the source. Screen readers know these as quotations.

## Comments

You can insert comments in HTML that are not displayed in the browser by using `<!-- comment here -->`. Comments help document code for developers. For example:

```html
<!-- This is a comment and will be ignored by the browser -->
<p>This is visible content.</p>
```

Never put sensitive information in comments, as they remain in the HTML source.

## HTML Colors

Colors in HTML are generally specified via CSS (inline or external). You can use color names or values:

* **Named colors** (like `"red"`, `"blue"`, `"orange"`, etc.)
* **Hex codes** (like `#FF0000` for red)
* **RGB/RGBA** (like `rgb(255,0,0)` or `rgba(255,0,0,0.5)`)
* **HSL/HSLA** (like `hsl(0,100%,50%)`)

For example, to color text red:

```html
<p style="color: blue;">This text is blue.</p>
```

Or in CSS:

```css
p { color: #FF0000; } /* red */
```

Named colors and these formats are standard; in HTML (via CSS) you can specify any of these.

## CSS (Styling)

While HTML defines structure, CSS (Cascading Style Sheets) defines presentation (layout, colors, fonts). In HTML, use the `<style>` tag or `style` attribute for quick styling, or link to an external CSS file with `<link>`. For example:

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1 style="color: teal;">Hello World</h1>
</body>
```

This links an external CSS file and also shows inline CSS via `style`. It’s best practice to keep CSS in separate files. The `<link>` tag (with `rel="stylesheet"`) is placed in `<head>`.

Key point: HTML should only define **what** the content is, while CSS defines **how** it looks.

## Links

Hyperlinks use the `<a>` element with the `href` attribute. Example:

```html
<a href="https://www.example.com">Visit Example.com</a>
```

This creates a clickable link. The `href` value can be a full URL (absolute) or a relative path to a file on your site. You can also add `target="_blank"` to open the link in a new tab. For example:

```html
<a href="page2.html" target="_blank">Open Page 2 in a new tab</a>
```

The `<a>` tag can wrap text or other inline elements to make them clickable. For accessibility, always include link text inside `<a>`.

## Images

Use `<img>` to embed images. Required attributes: `src` (the image URL or file path) and `alt` (a text description for accessibility). Example:

```html
<img src="picture.jpg" alt="A descriptive caption" width="300" height="200">
```

* `src`: path to the image file (can be a relative path or full URL).
* `alt`: describes the image content for screen readers or if image fails to load. It is **mandatory** for accessibility.

The image is an inline-replaced element, meaning it flows with text. Always include a meaningful `alt` attribute so that visually impaired users can understand the image.

## Favicon

A *favicon* is the small icon shown in the browser tab or bookmark bar for your site. To add one, put an icon file (usually a 16×16 or 32×32 PNG/ICO) in your site and include in `<head>`:

```html
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

The `<link rel="icon">` tag is used for favicons. Modern browsers accept many formats (PNG, SVG, ICO). The favicon path can be relative or absolute.

## Page Title

The `<title>` tag inside `<head>` sets the page title (shown on the browser tab and in search results). For example:

```html
<title>My Webpage Title</title>
```

The `<title>` element’s text must be plain text (no tags). It should briefly describe the page. This is crucial for SEO and usability.

## Tables

HTML tables organize data into rows and columns. Basic tags:

* `<table>`: the container for a table.
* `<tr>`: table row.
* `<th>`: header cell (usually bold and centered by default).
* `<td>`: data cell.

Example:

```html
<table>
  <tr>
    <th>Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>Alice</td>
    <td>30</td>
  </tr>
  <tr>
    <td>Bob</td>
    <td>25</td>
  </tr>
</table>
```

This creates a table with a header row (“Name”, “Age”) and two data rows. By default, tables have no border or spacing. You can add attributes like `border`, `cellpadding`, `cellspacing` (deprecated) or better use CSS (e.g., `border-collapse: collapse;`).

MDN explains `<table>` represents tabular data in rows and columns.

## Lists

HTML supports ordered and unordered lists:

* **Unordered list** (`<ul>`): bullet points.
* **Ordered list** (`<ol>`): numbered list.
* **Description list** (`<dl>`): terms and descriptions (defined list).

Each list contains `<li>` items. For example:

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>
<ol>
  <li>First step</li>
  <li>Second step</li>
</ol>
```

This displays a bulleted list of fruits and a numbered list of steps. Use `<dl>` with `<dt>` and `<dd>` for definition lists.

MDN notes `<ul>` and `<ol>` both create lists of items; `<ol>` implies order matters. The default style (bullets or numbers) can be changed via CSS (e.g., `list-style`).

## Block vs. Inline Elements

HTML elements are **block-level** or **inline-level**. Block elements (like `<div>`, `<p>`, `<h1>`) start on a new line and take the full width by default. Inline elements (like `<span>`, `<a>`, `<img>`) flow within a line and only take up as much width as needed.

* **Block**: `<div>`, `<p>`, `<h1>` – occupy full width, new line.
* **Inline**: `<span>`, `<a>`, `<em>`, `<img>` – flow with text, don’t force new lines.

Understanding this helps in layout. For instance, `<div>` is a block container (see next topic), while `<span>` is an inline container (for styling small chunks of text).

## Div

The `<div>` element is a generic container with no inherent meaning or styling. It is used to group other elements, usually for styling or scripting. By default, `<div>` is block-level. Example:

```html
<div class="header">
  <h1>Welcome</h1>
</div>
```

This creates a block (e.g., header) that can be styled via CSS (e.g., `.header { background: gray; }`). MDN notes that `<div>` “has no effect on content or layout until styled with CSS”. Use `<div>` to wrap sections when no semantic tag applies, but HTML5 provides many semantic tags (see Layout/Semantics) which are often preferred.

## Classes

The `class` attribute lets you assign a class name (or names) to an element, which can be used by CSS or JavaScript. For example:

```html
<p class="intro">This paragraph is styled with the "intro" class.</p>
```

Multiple elements can share a class, and an element can have multiple classes (separated by spaces). In CSS, refer to classes with a dot: `.intro { font-weight: bold; }`. As MDN explains, `class` is a global attribute listing class values separated by spaces. Use descriptive class names to indicate purpose (e.g., `.nav-bar`, `.footer-link`).

## Id

The `id` attribute assigns a unique identifier to an element (one per page). For example:

```html
<div id="main-content">
  <p id="intro-paragraph">Hello!</p>
</div>
```

IDs must be unique in the document. They can be used in CSS with `#` or in JavaScript (`document.getElementById("intro-paragraph")`). IDs are often used for anchoring (linking to a page section with `href="#intro-paragraph"`) or scripting. MDN notes that `id` is used for linking, scripting, or styling a single element. Because IDs are global, avoid generic words (like “header”); instead, use specific names (e.g., `site-header`).

## Iframes

An `<iframe>` (Inline Frame) embeds another HTML page within your page. This is commonly used for ads, embeds, or cross-origin content. Example:

```html
<iframe src="https://www.example.com" width="600" height="400" title="Example Site"></iframe>
```

This shows the content of `example.com` in a 600×400 area. The `title` attribute (not shown above) should be included for accessibility to describe the frame’s content. As MDN states, `<iframe>` represents a nested browsing context (an embedded document). Note that iframes have performance and security implications (like same-origin restrictions) but are useful for embedding external pages or videos.

## File Paths

HTML resources (images, links, scripts) use **paths** to locate files. Two main types:

* **Absolute paths**: full URL including protocol (e.g., `https://example.com/image.png`). These point to exactly one location on the web. Use absolute for resources on other sites.
* **Relative paths**: path relative to the current HTML file’s location. For example, if your page and image are in the same folder: `<img src="photo.jpg">`. If image is in a subfolder “images”, use `<img src="images/photo.jpg">`. Relative paths make your site portable across domains.

Example of relative path:

```html
<img src="images/geeks.jpg" alt="My Image"> <!-- images/geeks.jpg is in a subfolder -->
```

Root-relative paths start with `/` (root of domain), e.g., `/assets/pic.png`. Also use `.` and `..` to navigate directories (e.g., `../` goes up one folder).

## Head

The `<head>` element (inside `<html>`) contains metadata and resources for the document. Elements in `<head>` include:

* `<title>`: the page title shown in the browser tab.
* `<meta>`: character set (`charset=UTF-8`), viewport, description, etc.
* `<link>`: external resources (stylesheets, favicons).
* `<style>`: internal CSS.
* `<script>`: external or inline JavaScript (though scripts can also be placed before `</body>`).

For example:

```html
<head>
  <meta charset="UTF-8">
  <title>Example Page</title>
  <link rel="stylesheet" href="styles.css">
</head>
```

MDN notes the `<head>` is a container for metadata and resources (not displayed directly).

## Layout

HTML5 introduces semantic elements for page sections: `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`, etc. Using these instead of generic `<div>`s helps organize content. For example:

```html
<header>
  <h1>Site Title</h1>
  <nav>…</nav>
</header>
<main>
  <article>…</article>
  <aside>…</aside>
</main>
<footer>© 2025 My Site</footer>
```

Each of these tags describes its content’s role. For instance, `<nav>` holds navigation links, `<section>` groups a thematic block, and `<footer>` contains bottom information. This semantic structure makes HTML more meaningful. W3Schools highlights these layout tags in HTML5.

For multi-column or responsive layouts, HTML itself doesn’t do the layout – use CSS (e.g., Flexbox, Grid, floats). However, semantic markup (above) provides a skeleton for CSS to style.

## Responsive Design

To make pages adapt to mobile devices, use the viewport meta tag and responsive CSS. In `<head>` include:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

This tells mobile browsers to set the page width to the device width. Without it, mobile browsers may zoom out on desktop-scaled pages.

Then, use CSS media queries (outside of HTML) to adjust layout for different screens (e.g., `@media (max-width: 600px) { … }`). Fluid units (percentages, flexbox) help too. In summary: declare the viewport in HTML and use CSS for responsiveness.

## Semantics

*Semantic HTML* means using elements according to their meaning, not just visual effect. For example, use `<em>` to emphasize text instead of just making it italic with CSS. Semantic markup improves accessibility and SEO. Benefits include:

* **Accessibility**: Screen readers use tags (like `<nav>`, `<main>`, headings) to help visually impaired users navigate.
* **Search Engine Optimization**: Search engines treat semantic tags as important structure, influencing search ranking.
* **Maintainability**: It’s easier for developers to understand code if tags reflect content meaning.

MDN emphasizes using the correct elements for the right job. For example, don’t use `<div>` everywhere when `<article>`, `<section>`, `<header>`, etc., exist. Always think: “What is this content? Which tag best describes it?”

## Style Guide

Clean, consistent HTML is easier to read and maintain. Common conventions:

* Use **lowercase** for all tag and attribute names (e.g., `<div>`, not `<DIV>`).
* Quote all attribute values with double quotes.
* Indent nested elements (e.g., 2 spaces per level).
* Always include the doctype (`<!DOCTYPE html>`) at the top.
* Use meaningful class and id names, and keep formatting tidy.
* Avoid inline styles unless necessary; prefer external CSS.

Following a style guide (like Google’s HTML/CSS guide) ensures consistency: indent with spaces, lowercase tags/attrs, no trailing spaces.

## Entities

Some characters have special meaning in HTML (like `<` and `&`). Use **character entities** (references) to display these. For example:

* `&lt;` renders as `<`.
* `&gt;` renders as `>`.
* `&amp;` renders as `&`.
* `&quot;` renders as `"`.

These ensure the characters are not interpreted as HTML. For instance:

```html
<p>5 &lt; 10 and 10 &amp; 20 are examples of entities.</p>
```

MDN explains an HTML entity is a pattern representing another character. You can also use numeric codes (e.g., `&#169;` for ©).

## Symbols

In addition to basic entities, HTML supports many symbol entities (for math, currency, etc.). For example:

* `&copy;` for ©
* `&euro;` for €
* `&mdash;` for — (em dash)
* `&hearts;` for ♥
  You can also use Unicode code points (`&#x2665;` for ♥). These are handy for symbols not on the keyboard. Many of these are listed in references (e.g., the \[HTML Entities] reference).

## Emojis

Emojis are simply Unicode characters. You can include them directly (if your file is UTF-8) or via numeric entity. For example:

* Direct emoji: `<p>Happy face: 😄</p>`
* Numeric code: `&#128516;` also renders 😄.

MDN notes emojis are part of UTF-8 character set. No special HTML tag is needed—just treat them as text. For compatibility, ensure `<meta charset="UTF-8">` is in `<head>` so emojis display correctly.

---

## HTML Forms

HTML forms collect user input. Wrap form controls inside a `<form>` element. Example:

```html
<form action="/submit" method="post">
  <div>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
  </div>
  <input type="submit" value="Send">
</form>
```

* The `<form>` element defines a section for inputs and a submit button.
* `action` attribute: the URL where form data is sent (e.g., `/submit`).
* `method`: how to send data, typically `get` or `post`. `get` appends data to URL (not for sensitive data), `post` sends data in request body.

Inside a form, use:

* `<label>`: associates text with an input (via `for="id"`). Good for accessibility.
* `<input>`: for text fields, checkboxes, radios, etc..
* `<textarea>`: for multi-line text.
* `<button type="submit">` or `<input type="submit">`: to submit the form.
* `<select>` with `<option>`: dropdown lists.
* Other controls: `<fieldset>`, `<legend>`, `<label>`.

Form **attributes** include (besides `action`/`method`):

* `id`, `name`: name identifies the form (rarely needed).
* `autocomplete`: on/off for browser autofill.
* `novalidate`: disable HTML5 validation.

An example of input and form attributes:

```html
<form action="/search" method="get">
  <label for="q">Search:</label>
  <input type="search" id="q" name="q" required placeholder="Type keywords">
  <input type="submit" value="Go">
</form>
```

Here, `required` makes the field mandatory, and `placeholder` shows hint text. Common input attributes include `name`, `value`, `required`, `placeholder`, `min`, `max`, etc.

## Form Elements

Inside a form, you can include various input controls:

* **Text fields:** `<input type="text">`, `<input type="password">`, `<input type="email">` etc.
* **Checkboxes and radios:** `<input type="checkbox">`, `<input type="radio">`. For grouping radios, use the same `name` on multiple radio inputs.
* **Buttons:** `<button>` or `<input type="button|submit|reset">`.
* **Textarea:** `<textarea>` for multi-line input.
* **Dropdowns:** `<select><option>` lists.
* **File upload:** `<input type="file">`.

Each control should have a `name` attribute; this becomes the key when the form is submitted. Labels (`<label for="...">`) should reference the input’s `id` to improve usability.

## Input Types

HTML5 added many input types:

* `text`, `password`, `email`, `url`, `number`, `tel`, `date`, `color`, `search`, `range`, `file`, `checkbox`, `radio`, `submit`, etc.
* Example: `<input type="email" name="userEmail">` shows an email field (mobile devices may show the “@” key).
* `<input type="number" name="age" min="1" max="120">` for numeric input.
* `<input type="date" name="dob">` for date picker on supporting browsers.

MDN notes `<input>` is one of the most powerful elements due to many type and attribute combinations. If `type` is omitted, the default is `"text"`.

## Input Attributes

Common global and input-specific attributes:

* `name`: field name for form submission.
* `id`: unique identifier, linked with `<label for>`.
* `value`: default value of the control.
* `placeholder`: hint text inside empty input (not submitted).
* `required`: requires the field to be filled before submit.
* `readonly` / `disabled`: prevent user editing or submission.
* Validation attributes: `min`, `max`, `pattern`, `maxlength`, `step` (for numeric types).

Example:

```html
<input type="text" id="username" name="username" required maxlength="12" placeholder="Username">
```

This input must be filled and max 12 characters. Use these to leverage browser validation.

---

## HTML Graphics

HTML provides two main ways to render custom graphics:

* **Canvas (`<canvas>`)**: a bitmap drawing area that you control with JavaScript (2D drawing, animations, WebGL). Example:

  ```html
  <canvas id="myCanvas" width="200" height="100"></canvas>
  <script>
    const ctx = document.getElementById('myCanvas').getContext('2d');
    ctx.fillStyle = 'red';
    ctx.fillRect(10, 10, 150, 75);
  </script>
  ```

  The `<canvas>` element itself is just a blank rectangular region. Using the Canvas API (in JavaScript), you can draw shapes, images, etc.

* **SVG (`<svg>`)**: Scalable Vector Graphics, where shapes (lines, circles, paths) are defined in XML. SVG images scale without loss of quality. Example:

  ```html
  <svg width="100" height="100">
    <circle cx="50" cy="50" r="40" stroke="green" fill="yellow" />
  </svg>
  ```

  The `<svg>` tag defines a new coordinate system for vector drawings. Inside, use elements like `<circle>`, `<rect>`, `<path>`, etc. SVG is ideal for icons, charts, and graphics that need to scale.

MDN notes you use `<canvas>` for scripted graphics and animations, and `<svg>` as a container for vector graphics.

## HTML Media

HTML5 includes tags for embedding media:

* **Audio** (`<audio>`): for sound files (MP3, WAV, etc.). Use `controls` to show playback controls.

  ```html
  <audio controls>
    <source src="sound.mp3" type="audio/mpeg">
    <p>Your browser does not support the audio element.</p>
  </audio>
  ```

  The browser plays the first compatible source. Without `controls`, use JavaScript to play. The content inside `<audio>` (like a message or link) shows if the element isn’t supported. MDN says `<audio>` embeds sound content.

* **Video** (`<video>`): for video playback (MP4, WebM, etc.). Similar to `<audio>`:

  ```html
  <video controls width="320" height="240">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    <p>Your browser does not support the video tag.</p>
  </video>
  ```

  It embeds a player with play/pause, etc. Use `<source>` tags for multiple formats. MDN notes `<video>` is a media player for video (and can handle audio too).

* **Attributes**: common ones include `controls`, `autoplay`, `loop`, `muted`, `poster` (for video), and global attributes. For audio/video, always include controls (or provide your own JS controls).

### YouTube

To embed a YouTube video, use an `<iframe>` with YouTube’s embed URL. Steps:

1. Upload or pick a video on YouTube and note its **video ID** (e.g., `tgbNymZ7vqY`).
2. Insert an `<iframe>` in your HTML with `src="https://www.youtube.com/embed/VIDEO_ID"`, and set `width`/`height`.

Example:

```html
<iframe width="560" height="315"
        src="https://www.youtube.com/embed/tgbNymZ7vqY"
        title="YouTube video player"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen>
</iframe>
```

This plays the YouTube video in your page. You can add parameters (like `?autoplay=1`) to the URL for autoplay, mute, etc. W3Schools shows a basic iframe example for YouTube. The `allowfullscreen` attribute lets users view full screen.

---

## References

All information above is sourced from official documentation and reputable tutorials. Key references include the Mozilla Developer Network (MDN) and educational resources:

* MDN Web Docs (HTML element references): e.g., **HTML Intro**, **Headings**, **Forms**, **Media**, etc.
* W3Schools tutorials (for examples and lists): e.g., **HTML Colors**, **HTML Style Guide**, **HTML YouTube**
* MDN Glossary and guides (for concepts like semantics and entities).

These sources provide authoritative details on HTML usage, syntax, and best practices. The examples and explanations here combine that guidance with concise code snippets for clarity.
