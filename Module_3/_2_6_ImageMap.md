
---

# 🌐 **HTML Image Maps**

An **image map** allows you to make **different parts of an image clickable**, linking to **different URLs**.
Instead of the **whole image being a single link**, each **region** can have its **own link**.

---

## **1️⃣ Types of Image Maps**

1. **Client-side image map**

   * Defined in **HTML**.
   * Browser handles the clickable regions.

2. **Server-side image map**

   * Sends the **click coordinates to the server** for processing.
   * Rarely used now; client-side is more common.

---

## **2️⃣ Client-Side Image Maps in HTML**

* Use `<img>` with `usemap` attribute.
* Use `<map>` and `<area>` to define clickable regions.

### **Syntax:**

```html
<img src="example.jpg" usemap="#mapname" alt="Example Image">

<map name="mapname">
  <area shape="rect" coords="x1,y1,x2,y2" href="link1.html" alt="Rectangle">
  <area shape="circle" coords="x,y,radius" href="link2.html" alt="Circle">
  <area shape="poly" coords="x1,y1,x2,y2,x3,y3,..." href="link3.html" alt="Polygon">
</map>
```

---

## **3️⃣ Attributes of `<area>` Tag**

| Attribute | Purpose                                                            |
| --------- | ------------------------------------------------------------------ |
| `shape`   | Defines the shape of the clickable area (`rect`, `circle`, `poly`) |
| `coords`  | Coordinates of the shape (pixels)                                  |
| `href`    | Link to the page when area is clicked                              |
| `alt`     | Alternate text for the area                                        |
| `target`  | Where to open the link (`_blank`, `_self`)                         |

---

## **4️⃣ Example of an Image Map**

```html
<img src="worldmap.jpg" usemap="#worldmap" alt="World Map">

<map name="worldmap">
  <area shape="rect" coords="50,50,150,150" href="asia.html" alt="Asia">
  <area shape="circle" coords="300,100,50" href="africa.html" alt="Africa">
  <area shape="poly" coords="400,200,450,250,420,300" href="europe.html" alt="Europe">
</map>
```

**Explanation:**

* `shape="rect"` → clickable rectangle
* `shape="circle"` → clickable circle
* `shape="poly"` → clickable polygon
* `coords` define the size and position of the clickable area on the image

**Behavior:**

* Clicking different areas of the image opens **different pages**.

---

## **5️⃣ Exam Tips**

* Use **client-side image maps** (with `<map>` and `<area>`).
* Remember the **3 shapes**: `rect`, `circle`, `poly`.
* `usemap="#mapname"` on the `<img>` tag **links image to map**.
* Each `<area>` must have **href** and **alt** attributes.

---
