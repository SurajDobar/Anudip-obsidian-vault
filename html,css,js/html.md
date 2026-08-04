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

---

# Day 1

## HTML Basics

##### Doctype Declaration
Tells the browser this is an HTML5 document. Always put it at the top.

```html
<!DOCTYPE html>
```

##### Html Tag
Root element that wraps all HTML content. `lang` attribute sets the language.

```html
<html lang="en">
  <!-- all content goes here -->
</html>
```

##### Head Tag
Contains meta info, title, and links. Not visible on the page.

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
```

##### Meta Tags
- `charset="UTF-8"` → character encoding
- `viewport` → makes site responsive on mobile

##### Title Tag
Sets the browser tab title.

```html
<title>My Page</title>
```

---

## Body And Styling

##### Body Tag
Contains all visible content. `bgcolor` sets background color, `style` adds inline CSS.

```html
<body bgcolor="1a1a1a" style="color: white;">
  <!-- visible content -->
</body>
```

---

## Headings

##### H1 To H6
Six levels of headings. `h1` is the largest, `h6` is the smallest.

```html
<h1>Hello World 1</h1>
<h2>Hello World 2</h2>
<h3>Hello World 3</h3>
<h4>Hello World 4</h4>
<h5>Hello World 5</h5>
<h6>Hello World 6</h6>
```

---

## Text Tags

##### P Tag
Defines a paragraph. Browsers add space around it.

```html
<p>This is a paragraph of text.</p>
```

##### Br Tag
Inserts a line break. Self-closing tag (no closing tag needed).

```html
Line one<br>Line two
```

---

## Links

##### A Tag
Creates a hyperlink. `href` sets the URL, `target="_blank"` opens in new tab.

```html
<a href="https://www.google.com" target="_blank">google</a>
```

---

## Images

##### Img Tag
Embeds an image. Self-closing tag.
- `src` → image URL
- `alt` → alternative text if image fails
- `width` / `height` → size in pixels

```html
<img src="photo.jpg" alt="scenery" width="500px" height="300px">
```

---

## Lists

##### Ul Tag Unordered List
Bullet-point list. `type` attribute changes bullet style:
- `circle` → hollow bullets
- `square` → square bullets

```html
<ul type="circle">
    <li>List item 1</li>
    <li>List item 2</li>
</ul>
```

##### Ol Tag Ordered List
Numbered list. `type` attribute changes numbering style:
- `1` → numbers (default)
- `A` → uppercase letters
- `a` → lowercase letters
- `I` → uppercase roman
- `i` → lowercase roman

```html
<ol type="A">
    <li>List item 1</li>
    <li>List item 2</li>
</ol>
```

##### Li Tag
List item used inside `ul` or `ol`.

```html
<li>Item text here</li>
```

---

## Definition List

##### Dl Dt Dd Tags
- `dl` → definition list wrapper
- `dt` → term (bold by default)
- `dd` → definition (indented)

```html
<dl>
    <dt>Term 1</dt>
    <dd>Definition 1</dd>
    <dt>Term 2</dt>
    <dd>Definition 2</dd>
</dl>
```

---

## Semantic Tags

##### Header Tag
Defines the top section of a page (intro, logo, nav).

```html
<header>
    <h1>This is a header</h1>
</header>
```

##### Nav Tag
Contains navigation links.

```html
<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
</nav>
```

##### Section Tag
Groups related content together.

```html
<section>
    <h1>Section 1</h1>
    <p>Content goes here.</p>
</section>
```

---

## Media Tags

##### Audio Tag
Embeds audio with playback controls. `source` specifies file and type.

```html
<audio controls>
  <source src="swin.mp3" type="audio/mpeg">
  Your browser does not support the audio tag
</audio>
```

##### Video Tag
Embeds video with playback controls. Same structure as audio.

```html
<video controls>
    <source src="flwo.mp4" type="video/mp4">
    Your browser does not support the video tag
</video>
```

---

# Day 2

## Tables

##### Table Basics
`<table>` creates a table. `<caption>` adds a title. `<tr>` defines rows, `<th>` header cells, `<td>` data cells.

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
</table>
```

##### Table Sections
`<thead>` groups header rows, `<tbody>` groups body rows, `<tfoot>` groups footer rows.

```html
<table border="1">
  <thead>
    <tr><th>Id</th><th>Name</th></tr>
  </thead>
  <tbody>
    <tr><td>101</td><td>Mobile</td></tr>
  </tbody>
  <tfoot>
    <tr><td>107</td><td>washing machine</td></tr>
  </tfoot>
</table>
```

##### Column Styling
`<colgroup>` wraps `<col>` elements to style entire columns at once.

```html
<colgroup>
  <col style="background-color: antiquewhite;">
  <col style="background-color: antiquewhite;">
</colgroup>
```

---

# Day 3

## Forms

##### Form Basics
`<form>` wraps form elements. `method` sets HTTP method (get/post), `action` sets where data is sent.

```html
<form method="post" action="submit.php">
  <label>First Name:</label>
  <input type="text" name="fname" placeholder="Enter name" required>
  <input type="submit" value="Submit">
</form>
```

##### Fieldset And Legend
`<fieldset>` groups form elements. `<legend>` adds a caption to the group.

```html
<fieldset>
  <legend><h1>Registration Form</h1></legend>
  <!-- form fields here -->
</fieldset>
```

##### Label Tag
`<label>` ties text to an input. `for` attribute links to input's `id`.

```html
<label for="email">Email:</label>
<input type="email" id="email" name="email">
```

##### Input Types Text And Password
- `type="text"` → single-line text
- `type="password"` → hidden characters

```html
<input type="text" name="fname" placeholder="Enter first name" required>
<input type="password" name="password" placeholder="Enter password" required>
```

##### Input Types Email Url Number
- `type="email"` → validates email format
- `type="url"` → validates URL format
- `type="number"` → only numbers

```html
<input type="email" name="email" placeholder="Enter email" required>
<input type="url" name="github" placeholder="Enter github link" required>
<input type="number" name="age" placeholder="Enter age" required>
```

##### Input Types Date Time Month Week
- `type="date"` → date picker
- `type="time"` → time picker
- `type="month"` → month picker
- `type="week"` → week picker

```html
<input type="date" name="dob" required>
<input type="time" name="time" required>
<input type="month" name="joining_month" required>
<input type="week" name="joining_week" required>
```

##### Input Types Radio And Checkbox
- `type="radio"` → single selection (same `name` groups them)
- `type="checkbox"` → multiple selections

```html
<input type="radio" name="gender" value="male" required> Male
<input type="radio" name="gender" value="female" required> Female

<input type="checkbox" name="hobbies" value="reading"> Reading
<input type="checkbox" name="hobbies" value="sports"> Sports
```

##### Input Types Color And Range
- `type="color"` → color picker
- `type="range"` → slider with min/max

```html
<input type="color" name="color" required>
<input type="range" name="skill" min="1" max="10" required>
```

##### Input Types File Submit Reset
- `type="file"` → file upload
- `type="submit"` → sends form data
- `type="reset"` → clears all form fields

```html
<input type="file" name="file" required>
<input type="submit" value="Submit">
<input type="reset" value="Reset">
```

##### Select And Option Dropdown
`<select>` creates a dropdown. `<option>` defines each choice.

```html
<select name="country" required>
    <option value="">Select your country</option>
    <option value="india">India</option>
    <option value="uk">UK</option>
    <option value="canada">Canada</option>
</select>
```

##### Textarea Tag
`<textarea>` for multi-line text input (address, comments, etc).

```html
<textarea name="address" placeholder="Enter your address" required></textarea>
```

##### Button Tag
`<button>` creates a clickable button. `type` can be submit, reset, or button.

```html
<button type="submit">Login</button>
<button type="submit">Create your Amazon account</button>
```

##### Div And Center Tags
- `<div>` → container for grouping content
- `<center>` → centers content horizontally

```html
<div>
  <center>
    <img src="logo.png" alt="Logo" style="width: 100px;">
  </center>
</div>
```

##### Amazon Login Form Example
A styled login form with image, inputs, button, and checkbox.

```html
<div>
  <center>
    <img src="Amazon-logo.png" alt="Amazon Logo" style="width: 100px;">
  </center>
  <form method="post" action="submit" style="background-color: #f3f3f3; padding: 20px; border-radius: 5px; width: 300px; margin: auto;">
    <h1>Login</h1>
    <label>Email or phone number</label><br>
    <input type="text" name="email" placeholder="Enter your email" required><br><br>
    <label>Password</label><br>
    <input type="password" name="password" placeholder="Enter password" required><br><br>
    <button style="width:100%; background-color: #f0c14b; border: none; padding: 10px;" type="submit">Login</button><br><br>
    <input type="checkbox" name="remember" id="remember">
    <label for="remember">Keep me signed in</label>
  </form>
</div>
```

---

> **Remember:** HTML is about structure, not style. Forms need `name` attribute on inputs to send data. Always use `label` for accessibility. Use `required` to prevent empty submissions.
