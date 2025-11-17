
---

# 🌐 **Meta Information in HTML**

* **Meta information** is **data about the web page**.
* It is **not displayed** on the web page itself but is used by **browsers, search engines, and other services**.
* Meta information is placed **inside the `<head>` section** of an HTML document.

---

## **1️⃣ `<meta>` Tag**

* The `<meta>` tag is **self-closing** and does **not have a closing tag**.
* Syntax:

```html
<meta name="..." content="...">
```

---

## **2️⃣ Common Types of Meta Information**

| Attribute            | Purpose                                                    | Example                                                                     |
| -------------------- | ---------------------------------------------------------- | --------------------------------------------------------------------------- |
| `charset`            | Defines **character encoding**                             | `<meta charset="UTF-8">`                                                    |
| `name="description"` | Short **description of the page** (used by search engines) | `<meta name="description" content="This is a tutorial on HTML meta tags.">` |
| `name="keywords"`    | Keywords for SEO                                           | `<meta name="keywords" content="HTML, meta tags, tutorial">`                |
| `name="author"`      | Author of the page                                         | `<meta name="author" content="John Doe">`                                   |
| `name="viewport"`    | Controls **how page appears on mobile devices**            | `<meta name="viewport" content="width=device-width, initial-scale=1.0">`    |
| `http-equiv`         | Provides **HTTP headers**                                  | `<meta http-equiv="refresh" content="5;url=https://example.com">`           |

---

## **3️⃣ Examples**

### **1. Character Encoding**

```html
<meta charset="UTF-8">
```

* Ensures that text displays correctly (supports symbols, special characters, and other languages).

### **2. Page Description**

```html
<meta name="description" content="Learn HTML meta tags with examples.">
```

* Search engines like Google show this description in **search results**.

### **3. Keywords**

```html
<meta name="keywords" content="HTML, meta, tutorial, web development">
```

* Helps search engines understand the **topic of the page**.

### **4. Author**

```html
<meta name="author" content="Jane Smith">
```

* Identifies the **creator of the web page**.

### **5. Viewport (Mobile Friendly)**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

* Makes the page **responsive** on mobile devices.

### **6. Refresh / Redirect**

```html
<meta http-equiv="refresh" content="5;url=https://example.com">
```

* Automatically **redirects** the page to another URL after 5 seconds.

---

## **4️⃣ Key Points for Exams**

* Meta tags are inside `<head>`
* **Not visible** on the page
* Help with **SEO, page display, mobile responsiveness, and redirects**
* Always use `charset="UTF-8"` for proper character support

---
