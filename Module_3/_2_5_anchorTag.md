

---

# 🌐 **Anchor (`<a>`) Tag Attributes in HTML**

The **anchor tag `<a>`** is used to create **hyperlinks** in HTML. It can have several **attributes** that control how the link behaves.

---

## **1️⃣ `href` (Hypertext Reference)**

* **Purpose:** Specifies the **URL or link destination**.
* **Can link to:** another page, a section of the same page, a file, or an email.

**Examples:**

* Link to another website:

```html
<a href="https://www.google.com">Go to Google</a>
```

* Link to a section within the same page:

```html
<a href="#section1">Go to Section 1</a>
```

* Link to an email address:

```html
<a href="mailto:test@gmail.com">Send Email</a>
```

---

## **2️⃣ `target`**

* **Purpose:** Specifies **where to open the linked document**.

**Values:**

| Value     | Meaning                              |
| --------- | ------------------------------------ |
| `_self`   | Opens in the same tab (default)      |
| `_blank`  | Opens in a new tab or window         |
| `_parent` | Opens in the parent frame            |
| `_top`    | Opens in the full body of the window |

**Example:**

```html
<a href="https://example.com" target="_blank">Open in New Tab</a>
```

---

## **3️⃣ `title`**

* **Purpose:** Provides **tooltip text** when the user hovers over the link.
* Helps improve **accessibility**.

**Example:**

```html
<a href="https://example.com" title="Visit Example Site">Example</a>
```

---

## **4️⃣ `download`**

* **Purpose:** Tells the browser to **download the linked file** instead of opening it.
* Can also specify the **filename**.

**Example:**

```html
<a href="file.pdf" download>Download PDF</a>
<a href="file.pdf" download="MyFile.pdf">Download as MyFile.pdf</a>
```

---

## **5️⃣ `rel` (Relationship)**

* **Purpose:** Defines the **relationship between the current page and the linked page**.
* Often used for **SEO or security purposes**.

**Common values:**

* `nofollow` → tells search engines **not to follow** the link
* `noopener` → prevents **new tab from accessing window.opener** (security)
* `noreferrer` → does not send referrer info

**Example:**

```html
<a href="https://example.com" rel="nofollow" target="_blank">Example</a>
```

---

## **6️⃣ `id` and `class` (Optional)**

* Used to **style or navigate links** with CSS or JavaScript.
  **Example:**

```html
<a href="#top" id="backToTop" class="btn-link">Back to Top</a>
```

---

## **7️⃣ Summary Table of Anchor Attributes**

| Attribute  | Purpose                           | Example                                  |
| ---------- | --------------------------------- | ---------------------------------------- |
| `href`     | Link destination                  | `<a href="page.html">Go</a>`             |
| `target`   | Where to open the link            | `<a target="_blank">Open in new tab</a>` |
| `title`    | Tooltip text                      | `<a title="Tooltip">Hover me</a>`        |
| `download` | Download linked file              | `<a download>Download</a>`               |
| `rel`      | Relationship or SEO/security info | `<a rel="nofollow">Link</a>`             |
| `id`       | Unique identifier for CSS/JS      | `<a id="link1">Link</a>`                 |
| `class`    | Group for styling/JS              | `<a class="btn">Link</a>`                |

---

💡 **Exam Tip:**

* **Mandatory attribute:** `href`
* **Optional but useful:** `target`, `title`, `download`, `rel`
* Use `#id` in `href` for **internal navigation**

---

