- [HTML Basics](#"HTML""Basics")
  - [Doctype Declaration](#"Doctype""Declaration")
  - [Html Tag](#"Html""Tag")
  - [Head Tag](#"Head""Tag")
  - [Meta Tags](#"Meta""Tags")
  - [Title Tag](#"Title""Tag")
- [Body And Styling](#"Body""And""Styling")
  - [Body Tag](#"Body""Tag")
- [Headings](#"Headings")
  - [H1 To H6](#"H1""To""H6")
- [Text Tags](#"Text""Tags")
  - [P Tag](#"P""Tag")
  - [Br Tag](#"Br""Tag")
- [Links](#"Links")
  - [A Tag](#"A""Tag")
- [Images](#"Images")
  - [Img Tag](#"Img""Tag")
- [Lists](#"Lists")
  - [Ul Tag Unordered List](#"Ul""Tag""Unordered""List")
  - [Ol Tag Ordered List](#"Ol""Tag""Ordered""List")
  - [Li Tag](#"Li""Tag")
- [Definition List](#"Definition""List")
  - [Dl Dt Dd Tags](#"Dl""Dt""Dd""Tags")
- [Semantic Tags](#"Semantic""Tags")
  - [Header Tag](#"Header""Tag")
  - [Nav Tag](#"Nav""Tag")
  - [Section Tag](#"Section""Tag")
- [Media Tags](#"Media""Tags")
  - [Audio Tag](#"Audio""Tag")
  - [Video Tag](#"Video""Tag")
- [Tables](#"Tables")
  - [Table Basics](#"Table""Basics")
  - [Table Sections](#"Table""Sections")
  - [Column Styling](#"Column""Styling")
- [Forms](#"Forms")
  - [Form Basics](#"Form""Basics")
  - [Fieldset And Legend](#"Fieldset""And""Legend")
  - [Label Tag](#"Label""Tag")
  - [Input Types Text And Password](#"Input""Types""Text""And""Password")
  - [Input Types Email Url Number](#"Input""Types""Email""Url""Number")
  - [Input Types Date Time Month Week](#"Input""Types""Date""Time""Month""Week")
  - [Input Types Radio And Checkbox](#"Input""Types""Radio""And""Checkbox")
  - [Input Types Color And Range](#"Input""Types""Color""And""Range")
  - [Input Types File Submit Reset](#"Input""Types""File""Submit""Reset")
  - [Select And Option Dropdown](#"Select""And""Option""Dropdown")
  - [Textarea Tag](#"Textarea""Tag")
  - [Button Tag](#"Button""Tag")
  - [Div And Center Tags](#"Div""And""Center""Tags")
  - [Amazon Login Form Example](#"Amazon""Login""Form""Example")
- [CSS Basics](#"CSS""Basics")
  - [Three Ways To Add CSS](#"Three""Ways""To""Add""CSS")
  - [CSS Selectors](#"CSS""Selectors")
  - [CSS Reset](#"CSS""Reset")
  - [Common CSS Properties](#"Common""CSS""Properties")
  - [Flexbox](#"Flexbox")
  - [Border Styles](#"Border""Styles")
  - [Margin](#"Margin")
  - [Padding](#"Padding")
- [Marquee Tag](#"Marquee""Tag")
  - [Marquee Tag Deprecated](#"Marquee""Tag""Deprecated")
- [CSS Animations](#"CSS""Animations")
  - [Keyframes Animation](#"Keyframes""Animation")
  - [Animation Properties](#"Animation""Properties")
- [CSS Grid Layout](#"CSS""Grid""Layout")
  - [Grid Container](#"Grid""Container")
  - [Grid Template Columns](#"Grid""Template""Columns")
  - [Grid Template Rows](#"Grid""Template""Rows")
  - [Grid Column Span](#"Grid""Column""Span")
- [Grid Layout Assignment](#"Grid""Layout""Assignment")
  - [Real Layout With Grid And Flexbox](#"Real""Layout""With""Grid""And""Flexbox")
  - [Layout Breakdown](#"Layout""Breakdown")

---

# Day 1

## HTML Basics

##### Doctype Declaration
The `<!DOCTYPE html>` declaration tells the browser which version of HTML the document is written in. It must be the very first line in any HTML document. Without it, the browser may enter "quirks mode" and render the page inconsistently across different browsers. In HTML5, the declaration is short and simple — older versions like HTML4 required longer doctypes with DTD references.

```html
<!DOCTYPE html>
```

##### Html Tag
The `<html>` tag is the root element of the entire HTML page. Everything — from the head section to the visible body content — sits inside this tag. The `lang` attribute specifies the language of the document content (e.g., `"en"` for English, `"hi"` for Hindi). This is important for accessibility tools like screen readers and for search engine optimization (SEO) so Google knows which language audience to target.

```html
<html lang="en">
  <!-- all content goes here -->
</html>
```

##### Head Tag
The `<head>` tag contains metadata — information about the document that isn't displayed on the page itself. This includes the character encoding, viewport settings for mobile responsiveness, the page title shown in the browser tab, links to external CSS files, favicon links, and meta descriptions for SEO. Think of it as the "settings panel" of your HTML page. Search engines read head content to understand and index your page properly.

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

##### Meta Tags
Meta tags provide metadata to the browser and search engines. `charset="UTF-8"` ensures all characters (including special symbols and emojis) display correctly — without it, you'll see garbled text. The `viewport` tag is critical for responsive design: it tells the browser to set the page width to the device width and set the initial zoom level to 1.0, preventing the page from appearing zoomed out on mobile devices. Other common meta tags include `description` (for SEO snippets) and `keywords`.

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

##### Title Tag
The `<title>` tag sets the text that appears in the browser tab, bookmark bar, and search engine results page (SERP). Every page must have exactly one title tag inside the head. A good title is 50-60 characters, includes primary keywords, and clearly describes the page content. This is one of the most important on-page SEO factors.

```html
<title>My Website - Learn HTML</title>
```

---

## Body And Styling

##### Body Tag
The `<body>` tag contains everything the user actually sees on the webpage — headings, paragraphs, images, links, forms, everything. The `bgcolor` attribute sets a background color (deprecated in modern HTML — prefer CSS `background-color`), and the `style` attribute applies inline CSS directly to the element. The body tag is where the visual content lives, while the head tag handles metadata.

```html
<body bgcolor="1a1a1a" style="color: white;">
  <h1>This is visible on the page</h1>
</body>
```

---

## Headings

##### H1 To H6
HTML provides six levels of headings from `<h1>` (largest, most important) to `<h6>` (smallest, least important). Headings create a document hierarchy that helps both users and search engines understand the structure of your content. `<h1>` should be used only once per page (for the main title), while `<h2>` through `<h6>` can be used multiple times for subsections. Search engines use heading hierarchy to understand content structure and rank pages — proper heading usage is a basic SEO requirement. Screen readers also use headings to help visually impaired users navigate the page.

```html
<h1>Main Title (used once per page)</h1>
<h2>Section Heading</h2>
<h3>Sub-section Heading</h3>
<h4>Minor Heading</h4>
<h5>Small Heading</h5>
<h6>Smallest Heading</h6>
```

---

## Text Tags

##### P Tag
The `<p>` tag defines a paragraph of text. Browsers automatically add spacing (margin) before and after each paragraph, creating visual separation between blocks of text. Paragraphs are the most common way to display text content. You should wrap all body text in paragraph tags rather than just using line breaks — this gives proper semantic meaning and better spacing control through CSS.

```html
<p>This is a paragraph. Browsers add space around it automatically.</p>
<p>Each paragraph starts on a new line with margins above and below.</p>
```

##### Br Tag
The `<br>` tag inserts a line break within text without starting a new paragraph. It's a self-closing (void) element — it has no closing tag. Use it when you need a line break inside a paragraph, poem, address, or any text block where you want to break to the next line without the extra spacing that `<p>` adds. Don't overuse `<br>` for spacing — that's what CSS margins and padding are for.

```html
<p>First line of text<br>Second line of text<br>Third line of text</p>
```

---

## Links

##### A Tag
The `<a>` (anchor) tag creates hyperlinks that navigate to other pages, files, or locations. The `href` attribute specifies the destination URL — it can be an external website (`https://google.com`), an internal page (`about.html`), an email (`mailto:user@example.com`), or a section on the same page (`#section-id`). The `target="_blank"` attribute opens the link in a new browser tab. The text between the opening and closing tags is what the user sees and clicks on — always make link text descriptive ("Read more about Python" is better than "Click here") for accessibility and SEO.

```html
<a href="https://www.google.com" target="_blank">Visit Google</a>
<a href="about.html">About Us</a>
<a href="mailto:contact@example.com">Email Us</a>
<a href="#section2">Jump to Section 2</a>
```

---

## Images

##### Img Tag
The `<img>` tag embeds images into the page. It's a self-closing (void) element — no closing tag needed. The `src` attribute specifies the image path (local file or URL). The `alt` attribute provides alternative text that describes the image — this is crucial for accessibility (screen readers read it aloud to visually impaired users) and SEO (search engines use it to understand image content). If the image fails to load, the alt text is displayed instead. `width` and `height` attributes set the image size in pixels — setting these prevents layout shifts while the image loads. For responsive images, use CSS instead of fixed pixel values.

```html
<img src="photo.jpg" alt="Mountain landscape at sunset" width="500" height="300">
```

---

## Lists

##### Ul Tag Unordered List
The `<ul>` tag creates an unordered (bulleted) list. Each list item is wrapped in `<li>` tags. The `type` attribute controls the bullet style: `"disc"` (filled circle, default), `"circle"` (hollow circle), and `"square"` (filled square). Unordered lists are used when the order of items doesn't matter — like navigation menus, feature lists, or sidebars. In modern HTML, CSS `list-style-type` is preferred over the `type` attribute for styling bullets.

```html
<ul type="circle">
    <li>HTML - Structure</li>
    <li>CSS - Styling</li>
    <li>JavaScript - Behavior</li>
</ul>
```

##### Ol Tag Ordered List
The `<ol>` tag creates an ordered (numbered) list. The `type` attribute changes the numbering format: `"1"` (numbers, default), `"A"` (uppercase letters), `"a"` (lowercase letters), `"I"` (uppercase Roman numerals), and `"i"` (lowercase Roman numerals). The `start` attribute sets the starting number/letter. Ordered lists are used when sequence matters — like steps in a recipe, rankings, or tutorial instructions.

```html
<ol type="A">
    <li>Learn HTML</li>
    <li>Learn CSS</li>
    <li>Learn JavaScript</li>
</ol>

<ol type="i" start="3">
    <li>Third item (starts from iii)</li>
    <li>Fourth item (iv)</li>
</ol>
```

##### Li Tag
The `<li>` (list item) tag defines individual items inside `<ul>` or `<ol>` lists. Every direct child of a list container must be an `<li>` tag — putting other elements directly inside `<ul>` or `<ol>` is invalid HTML. You can nest lists by placing a `<ul>` or `<ol>` inside an `<li>` to create sublists. Each `<li>` gets a bullet (in `<ul>`) or number (in `<ol>`) automatically.

```html
<ul>
    <li>Item 1</li>
    <li>Item 2
        <ul>
            <li>Sub-item A</li>
            <li>Sub-item B</li>
        </ul>
    </li>
</ul>
```

---

## Definition List

##### Dl Dt Dd Tags
A definition list is used to display term-definition pairs, like a glossary or FAQ section. `<dl>` wraps the entire list, `<dt>` defines the term (displayed bold by default), and `<dd>` provides the definition (displayed indented). A single `<dt>` can have multiple `<dd>` elements if a term has multiple definitions. This semantic structure is better for SEO and accessibility than using plain paragraphs when displaying glossary-style content.

```html
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language — the structure of web pages.</dd>

    <dt>CSS</dt>
    <dd>Cascading Style Sheets — the styling and layout of web pages.</dd>

    <dt>JavaScript</dt>
    <dd>A programming language that adds interactivity to web pages.</dd>
</dl>
```

---

## Semantic Tags

##### Header Tag
The `<header>` tag represents the introductory content at the top of a page or section. It typically contains the site logo, navigation, search bar, or introductory headings. Using semantic tags like `<header>` instead of generic `<div>` tags gives meaning to your content structure, which helps search engines understand page layout and improves accessibility for screen readers. Each `<section>` or `<article>` can have its own `<header>` — it's not limited to just the top of the page.

```html
<header>
    <h1>My Website</h1>
    <p>Welcome to my portfolio</p>
</header>
```

##### Nav Tag
The `<nav>` tag wraps major navigation blocks — typically the main site navigation, sidebar navigation, or table of contents. It tells screen readers and search engines "this block contains navigation links." Not all groups of links need `<nav>` — only the primary navigation blocks. Using `<nav>` improves accessibility and helps search engines understand your site structure, which can influence how your site appears in search results.

```html
<nav>
    <a href="index.html">Home</a>
    <a href="about.html">About</a>
    <a href="contact.html">Contact</a>
</nav>
```

##### Section Tag
The `<section>` tag groups related content together with a thematic purpose. It's used to divide a page into meaningful sections — like "About Us," "Services," "Contact" — each with its own heading. Sections improve document structure for both developers (easier to read and maintain code) and machines (search engines can understand and index each section separately). Don't confuse it with `<div>` — use `<section>` when the content has a heading and thematic meaning, use `<div>` for generic grouping or styling purposes.

```html
<section>
    <h2>About Us</h2>
    <p>We are a team of developers building modern web applications.</p>
</section>

<section>
    <h2>Our Services</h2>
    <p>We offer web development, mobile apps, and cloud solutions.</p>
</section>
```

---

## Media Tags

##### Audio Tag
The `<audio>` tag embeds audio players directly in the page. The `controls` attribute displays the browser's default audio player (play, pause, volume, seek bar). The `<source>` tag inside specifies the audio file path and its MIME type — you can provide multiple `<source>` tags for different formats (MP3, OGG, WAV) so the browser picks the first one it supports. The fallback text between `<audio>` tags is shown only if the browser doesn't support audio elements at all. Common audio MIME types: `audio/mpeg` (MP3), `audio/ogg` (OGG), `audio/wav` (WAV).

```html
<audio controls>
  <source src="song.mp3" type="audio/mpeg">
  <source src="song.ogg" type="audio/ogg">
  Your browser does not support the audio tag
</audio>
```

##### Video Tag
The `<video>` tag embeds video players with the same structure as audio. The `controls` attribute shows play/pause/volume/fullscreen buttons. Additional useful attributes: `autoplay` (plays automatically, but browsers block it without `muted`), `loop` (replays after ending), `muted` (starts muted), and `poster` (thumbnail image shown before playing). Common video MIME types: `video/mp4` (MP4), `video/webm` (WebM), `video/ogg` (OGG). For production websites, use YouTube embeds or dedicated video players instead of raw `<video>` tags for better performance and bandwidth handling.

```html
<video controls width="640" height="360" poster="thumbnail.jpg">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser does not support the video tag
</video>
```

---

# Day 2

## Tables

##### Table Basics
HTML tables display data in rows and columns — like spreadsheets. The `<table>` tag wraps the entire table. `<tr>` (table row) creates each horizontal row. `<th>` (table header) defines header cells — text is bold and centered by default. `<td>` (table data) defines regular data cells. The `<caption>` tag adds a title/label above the table — it's read aloud by screen readers, so always include it for accessibility. The `border` attribute adds visible borders (deprecated in modern HTML — prefer CSS borders). Tables should be used for tabular data only, not for page layout — that's what CSS Flexbox and Grid are for.

```html
<table border="1">
  <caption>Product Details</caption>
  <tr>
    <th>Product id</th>
    <th>Product name</th>
    <th>Product Price</th>
  </tr>
  <tr>
    <td>101</td>
    <td>Mobile</td>
    <td>20000</td>
  </tr>
  <tr>
    <td>102</td>
    <td>Laptop</td>
    <td>70000</td>
  </tr>
</table>
```

##### Table Sections
Tables can be divided into three semantic sections: `<thead>` (table head) groups header rows, `<tbody>` (table body) groups data rows, and `<tfoot>` (table foot) groups footer rows like totals or summaries. These sections improve code readability, allow CSS targeting of specific sections (e.g., styling the header differently), and help screen readers navigate table content. `<tfoot>` can appear before `<tbody>` in code (for calculation purposes) but renders at the bottom visually.

```html
<table border="1">
  <thead>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>101</td>
      <td>Mobile</td>
      <td>20000</td>
    </tr>
    <tr>
      <td>102</td>
      <td>Laptop</td>
      <td>70000</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td colspan="2">Total Products</td>
      <td>2</td>
    </tr>
  </tfoot>
</table>
```

##### Column Styling
The `<colgroup>` tag wraps one or more `<col>` tags to style entire columns at once without adding classes to each cell. Each `<col>` represents a column in the table — the first `<col>` targets the first column, the second targets the second column, and so on. You can apply background colors, widths, and other CSS properties to columns. The `span` attribute on `<col>` lets one `<col>` element style multiple columns. This is more efficient than adding inline styles to every `<td>`.

```html
<table border="1">
  <colgroup>
    <col style="background-color: lightblue;">
    <col style="background-color: lightgreen;">
    <col span="2" style="background-color: lightyellow;">
  </colgroup>
  <tr>
    <th>Id</th>
    <th>Name</th>
    <th>Price</th>
    <th>Quantity</th>
  </tr>
  <tr>
    <td>101</td>
    <td>Mobile</td>
    <td>20000</td>
    <td>50</td>
  </tr>
</table>
```

---

# Day 3

## Forms

##### Form Basics
The `<form>` tag is a container for collecting user input. The `method` attribute specifies how data is sent: `GET` appends data to the URL (visible, insecure, limited to ~2000 characters — use for search forms), `POST` sends data in the request body (secure, no size limit — use for login, registration, file uploads). The `action` attribute specifies the server endpoint URL where form data is sent for processing. Every input inside the form needs a `name` attribute — this is the key used when sending data to the server (e.g., `name="email"` sends `email=value`). The `required` attribute prevents form submission if the field is empty — basic client-side validation.

```html
<form method="post" action="/submit-registration">
  <label>First Name:</label>
  <input type="text" name="fname" placeholder="Enter your first name" required>

  <label>Email:</label>
  <input type="email" name="email" placeholder="Enter email" required>

  <input type="submit" value="Register">
</form>
```

##### Fieldset And Legend
The `<fieldset>` tag groups related form fields together with a visual border. The `<legend>` tag provides a caption/label for that group — it's positioned inside the border. This improves form organization and accessibility: screen readers announce the legend when the user enters the fieldset, giving context about what the grouped fields are for. Use fieldsets to logically group related inputs — like "Personal Information," "Address," "Payment Details" in a registration form.

```html
<form>
  <fieldset>
    <legend><h2>Personal Information</h2></legend>
    <label>First Name:</label>
    <input type="text" name="fname" required><br><br>

    <label>Last Name:</label>
    <input type="text" name="lname" required><br><br>

    <label>Date of Birth:</label>
    <input type="date" name="dob" required>
  </fieldset>
</form>
```

##### Label Tag
The `<label>` tag provides a text label for form inputs. It improves accessibility: when a label is clicked, the associated input gets focus (clicking the label text toggles a checkbox or selects a radio button). The `for` attribute links the label to an input's `id` — when they match, clicking the label activates that input. This is critical for mobile usability (larger tap target) and screen readers (reads the label when the input is focused). Always pair every input with a label — unlabelled forms fail accessibility checks.

```html
<label for="email">Email Address:</label>
<input type="email" id="email" name="email" required>

<label for="password">Password:</label>
<input type="password" id="password" name="password" required>
```

##### Input Types Text And Password
- `type="text"` — Single-line plain text input. The most common input type. Accepts any characters. The `placeholder` attribute shows hint text inside the field that disappears when the user starts typing.
- `type="password"` — Same as text but masks the characters (shows dots or asterisks). Prevents shoulder surfing. The actual value is sent to the server, but the display is hidden. Always use HTTPS when transmitting password fields.

```html
<input type="text" name="username" placeholder="Enter username" required>
<input type="password" name="password" placeholder="Enter password" required>
```

##### Input Types Email Url Number
- `type="email"` — Validates that the input contains a valid email format (must have `@` and domain). Shows an error on mobile if invalid. Triggers the email keyboard on phones.
- `type="url"` — Validates URL format (must start with `http://` or `https://`). Shows URL-specific keyboard on mobile.
- `type="number"` — Restricts input to numbers only. Shows a number spinner (up/down arrows). Use `min` and `max` attributes to set range limits. The `step` attribute controls increment value.

```html
<input type="email" name="email" placeholder="user@example.com" required>
<input type="url" name="website" placeholder="https://example.com" required>
<input type="number" name="age" min="1" max="120" step="1" placeholder="Enter age" required>
```

##### Input Types Date Time Month Week
- `type="date"` — Opens a date picker (calendar). Returns value in `YYYY-MM-DD` format. Use `min` and `max` to restrict date range.
- `type="time"` — Opens a time picker (hours and minutes). Returns value in `HH:MM` format (24-hour).
- `type="month"` — Opens a month/year picker. Returns value in `YYYY-MM` format.
- `type="week"` — Opens a week picker. Returns value in `YYYY-Www` format (e.g., `2026-W30`).

All four provide native browser pickers on mobile and desktop, eliminating the need for JavaScript date picker libraries for basic use cases.

```html
<input type="date" name="dob" min="2000-01-01" max="2010-12-31" required>
<input type="time" name="meeting_time" required>
<input type="month" name="joining_month" required>
<input type="week" name="joining_week" required>
```

##### Input Types Radio And Checkbox
- `type="radio`" — Single selection from a group. All radio buttons in the same group must share the same `name` attribute — this tells the browser they belong together, so only one can be selected at a time. Each option needs a unique `value` attribute. The `checked` attribute pre-selects an option.
- `type="checkbox"` — Multiple selections allowed. Each checkbox can be independently checked/unchecked. The `name` can be the same (server receives an array of checked values) or different. The `checked` attribute pre-checks the box.

```html
<!-- Radio: only one can be selected -->
<label>Gender:</label>
<input type="radio" name="gender" value="male" required> Male
<input type="radio" name="gender" value="female" required> Female
<input type="radio" name="gender" value="other" required> Other

<!-- Checkbox: multiple can be selected -->
<label>Hobbies:</label>
<input type="checkbox" name="hobbies" value="reading"> Reading
<input type="checkbox" name="hobbies" value="gaming"> Gaming
<input type="checkbox" name="hobbies" value="sports"> Sports
```

##### Input Types Color And Range
- `type="color"` — Opens a color picker widget. Returns the selected color as a hex value (e.g., `#ff5733`). Defaults to black (`#000000`). Useful for theme customization or design tools.
- `type="range"` — Creates a slider control. The `min` and `max` attributes set the range boundaries. The `value` attribute sets the initial position. The `step` attribute controls increment size (default is 1). Returns the current numeric position. Common use cases: volume sliders, brightness controls, rating systems.

```html
<input type="color" name="theme_color" value="#3498db">
<input type="range" name="volume" min="0" max="100" value="50" step="5">
```

##### Input Types File Submit Reset
- `type="file"` — Opens a file browser dialog for uploading files. The `accept` attribute restricts file types (e.g., `accept=".jpg,.png,.pdf"` or `accept="image/*"`). The `multiple` attribute allows selecting multiple files. Always use `POST` method with `enctype="multipart/form-data"` on the form for file uploads.
- `type="submit"` — Sends the form data to the server endpoint specified in `action`. The `value` attribute sets the button text.
- `type="reset"` — Clears all form fields back to their default values. Does NOT clear the form — it resets to initial state. The `value` attribute sets the button text.

```html
<input type="file" name="resume" accept=".pdf,.doc,.docx" required>
<input type="submit" value="Upload Resume">
<input type="reset" value="Clear Form">
```

##### Select And Option Dropdown
The `<select>` tag creates a dropdown list. Each `<option>` tag defines a selectable item. The `value` attribute on `<option>` specifies what gets sent to the server when that option is selected — the text between tags is what the user sees. The first option with an empty `value` acts as a placeholder/prompt. The `selected` attribute pre-selects an option. The `multiple` attribute allows selecting multiple options (hold Ctrl/Cmd to select). The `<optgroup>` tag groups options under a label for better organization.

```html
<label>Country:</label>
<select name="country" required>
    <option value="">Select your country</option>
    <option value="india">India</option>
    <option value="usa">United States</option>
    <option value="uk">United Kingdom</option>
    <option value="canada" selected>Canada</option>
</select>

<label>Subjects:</label>
<select name="subjects" multiple>
    <option value="html">HTML</option>
    <option value="css">CSS</option>
    <option value="javascript">JavaScript</option>
</select>
```

##### Textarea Tag
The `<textarea>` tag creates a multi-line text input area for longer text content like addresses, comments, descriptions, or messages. Unlike `<input type="text">`, it supports line breaks and can be resized by the user (by default). The `rows` attribute sets visible height (in lines), and `cols` sets visible width (in characters). The `placeholder` provides hint text. The content between opening and closing tags becomes the default value. Use `<textarea>` whenever you need more than a single line of text input.

```html
<textarea name="address" rows="5" cols="40" placeholder="Enter your full address..." required></textarea>

<textarea name="bio" rows="4" cols="50">Default text goes here</textarea>
```

##### Button Tag
The `<button>` tag creates a clickable button. Unlike `<input type="button">`, buttons can contain HTML content — text, images, icons, or a combination. The `type` attribute determines behavior: `type="submit"` (submits the form — default behavior), `type="reset"` (resets the form), `type="button"` (no default action — used with JavaScript event handlers). The `<button>` tag is more flexible and styled than `<input type="submit">` — it supports inner HTML for complex button designs. Always specify the `type` attribute to avoid unexpected form submissions.

```html
<button type="submit">Login</button>
<button type="reset">Clear Form</button>
<button type="button" onclick="alert('Clicked!')">Click Me</button>
<button type="submit" style="background-color: gold; padding: 10px 20px;">
    <strong>Sign Up</strong> Now!
</button>
```

##### Div And Center Tags
- `<div>` — A generic block-level container with no visual styling by itself. It groups content for styling with CSS or manipulating with JavaScript. Every element inside a `<div>` stacks vertically (block-level). Divs are the building blocks of page layout — you'll use them extensively for sections, cards, containers, headers, footers, and any grouping need. Overuse of divs without semantic meaning leads to "div soup" — prefer semantic tags like `<header>`, `<nav>`, `<section>` when possible.
- `<center>` — Deprecated tag that centers content horizontally. Modern alternative: use CSS `text-align: center` or `margin: 0 auto` for block elements or Flexbox/Grid for layout centering.

```html
<!-- Generic container for layout -->
<div style="width: 500px; margin: 0 auto; padding: 20px;">
    <h2>Centered Container</h2>
    <p>This div is centered using CSS margin auto.</p>
</div>

<!-- Using Flexbox for centering (modern approach) -->
<div style="display: flex; justify-content: center; align-items: center; height: 200px;">
    <p>Centered both horizontally and vertically</p>
</div>
```

##### Amazon Login Form Example
A realistic styled login form demonstrating form elements, inline CSS, and layout. This example combines multiple concepts: `<form>` with method and action, `<label>` for accessibility, different `<input>` types, `<button>` for submission, `<div>` for layout, `<center>` for alignment, and inline `style` attributes for quick styling. The form uses `margin: auto` to center itself, `background-color` for visual distinction, `padding` for internal spacing, and `border-radius` for rounded corners.

```html
<div>
  <center>
    <img src="Amazon-logo.png" alt="Amazon Logo" style="width: 100px;">
  </center>
  <form method="post" action="/login" style="background-color: #f3f3f3; padding: 20px; border-radius: 5px; width: 300px; margin: auto;">
    <h1>Login</h1>

    <label for="email">Email or phone number</label><br>
    <input type="text" id="email" name="email" placeholder="Enter your email" required><br><br>

    <label for="password">Password</label><br>
    <input type="password" id="password" name="password" placeholder="Enter password" required><br><br>

    <button type="submit" style="width: 100%; background-color: #f0c14b; border: none; padding: 10px; border-radius: 5px; cursor: pointer;">
        Login
    </button><br><br>

    <input type="checkbox" name="remember" id="remember">
    <label for="remember">Keep me signed in</label><br><br>

    <hr>
    <p>New to Amazon?</p>
    <button type="submit" style="width: 100%; padding: 10px; border-radius: 5px; cursor: pointer;">
        Create your Amazon account
    </button>
  </form>
</div>
```

---

> **Remember:** HTML is about structure and semantics, not visual styling. Forms need `name` attributes on every input to send data. Always pair inputs with `<label>` tags for accessibility. Use `required` for basic client-side validation. Semantic tags (`header`, `nav`, `section`, `article`) improve SEO, accessibility, and code maintainability.

---

# Day 4
![[Pasted image 20260805175404.png]]
## CSS Basics

CSS (Cascading Style Sheets) controls how HTML elements look — colors, fonts, spacing, layout, animations, and more. "Cascading" means styles follow a priority order: inline styles override internal styles, internal styles override external styles, and more specific selectors override general ones. CSS separates presentation from structure, meaning you can change the entire look of a website by modifying one `.css` file without touching any HTML. This is the foundation of modern web design — HTML provides structure, CSS provides style.

---

## Three Ways To Add CSS

##### Inline CSS
Apply styles directly on an element using the `style` attribute. Quick for testing or one-off styles, but bad for maintainability — you can't reuse styles and mixing structure with presentation makes code hard to read. Inline styles have the highest specificity (override all other CSS except `!important`), so they're hard to override later. Avoid in production — use classes instead.

```html
<h1 style="color: blue; font-size: 24px; text-align: center;">Inline Styled Heading</h1>
<p style="background-color: yellow; padding: 10px;">Yellow background paragraph</p>
```

##### Internal CSS
Use the `<style>` tag inside the `<head>` section. Good for single-page styles or page-specific overrides. Styles apply to all matching elements on that page only. Better than inline for maintainability since styles are centralized, but still not ideal for multi-page websites where you'd need to duplicate styles across pages.

```html
<head>
  <style>
    h1 { color: blue; }
    p { background-color: lightgray; padding: 10px; }
    .highlight { color: red; font-weight: bold; }
  </style>
</head>
<body>
  <h1>This heading is blue</h1>
  <p>This paragraph has a light gray background</p>
</body>
```

##### External CSS
Link a separate `.css` file using the `<link>` tag. The best and most common method for real projects. One CSS file can style multiple HTML pages — change the stylesheet once, and every page updates. Browser caching improves performance (CSS file loads once, then from cache). Keeps HTML clean and focused on structure. The `rel="stylesheet"` attribute tells the browser this is a stylesheet. The `href` attribute points to the CSS file path.

```html
<head>
  <link rel="stylesheet" href="styles.css">
</head>
```

**Interview point:** External CSS enables separation of concerns (HTML = structure, CSS = style), improves caching, reduces page load time, and makes team collaboration easier (designer works on CSS, developer works on HTML).

---

## CSS Selectors

Selectors tell the browser which HTML elements to style. There are 5 main types:

##### Element Selector
Targets all elements of that type. If you write `p { }`, it styles every `<p>` tag on the page. Useful for setting base styles for specific element types. Least specific selector — can be overridden by class, ID, or inline styles.

```css
p { color: blue; font-size: 16px; }
h1 { color: navy; }
```

##### ID Selector
Targets one unique element using `#`. IDs must be unique within a page — each ID can only be used once. Highest specificity among regular selectors (overridden only by inline styles and `!important`). Use IDs for unique elements like the main header, navigation bar, or footer. In JavaScript, `document.getElementById()` uses IDs for direct element access.

```css
#main-header { background-color: #333; color: white; padding: 20px; }
#login-form { max-width: 400px; margin: 0 auto; }
```

##### Class Selector
Targets all elements with that class using `.`. Classes can be reused on multiple elements — this is the most commonly used selector. One element can have multiple classes (e.g., `class="btn btn-primary"`). Use classes for reusable styles like button styles, card layouts, or text formatting. Classes are the backbone of CSS architecture and component-based design (used heavily in frameworks like Bootstrap and Tailwind).

```css
.card { background: white; padding: 20px; border-radius: 8px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); }
.btn-primary { background-color: blue; color: white; padding: 10px 20px; border: none; }
.text-center { text-align: center; }
```

##### Group Selector
Targets multiple elements at once using commas. Saves code by applying the same styles to different selectors without repeating the declaration block. You can mix element, class, and ID selectors in a group. Great for resetting styles across multiple elements or applying shared base styles.

```css
h1, h2, h3 { color: #333; font-family: Arial, sans-serif; }
.btn, .link, #submit { cursor: pointer; transition: all 0.3s ease; }
```

##### Universal Selector
Targets every element on the page using `*`. Primarily used for CSS reset — removing default browser margins, padding, and box-sizing inconsistencies. Applied rarely for actual styling (styling everything the same is usually not what you want). The `box-sizing: border-box` reset is extremely common — it makes width/height include padding and border, which is more intuitive for layout calculations.

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

**Interview point:** Specificity order: Universal (*) < Element < Class < ID < Inline. Higher specificity overrides lower. `!important` overrides everything (avoid using it — specificity should handle conflicts).

---

## CSS Reset

Browsers apply default margins and padding to elements (e.g., `<body>` has 8px margin, `<p>` has 16px margin). These defaults vary across browsers, causing inconsistent rendering. A CSS reset removes all default styles so you start from a clean slate. The universal selector reset (`* { margin: 0; padding: 0; }`) is the most basic reset. Professional projects use more comprehensive resets like Normalize.css or a custom reset that also addresses font sizes, line heights, and box-sizing.

```css
/* Basic reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* More thorough reset */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  font-size: 16px;
}
```

**Interview point:** `box-sizing: border-box` means width = content + padding + border (not just content). This makes layout calculations much simpler — when you set `width: 200px`, the element is exactly 200px including its padding and border.

---

## Common CSS Properties

##### Background And Text
- `background-color` — Sets the background color (hex, rgb, hsl, or named color)
- `color` — Sets the text color
- `text-align` — Aligns text horizontally: `left`, `center`, `right`, `justify`
- `font-family` — Sets the font type
- `font-size` — Sets text size (px, em, rem, %)
- `font-weight` — Sets boldness: `normal`, `bold`, `100`-`900`
- `line-height` — Sets spacing between lines of text

```css
body {
  background-color: #f5f5f5;
  color: #333333;
  font-family: 'Arial', sans-serif;
  font-size: 16px;
  line-height: 1.6;
}

h1 {
  text-align: center;
  font-weight: bold;
  color: #2c3e50;
}
```

##### Sizing
- `width` / `height` — Sets element dimensions. Values: `px`, `%`, `em`, `rem`, `vw`, `vh`, `auto`
- `min-width` / `max-width` — Sets minimum/maximum dimensions
- `min-height` / `max-height` — Prevents elements from growing/shrinking beyond limits

```css
.container {
  width: 80%;          /* 80% of parent width */
  max-width: 1200px;   /* never wider than 1200px */
  min-height: 100vh;   /* full viewport height */
  height: auto;        /* height adjusts to content */
}
```

##### Display
The `display` property controls how an element behaves in the layout:
- `none` — Removes element from layout entirely (like it doesn't exist)
- `block` — Full-width, stacks vertically (default for div, p, h1-h6)
- `inline` — Only takes up needed width, flows with text (default for span, a)
- `inline-block` — Inline flow but accepts width/height
- `flex` — Enables Flexbox layout (one-dimensional)
- `grid` — Enables Grid layout (two-dimensional)

```css
.hidden { display: none; }
.card { display: block; width: 300px; }
.badge { display: inline-block; padding: 5px 10px; }
.container { display: flex; }
.grid-layout { display: grid; }
```

---

## Flexbox

Flexbox is a one-dimensional layout system that arranges items in a row or column. It solves the age-old problems of centering elements, equal-height columns, and responsive spacing without floats or positioning hacks. The parent container becomes a "flex container" with `display: flex`, and its direct children become "flex items" that can be aligned, distributed, and ordered regardless of their HTML order.

```css
.container {
  display: flex;                    /* enables flexbox */
  flex-direction: row;              /* main axis: row | column | row-reverse | column-reverse */
  justify-content: space-evenly;    /* main axis alignment */
  align-items: center;              /* cross axis alignment */
  flex-wrap: wrap;                  /* allows items to wrap to next line */
  gap: 20px;                        /* space between items */
}
```

| Property | What It Does | Common Values |
|----------|-------------|---------------|
| `flex-direction` | Sets main axis direction | `row`, `column`, `row-reverse`, `column-reverse` |
| `justify-content` | Aligns items on main axis | `flex-start`, `center`, `space-between`, `space-around`, `space-evenly` |
| `align-items` | Aligns items on cross axis | `flex-start`, `center`, `stretch`, `baseline`, `flex-end` |
| `flex-wrap` | Whether items wrap | `nowrap` (default), `wrap`, `wrap-reverse` |
| `gap` | Space between items | `10px`, `20px`, `1rem` |

**Interview point:** Flexbox handles one axis at a time (row OR column). For two-dimensional layouts (rows AND columns simultaneously), use CSS Grid. Flexbox is for component-level layout; Grid is for page-level layout.

---

## Border Styles

Borders outline elements with different visual styles. The `border` shorthand sets width, style, and color in one line. Border styles include:

| Style | Description |
|-------|-------------|
| `solid` | Continuous line (most common) |
| `dotted` | Dots |
| `dashed` | Dashes |
| `double` | Two parallel solid lines |
| `groove` | 3D grooved effect (depends on background) |
| `ridge` | 3D ridged effect (opposite of groove) |
| `inset` | 3D inset effect |
| `outset` | 3D outset effect (opposite of inset) |
| `none` | No border |

```css
.card { border: 2px solid #333; }
.error { border: 2px dotted red; }
.fancy { border: 3px double gold; }
.groove { border: 4px groove #ccc; }

/* Individual border properties */
.button {
  border-width: 2px;
  border-style: solid;
  border-color: #007bff;
  border-radius: 8px;    /* rounds the corners */
}
```

**Interview point:** `border-radius` creates rounded corners. Use `border-radius: 50%` on a square element to make a circle. `border: none` removes borders entirely. Borders add to the element's total width unless `box-sizing: border-box` is set.

---

## Margin

Margin is the space **outside** an element's border. It pushes other elements away, creating space between the element and its neighbors. Margin can be negative (pulls elements closer). Margin collapse: when two vertical margins touch, the larger one wins (they don't add up). This only happens vertically, not horizontally.

```css
/* All sides */
.box { margin: 20px; }

/* Vertical | Horizontal */
.box { margin: 10px 20px; }

/* Top | Right | Bottom | Left (clockwise) */
.box { margin: 10px 20px 30px 40px; }

/* Center horizontally (block element) */
.container { margin: 0 auto; }

/* Negative margin (pulls element closer) */
.shifted { margin-top: -10px; }

/* rem unit (relative to root font size) */
.large-gap { margin: 2rem; }
```

| Shortcut | Meaning |
|----------|---------|
| `margin: 10px` | All four sides: 10px |
| `margin: 10px 20px` | Top/Bottom: 10px, Left/Right: 20px |
| `margin: 10px 20px 30px` | Top: 10px, Left/Right: 20px, Bottom: 30px |
| `margin: 10px 20px 30px 40px` | Top: 10px, Right: 20px, Bottom: 30px, Left: 40px |

**Interview point:** `margin: 0 auto` centers a block element horizontally within its parent. This only works when the element has a defined width (not `width: auto`). Margin collapse doesn't happen with flex/grid containers.

---

## Padding

Padding is the space **inside** an element's border, between the border and the content. It creates breathing room around text, images, or any content. Unlike margin, padding never collapses and always adds to the element's total visible size (unless `box-sizing: border-box` is used, where it's included in the width/height).

```css
/* All sides */
.card { padding: 20px; }

/* Vertical | Horizontal */
.button { padding: 10px 20px; }

/* Top | Right | Bottom | Left (clockwise) */
.asymmetric { padding: 5px 10px 15px 20px; }

/* Only specific sides */
.no-top-padding { padding-top: 0; }
.only-horizontal { padding-left: 20px; padding-right: 20px; }
```

| Shortcut | Meaning |
|----------|---------|
| `padding: 20px` | All four sides: 20px |
| `padding: 10px 20px` | Top/Bottom: 10px, Left/Right: 20px |
| `padding: 10px 20px 30px` | Top: 10px, Left/Right: 20px, Bottom: 30px |
| `padding: 10px 20px 30px 40px` | Top: 10px, Right: 20px, Bottom: 30px, Left: 40px |

**Interview point:** Margin = outside (space between elements), Padding = inside (space between border and content). With `box-sizing: border-box`, padding is included in the element's width/height, so setting `width: 200px; padding: 20px;` keeps the element at 200px total. Without `border-box`, the element becomes 240px.

---

> **Remember:** Always start with CSS reset. Use external CSS for real projects. Flexbox is the modern way to layout elements — it handles 90% of layout needs. Margin collapses vertically; padding never collapses. `box-sizing: border-box` should be on every project. Classes (`.`) are reusable, IDs (`#`) are unique. Specificity determines which styles win when conflicts exist.

---

# Day 5

## Marquee Tag

##### Marquee Tag (Deprecated)
The `<marquee>` tag creates scrolling or blinking text on the page. It's **deprecated** (removed from HTML5 spec) and should not be used in production websites, but it's still taught for understanding legacy code. The `behavior` attribute controls how text moves: `"scroll"` (continuous loop), `"slide"` (stops at edge), `"alternate"` (bounces back and forth). The `direction` attribute sets the direction: `"left"`, `"right"`, `"up"`, `"down"`. The `scrollamount` attribute controls speed (higher = faster). Modern alternatives: CSS `@keyframes` animations or JavaScript-based marquee libraries.

```html
<!-- Basic scrolling text -->
<marquee behavior="scroll" direction="left" scrollamount="10" style="color: red; font-size: 30px;">
  This text scrolls left
</marquee>

<!-- Scrolling down -->
<marquee behavior="scroll" direction="down" scrollamount="5" style="color: blue;">
  This text scrolls down
</marquee>

<!-- Bouncing text -->
<marquee behavior="alternate" direction="left" style="color: green;">
  This text bounces left and right
</marquee>
```

**Interview point:** Never use `<marquee>` in production. It's deprecated, hurts accessibility (screen readers can't parse scrolling text properly), affects performance, and annoys users. If asked about it in an interview, mention CSS animations as the modern replacement.

---

## CSS Animations

##### Keyframes Animation
CSS `@keyframes` define reusable animation sequences. You create a named animation with keyframe stops (0% to 100%), then apply it to elements using the `animation` property. This replaces the deprecated `<marquee>` for creating motion effects. The `animation` shorthand includes: `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`. The example below creates a blink effect by toggling opacity between 1 (visible) and 0 (invisible).

```html
<style>
  .blink {
    animation: blink 1s infinite;
  }

  @keyframes blink {
    0%   { opacity: 1; }    /* fully visible */
    50%  { opacity: 0; }    /* fully invisible */
    100% { opacity: 1; }    /* fully visible again */
  }
</style>

<marquee class="blink"><h1>Blinking Text</h1></marquee>
```

##### Animation Properties
The `animation` shorthand property combines multiple animation settings into one line:

| Property | What It Does | Example |
|----------|-------------|---------|
| `animation-name` | Name of the @keyframes | `blink` |
| `animation-duration` | How long one cycle takes | `1s`, `500ms` |
| `animation-timing-function` | Speed curve | `ease`, `linear`, `ease-in` |
| `animation-delay` | Wait before starting | `0.5s` |
| `animation-iteration-count` | How many times to repeat | `1`, `3`, `infinite` |
| `animation-direction` | Direction of playback | `normal`, `reverse`, `alternate` |

```css
.fade-in {
  animation: fadeIn 2s ease-in-out infinite alternate;
}

@keyframes fadeIn {
  0%   { opacity: 0; transform: translateY(20px); }
  100% { opacity: 1; transform: translateY(0); }
}
```

**Interview point:** CSS animations are more performant than JavaScript animations because they run on the browser's compositor thread (GPU-accelerated). Use `transform` and `opacity` for smooth animations — animating `width`, `height`, or `top` triggers layout reflows and causes jank.

---

## CSS Grid Layout

##### Grid Container
CSS Grid is a two-dimensional layout system that handles both rows and columns simultaneously. Set `display: grid` on a parent container to enable grid layout on its direct children (grid items). The `grid-template-columns` property defines how many columns and their widths. The `repeat()` function repeats column/row patterns. The `fr` unit (fraction) distributes available space proportionally — `1fr 1fr` creates two equal columns. The `gap` property adds space between grid items without affecting outer margins.

```html
<style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);  /* 2 equal columns */
    gap: 10px;                               /* space between items */
  }

  .g-col-4 {
    background-color: #f2f2f2;
    padding: 20px;
    text-align: center;
  }
</style>

<div class="grid-container">
  <div class="g-col-4">Item 1</div>
  <div class="g-col-4">Item 2</div>
  <div class="g-col-4">Item 3</div>
  <div class="g-col-4">Item 4</div>
</div>
```

##### Grid Template Columns
Define column structure with `grid-template-columns`. The `fr` unit distributes available space proportionally. You can mix units for different column sizes.

```css
/* 3 equal columns */
grid-template-columns: repeat(3, 1fr);

/* Fixed + flexible columns */
grid-template-columns: 200px 1fr 1fr;   /* sidebar + 2 content areas */

/* Mixed sizes */
grid-template-columns: 1fr 2fr 1fr;     /* narrow-wide-narrow */

/* Auto-fit for responsive */
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
```

##### Grid Template Rows
Define row heights with `grid-template-rows`. Works the same way as columns but for vertical sizing.

```css
.container {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: 70px 180px 80px 70px;  /* header, main, extra, footer */
  gap: 5px;
}
```

##### Grid Column Span
Use `grid-column` to make an item span multiple columns. `1 / 3` means "start at column line 1, end at column line 3" (spans 2 columns in a 2-column grid).

```css
.header {
  grid-column: 1 / 3;    /* spans full width */
}

.footer {
  grid-column: 1 / 3;    /* spans full width */
}

.sidebar {
  grid-row: 2 / 4;       /* spans rows 2 and 3 */
}
```

**Interview point:** Grid is two-dimensional (rows AND columns), Flexbox is one-dimensional (row OR column). Use Grid for page-level layouts (header/sidebar/content/footer), Flexbox for component-level alignment (nav items, card content, buttons). Grid + Flexbox together = complete layout solution.

---

## Grid Layout Assignment

##### Real Layout with Grid and Flexbox
A practical example combining CSS Grid for page structure and Flexbox for centering content inside grid items. The layout has a header spanning full width, a sidebar on the left, main content area, extra content area, and a footer spanning full width. This is the classic "holy grail layout" pattern used in dashboards, admin panels, and content websites.

```html
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: Arial, sans-serif;
    background: #f4f4f4;
  }

  .container {
    display: grid;
    grid-template-columns: 1fr 3fr;           /* sidebar | main content */
    grid-template-rows: 70px 180px 80px 70px; /* header, main, extra, footer */
    gap: 5px;
    width: 90%;
    margin: 20px auto;                        /* center on page */
  }

  .header {
    grid-column: 1 / 3;                       /* full width */
    background: skyblue;
  }

  .sidebar {
    grid-row: 2 / 4;                          /* spans main + extra rows */
    background: yellowgreen;
  }

  .main {
    background: gold;
  }

  .extra {
    background: gray;
  }

  .footer {
    grid-column: 1 / 3;                       /* full width */
    background: orange;
  }

  .box {
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }
</style>

<div class="container">
  <div class="header box">Header</div>
  <div class="sidebar box">Sidebar</div>
  <div class="main box">Main Content</div>
  <div class="extra box">Extra Content</div>
  <div class="footer box">Footer</div>
</div>
```

##### Layout Breakdown
| Element | Grid Position | Spans |
|---------|--------------|-------|
| Header | `grid-column: 1 / 3` | Full width (2 columns) |
| Sidebar | `grid-row: 2 / 4` | 2 rows tall |
| Main | Default position | 1 column, 1 row |
| Extra | Default position | 1 column, 1 row |
| Footer | `grid-column: 1 / 3` | Full width (2 columns) |

The `.box` class uses Flexbox to center text inside each grid item — this demonstrates Grid + Flexbox working together: Grid handles the page layout, Flexbox handles the content alignment within each cell.

**Interview point:** This layout pattern is the foundation of most website designs. The header and footer span full width, sidebar stays fixed on the left, main content takes up the remaining space. In real projects, you'd replace fixed pixel heights with `minmax()` or `auto` for responsive behavior, and use `@media` queries to stack the sidebar on mobile.

---

> **Remember:** `<marquee>` is deprecated — use CSS `@keyframes` animations instead. CSS Grid is two-dimensional (rows + columns), Flexbox is one-dimensional (row OR column). Use `fr` unit for proportional column widths. `grid-column: 1 / 3` makes an item span the full width of a 2-column grid. Always combine Grid for layout and Flexbox for content alignment for clean, maintainable code.

