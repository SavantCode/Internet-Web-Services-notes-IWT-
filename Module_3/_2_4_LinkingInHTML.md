

---

# 🌐 **Linking in HTML**

In HTML, **linking** is the process of connecting your web page to:

1. **Other web pages**
2. **Websites**
3. **Files** (like images, documents, CSS, or JavaScript)
4. **Email addresses**

---

## **1️⃣ Linking to Another Web Page (Hyperlinks)**

* Use the `<a>` tag (anchor tag) to create links.
* **Syntax:**

```html
<a href="URL">Link Text</a>
```

* **Attributes of `<a>` tag:**

  1. `href` → URL of the page or file
  2. `target` → where the page opens (`_blank` for new tab)
  3. `title` → tooltip text

**Example:**

```html
<a href="https://www.google.com" target="_blank" title="Go to Google">
  Visit Google
</a>
```

**Behavior:**

* Clicking the link opens Google in a **new tab**.

---

## **2️⃣ Linking to a File (Download)**

* You can link **files like PDFs, images, or documents** for download.

```html
<a href="file.pdf" download>Download PDF</a>
```

* `download` attribute tells the browser to **download the file** instead of opening it.

---

## **3️⃣ Linking to an Email Address**

* Use `mailto:` in the `href` to open the user’s email client.

```html
<a href="mailto:example@gmail.com">Send Email</a>
```

**Behavior:**

* Clicking the link opens the default **email app** with recipient prefilled.

---

## **4️⃣ Linking Within the Same Page (Anchors)**

* You can link to a **specific section** in the same page using **IDs**.

**Step 1:** Give the section an `id`

```html
<h2 id="section1">Section 1</h2>
<p>Content of section 1...</p>
```

**Step 2:** Link to it

```html
<a href="#section1">Go to Section 1</a>
```

**Behavior:**

* Clicking the link **jumps to that section** in the page.

---

## **5️⃣ Linking External CSS or JavaScript**

* **CSS**

```html
<link rel="stylesheet" href="styles.css">
```

* **JavaScript**

```html
<script src="script.js"></script>
```

**Purpose:**

* Keeps **code organized** and allows **reusing styles/scripts** across multiple pages.

---

## **6️⃣ Summary Table**

| Type of Linking  | Tag / Attribute                           | Example                                     |
| ---------------- | ----------------------------------------- | ------------------------------------------- |
| Web page link    | `<a href="URL">`                          | `<a href="https://example.com">Click</a>`   |
| File download    | `<a href="file" download>`                | `<a href="doc.pdf" download>Download</a>`   |
| Email link       | `<a href="mailto:email@example.com">`     | `<a href="mailto:test@gmail.com">Email</a>` |
| Within same page | `<a href="#id">`                          | `<a href="#section1">Go to Section 1</a>`   |
| CSS file         | `<link rel="stylesheet" href="file.css">` | `<link rel="stylesheet" href="styles.css">` |
| JS file          | `<script src="file.js"></script>`         | `<script src="script.js"></script>`         |

---

💡 **Exam Tip:**

* **Remember:** `<a>` tag is for hyperlinks.
* `href` = **destination**
* `target="_blank"` = opens in **new tab**
* Anchors with `id` = **navigate within the page**

---
