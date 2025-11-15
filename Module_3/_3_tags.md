
---

## **1️⃣ HTML Elements**

HTML elements are the building blocks of a webpage. An element usually has a **start tag, content, and end tag**:

```html
<tagname>content</tagname>
```

---

### **a) Paragraphs `<p>`**

* Used for text content.
* **Example:**

```html
<p>This is a paragraph.</p>
<p>HTML makes web pages easy!</p>
```

---

### **b) Headings `<h1>` to `<h6>`**

* Used for titles and headings. `<h1>` = biggest, `<h6>` = smallest.
* **Example:**

```html
<h1>Main Title</h1>
<h2>Subheading</h2>
<h3>Smaller Heading</h3>
```

---

### **c) Lists**

**1. Ordered list `<ol>`** – numbers items

```html
<ol>
  <li>First item</li>
  <li>Second item</li>
</ol>
```

**2. Unordered list `<ul>`** – bullets

```html
<ul>
  <li>Apple</li>
  <li>Banana</li>
</ul>
```

---

### **d) Div `<div>` and Span `<span>`**

* **`<div>`** → block-level container (used to group elements)
* **`<span>`** → inline container (used to style part of text)

**Example:**

```html
<div style="background-color: lightgray; padding: 10px;">
  <p>This paragraph is inside a div.</p>
  <span style="color: red;">This text is red.</span>
</div>
```

---

## **2️⃣ Semantic Tags**

Semantic tags describe **the meaning of content** for humans and browsers.

**Common semantic tags:**

* `<header>` → top section (logo, menu)
* `<footer>` → bottom section (copyright, contact)
* `<article>` → independent content (blog post, news)
* `<section>` → group of related content

**Example:**

```html
<header>
  <h1>My Website</h1>
</header>

<section>
  <h2>About Us</h2>
  <p>We create websites.</p>
</section>

<article>
  <h2>Blog Post</h2>
  <p>HTML is fun!</p>
</article>

<footer>
  <p>© 2025 My Website</p>
</footer>
```

---

## **3️⃣ Linking in HTML**

### **a) Anchor tag `<a>`**

* Used to create links.

```html
<a href="https://www.google.com">Go to Google</a>
```

---

### **b) Internal vs External links**

* **Internal link** → links to another page on the **same website**

```html
<a href="about.html">About Us</a>
```

* **External link** → links to a **different website**

```html
<a href="https://www.wikipedia.org">Wikipedia</a>
```

---

### **c) Relative vs Absolute URLs**

* **Relative URL** → path relative to current page

```html
<a href="contact.html">Contact</a>
```

* **Absolute URL** → full website address

```html
<a href="https://www.example.com/contact.html">Contact</a>
```

---

## **4️⃣ Anchor Attributes**

* **`href`** → link URL
* **`target`** → where to open link (`_blank` = new tab)
* **`name`** → link anchor inside a page
* **`title`** → tooltip text

**Example:**

```html
<a href="https://www.google.com" target="_blank" title="Go to Google">Google</a>
```

---

## **5️⃣ Image Maps**

* **Concept:** Make certain areas of an image clickable.
* **Tags:** `<map>` defines the map, `<area>` defines clickable areas.

**Example:**

```html
<img src="worldmap.jpg" usemap="#worldmap" alt="World Map">

<map name="worldmap">
  <area shape="rect" coords="0,0,100,100" href="https://www.usa.gov" alt="USA">
  <area shape="circle" coords="150,150,50" href="https://www.india.gov.in" alt="India">
</map>
```

**Explanation:**

* `shape` → rectangle, circle, polygon
* `coords` → coordinates of clickable area
* `href` → link to open

---

✅ **Tip to remember:**

* **Elements = building blocks**
* **Semantic = meaningful blocks**
* **Anchor `<a>` = links**
* **Image maps = clickable parts of an image**

---
💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛💛