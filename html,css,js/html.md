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

> **Remember:** HTML is about structure, not style. Use semantic tags (`header`, `nav`, `section`) for better readability and SEO.
