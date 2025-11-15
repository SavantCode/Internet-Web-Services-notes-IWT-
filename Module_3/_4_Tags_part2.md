
---

## **1️⃣ Meta Information**

The `<meta>` tag provides **information about the HTML page** to browsers and search engines. It goes inside the `<head>` section.

**Common uses:**

1. **Character encoding**

```html
<meta charset="UTF-8">
```

* Tells the browser which characters to display (UTF-8 = standard).

2. **Viewport (for mobile devices)**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

* Makes the page **responsive** on phones and tablets.

3. **Keywords**

```html
<meta name="keywords" content="HTML, CSS, Web Development">
```

* Helps search engines understand page content.

4. **Description**

```html
<meta name="description" content="Learn HTML basics easily.">
```

* Short page description for search engines.

---

## **2️⃣ Image Preliminaries**

The `<img>` tag is used to **add images** to a page.

**Basic structure:**

```html
<img src="image.jpg" alt="Description" height="200" width="300">
```

**Attributes:**

* `src` → path to image
* `alt` → text if image doesn’t load
* `height` / `width` → image size

**Example:**

```html
<img src="flower.jpg" alt="Red Flower" height="150" width="200">
```

---

## **3️⃣ Layouts**

### **a) Using `<div>` and `<span>`**

* `<div>` → block-level container for grouping elements (like sections)
* `<span>` → inline container for styling small parts of text

**Example:**

```html
<div style="background-color: lightblue; padding: 10px;">
  <p>This is a block inside a div.</p>
  <span style="color: red;">Red text inside span</span>
</div>
```

### **b) Using CSS for layout**

* CSS positions elements on a page.
* **Example:**

```html
<style>
  .box { width: 200px; height: 100px; background-color: yellow; margin: 10px; }
</style>

<div class="box">Box 1</div>
<div class="box">Box 2</div>
```

---

## **4️⃣ Backgrounds, Colors, and Text**

### **Backgrounds**

```html
<body style="background-color: lightgray; background-image: url('bg.jpg');">
```

### **Text color and alignment**

```html
<p style="color: blue; text-align: center;">Hello World!</p>
```

---

## **5️⃣ Fonts**

### **Using `<font>` tag (deprecated)**

```html
<font face="Arial" size="4" color="red">Hello</font>
```

* **Note:** Modern HTML uses **CSS instead of `<font>`**.

### **CSS font styles**

```html
<p style="font-family: Verdana; font-size: 18px; color: green;">Styled Text</p>
```

---

## **6️⃣ Tables**

### **Basic Table**

```html
<table border="1">
  <caption>Student Marks</caption>
  <tr>
    <th>Name</th>
    <th>Math</th>
    <th>Science</th>
  </tr>
  <tr>
    <td>Ali</td>
    <td>90</td>
    <td>85</td>
  </tr>
</table>
```

output:
```
+------+-------+--------+
|      Student Marks    |
+------+-------+--------+
| Name | Math  | Science|
+------+-------+--------+
| Ali  |  90   |   85   |
+------+-------+--------+
```

### **Rowspan and Colspan**

```html
<tr>
  <td rowspan="2">Ali</td> <!-- Spans 2 rows -->
  <td>90</td>
  <td>85</td>
</tr>
<tr>
  <td>95</td>
  <td>88</td>
</tr>

<tr>
  <td colspan="2">Total</td> <!-- Spans 2 columns -->
  <td>348</td>
</tr>
```
```
output:

+------+----+----+
| Ali  | 90 | 85 |
|      | 95 | 88 |
+------+----+----+
| Total      |348|
+------------+---+

```
---

## **7️⃣ Frames and Layers**

### **a) `<iframe>` for embedding content**

* Used to embed another page or content inside your page.

```html
<iframe src="https://www.example.com" width="300" height="200"></iframe>
```

### **b) Layers using CSS**

* Layers control **overlapping content** using `position` and `z-index`.
Sure! Here’s a **concise, exam-friendly explanation** of **Frames and Layers** suitable for a **theory answer**:

---

### **Frames and Layers**

**1. Frames:**

* **Definition:** Frames allow a webpage to be divided into **multiple sections (frames)**, each of which can display a different HTML document.
* **Purpose:** Used to show **multiple pages within a single browser window**.
* **Tag used:** `<iframe>` (modern alternative to old `<frame>` tag, which is now obsolete).

**Example:**

```html
<iframe src="page1.html" width="400" height="300"></iframe>
<iframe src="page2.html" width="400" height="300"></iframe>
```

* Each `<iframe>` acts like a **window displaying another webpage**.

**Advantages of `<iframe>`:**

* Embed external content (like YouTube videos, maps).
* Allows independent scrolling in each frame.

**Disadvantages of traditional frames:**

* Complicated navigation and bookmarking.
* Not mobile-friendly.

---

**2. Layers:**

* **Definition:** Layers allow **elements to overlap or stack** on a webpage using CSS.
* **Purpose:** Used to create **pop-ups, floating menus, or overlapping content**.

**Key CSS properties for layers:**

* `position: absolute` → places element at a specific location.
* `z-index` → controls stacking order (higher value appears on top).

**Example:**

```html
<div style="position:absolute; top:50px; left:50px; width:200px; height:100px; background-color: yellow; z-index:1;">Layer 1</div>
<div style="position:absolute; top:80px; left:100px; width:200px; height:100px; background-color: lightblue; z-index:2;">Layer 2</div>
```

* **Layer 2** appears on top of **Layer 1** because its `z-index` is higher.

**Advantages of Layers:**

* Flexible design options.
* Can create dynamic effects like pop-ups, tooltips, and modal windows.

---

**Exam Tip:**

* Remember: **Frames = separate windows in one page**, **Layers = overlapping elements using CSS**.
* Always mention **`<iframe>` for frames** and **`position + z-index` for layers** in theory answers.

---

✅ **Quick memory tips:**

1. Meta → info for browser/search engines
2. Images → `<img>` with `src`, `alt`, size
3. Layout → `<div>`/`<span>` + CSS
4. Background/text → color, alignment, fonts
5. Tables → rows, columns, rowspan/colspan
6. Frames/Layers → `<iframe>` + CSS `position` and `z-index`

---
