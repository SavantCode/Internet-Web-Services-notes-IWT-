
---

# **3️⃣ CSS (Cascading Style Sheets)**

---

## **1. Introduction to CSS**

**Definition:**
CSS (Cascading Style Sheets) is a **style sheet language** used to **control the presentation of HTML elements**. It allows you to **separate content (HTML) from design (CSS)**, making websites easier to maintain and more attractive.

**Purpose of CSS:**

* Change the **appearance** of web pages (colors, fonts, layout).
* Make web pages **responsive** and **visually appealing**.
* Reduce **repetition** by styling multiple elements at once.

**Example (HTML + CSS):**

```html
<!DOCTYPE html>
<html>
<head>
<style>
  p { color: blue; font-size: 18px; }
</style>
</head>
<body>
<p>This is a styled paragraph using CSS.</p>
</body>
</html>
```

* The paragraph appears **blue** and **18px in size**.

---

## **2. Types of CSS**

CSS can be applied to HTML in **three ways**:

### **a) Inline CSS**

* Applied directly to an HTML element using the `style` attribute.

```html
<p style="color:red; font-size:16px;">Inline CSS Example</p>
```

* **Pros:** Quick and simple.
* **Cons:** Hard to maintain for large websites.

---

### **b) Internal CSS**

* Placed inside the `<style>` tag in the `<head>` section.

```html
<head>
<style>
h1 { color: green; text-align: center; }
</style>
</head>
<body>
<h1>Internal CSS Example</h1>
</body>
```

* **Pros:** Useful for styling a single page.
* **Cons:** Cannot be reused across multiple pages.

---

### **c) External CSS**

* Stored in a **separate `.css` file** and linked using `<link>`.

```html
<head>
<link rel="stylesheet" href="style.css">
</head>
```

* **style.css:**

```css
body { background-color: lightyellow; }
h2 { color: purple; }
```

* **Pros:** Styles can be applied to multiple pages, easier to maintain.
* **Cons:** Requires extra HTTP request to load the CSS file.

---

## **3. Positioning with Stylesheets**

**CSS positioning** controls the **placement of HTML elements** on the page.

### **a) Static Positioning (default)**

* Elements are positioned according to the **normal flow of the page**.

```css
p { position: static; }
```

* **No effect** unless you specify other properties.

---

### **b) Relative Positioning**

* Moves an element **relative to its normal position**.

```css
p { position: relative; top: 10px; left: 20px; }
```

* Moves **10px down** and **20px right** from its original position.

---

### **c) Absolute Positioning**

* Positions an element **relative to the nearest positioned ancestor** (or the page if none exists).

```css
div { position: relative; width: 300px; height: 200px; background: yellow; }
p { position: absolute; top: 50px; left: 50px; }
```

* The paragraph will appear **50px from the top and left** inside the div.

---

### **d) Fixed Positioning**

* The element stays **fixed relative to the viewport** even when scrolling.

```css
p { position: fixed; top: 0; right: 0; background: lightblue; }
```

* Example: **Sticky headers or floating buttons**.

---

### **e) Sticky Positioning**

* Combines **relative** and **fixed**.
* Sticks the element to the top when you **scroll past it**.

```css
h2 { position: sticky; top: 0; background: yellow; }
```

---

## **4. Styling Web Elements**

### **a) Text Styling**

* **Color:** `color: blue;`
* **Font family:** `font-family: Arial, sans-serif;`
* **Font size:** `font-size: 18px;`
* **Text alignment:** `text-align: center;`

**Example:**

```css
p { color: red; font-family: Verdana; font-size: 16px; text-align: center; }
```

---

### **b) Backgrounds**

* Background color: `background-color: lightgray;`
* Background image: `background-image: url('bg.jpg');`

**Example:**

```css
body {
  background-color: lightyellow;
  background-image: url('pattern.png');
}
```

---

### **c) Borders**
Borders are the lines around an HTML element that help **define its boundaries**. Borders can be **styled, colored, and rounded** using CSS.

**Why Borders are important:**

* Improve the **visual structure** of a web page.
* Highlight important sections (like boxes, cards, or menus).
* Can create shapes and designs when combined with colors and radius.

## **1. Border Properties**

CSS has **four main border properties**:

1. **`border-width`** – Thickness of the border

   * Example: `border-width: 2px;`

2. **`border-style`** – Type of border line

   * Values:

     * `solid` → a single line
     * `dotted` → small dots
     * `dashed` → dashes
     * `double` → two lines
     * `groove` → 3D grooved effect
     * `ridge` → 3D ridged effect
     * `none` → no border
     * `hidden` → hides the border
   * Example: `border-style: dashed;`

3. **`border-color`** – Color of the border

   * Example: `border-color: red;`

4. **`border-radius`** – Rounds the corners of the border

   * Example: `border-radius: 10px;` → smooth rounded corners

---





* `border: 2px solid black;`
* `border-radius: 10px;` → rounded corners

**Example:**

```css
div { border: 2px solid black; border-radius: 8px; padding: 10px; }
```


---

### **d) Margins and Padding**

* **Margin:** Space **outside** an element
* **Padding:** Space **inside** an element, between content and border

**Example:**

```css
div {
  margin: 20px;
  padding: 15px;
  border: 1px solid gray;
}
```

---

### **e) Layout Adjustments**

* Width and height: `width: 200px; height: 100px;`
* Display: `block`, `inline`, `inline-block`
* Flexbox for alignment: `display: flex; justify-content: center; align-items: center;`

**Example:**

```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px;
  background-color: lightblue;
}
```

---

## **Summary for Exams**

1. **CSS** separates content from design and makes web pages visually appealing.
2. **Types:**

   * Inline → direct in element
   * Internal → `<style>` in head
   * External → separate `.css` file
3. **Positioning:** static, relative, absolute, fixed, sticky
4. **Text and Fonts:** color, font-family, font-size, alignment
5. **Backgrounds and Borders:** colors, images, border style, radius
6. **Margins & Padding:** control space inside/outside elements
7. **Layouts:** width, height, display, flexbox

---
```
CSS Positioning Example

+----------------------------------------------------+
|               Static Position (normal flow)       |
|  [Header]                                         |
|                                                    |
|  [Paragraph]                                      |
|                                                    |
+----------------------------------------------------+

+----------------------------------------------------+
|               Relative Position                   |
|  [Paragraph - shifted 20px right, 10px down]     |
+----------------------------------------------------+

+----------------------------------------------------+
|               Absolute Position                   |
|  Parent Container:                                |
|  +----------------------+                          |
|  | [Absolute Box]      | <-- positioned inside   |
|  +----------------------+     parent container   |
+----------------------------------------------------+

+----------------------------------------------------+
|               Fixed Position                      |
|  [Fixed Header - stays at top even on scroll]     |
|                                                    |
|  [Content scrolls underneath]                     |
+----------------------------------------------------+

+----------------------------------------------------+
|               Sticky Position                     |
|  [Sticky Header - sticks at top when scrolling]   |
|                                                    |
|  [Content scrolls below until header sticks]      |
+----------------------------------------------------+
```