
---

# 🌐 **Image Preliminaries in HTML**

Before we can **use images in HTML**, it’s important to understand **basic concepts and preliminaries** about images.

---

## **1️⃣ Image Basics**

* An **image** is a visual content file (like `.jpg`, `.png`, `.gif`, `.svg`) used to enhance a web page.
* In HTML, images are displayed using the **`<img>` tag**.
* Images **cannot have closing tags**; they are **self-closing**.

**Syntax:**

```html
<img src="image.jpg" alt="Description of image">
```

---

## **2️⃣ Important Attributes of `<img>` Tag**

| Attribute | Purpose                                     |
| --------- | ------------------------------------------- |
| `src`     | Source of the image (file path or URL)      |
| `alt`     | Alternate text if image cannot be displayed |
| `width`   | Width of the image in pixels or %           |
| `height`  | Height of the image in pixels or %          |
| `title`   | Tooltip text when hovering over the image   |
| `loading` | Controls lazy loading (`lazy` or `eager`)   |

**Example:**

```html
<img src="flower.jpg" alt="Red Flower" width="300" height="200" title="Beautiful Flower">
```

---

## **3️⃣ Image Formats**

| Format         | Description                                          |
| -------------- | ---------------------------------------------------- |
| `JPEG` / `JPG` | Good for photos, compressed images, small file size  |
| `PNG`          | Supports transparency, better for graphics and logos |
| `GIF`          | Supports animation, small file size, limited colors  |
| `SVG`          | Vector image, scalable without losing quality        |

---

## **4️⃣ Image Placement**

* Images can be **inline with text** or **block elements**.
* You can **align images** using `style` or CSS:

```html
<img src="flower.jpg" alt="Flower" style="float:right; margin:10px;">
```

* CSS allows advanced styling like borders, rounded corners, shadows, etc.

---

## **5️⃣ Accessibility and Best Practices**

1. **Always use `alt` attribute**

   * Helps **screen readers** and users if image fails to load.

2. **Optimize image size**

   * Small images load faster → better user experience.

3. **Use proper file formats**

   * Choose format based on **image type and quality** required.

4. **Responsive images**

   * Use CSS or HTML attributes to make images scale on **different devices**.

---

## **6️⃣ Exam Tip**

* `<img>` is a **self-closing tag**.
* Mandatory attributes: `src`, `alt`.
* Optional but useful: `width`, `height`, `title`, `loading`.

---

### **Simple Example Putting it Together**

```html
<img src="nature.jpg" alt="Beautiful Nature" width="400" height="300" title="Nature Image">
```

**Behavior:**

* Displays a 400x300 image.
* If the image cannot load, text **“Beautiful Nature”** will appear.
* Tooltip shows **“Nature Image”** when hovering.

---