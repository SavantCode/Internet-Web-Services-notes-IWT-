

---

# ⭐ **DHTML (Dynamic HTML)**

DHTML stands for **Dynamic HyperText Markup Language**.
It is **not a language by itself**, but a *combination* of technologies used to create **interactive and animated web pages**.

Think of DHTML as:
👉 **HTML + CSS + JavaScript + DOM**

---

# 🔹 **1. What is DHTML?**

DHTML allows a web page to **change dynamically** on the browser **without reloading** the page.

Examples:

* Text changes color when you hover
* Menus that expand/collapse
* Moving images/animations
* Form validation without reloading
* Popup messages
* Interactive buttons

---

# 🔹 **2. Technologies Used in DHTML**

### **1. HTML**

Provides the **structure** of the page.

### **2. CSS**

Controls **styling** and formatting.

### **3. JavaScript**

Adds **interactivity** and dynamic behavior.

### **4. DOM (Document Object Model)**

Allows JavaScript to **access and modify** HTML elements.
Example:
`document.getElementById("title").style.color = "red";`

---

# 🔹 **3. Features of DHTML**

* Dynamic content change
* Real-time page updates
* Animations & transitions
* Form validation
* Style changes on events
* Interactive user experience
* No need to reload the full page

---

# 🔹 **4. How DHTML Works (Simple Flow)**

1. The web page loads HTML + CSS.
2. JavaScript detects user actions (click, hover, scroll…).
3. Through DOM, JavaScript changes:

   * Text
   * Images
   * Styles
   * Position of elements
4. Browser displays updates instantly.

---

# 🔹 **5. DHTML Example Code**

```html
<html>
<head>
    <style>
        #box {
            width: 100px;
            height: 100px;
            background: blue;
        }
    </style>

    <script>
        function changeColor() {
            document.getElementById("box").style.background = "green";
        }
    </script>
</head>

<body>
    <div id="box" onmouseover="changeColor()"></div>
</body>
</html>
```

**What happens:**
When you hover the box, JavaScript changes its color → **Dynamic behavior = DHTML**.

---

# 🔹 **6. Advantages of DHTML**

* Improved user interaction
* Faster responses without page reload
* Rich, animated web interfaces
* Better visual effects
* Real-time content updates

---

# 🔹 **7. Limitations of DHTML**

* Browser compatibility issues
* Heavy use of JavaScript can slow pages
* Harder to maintain
* Limited compared to modern technologies like **AJAX, React, Angular**

---

# 🔹 **8. DHTML vs HTML (Important for Exams)**

| HTML               | DHTML                         |
| ------------------ | ----------------------------- |
| Static pages       | Dynamic pages                 |
| No instant updates | Real-time updates             |
| Only structure     | Structure + style + scripting |
| Page reload needed | No reload needed              |
| No animations      | Supports animations           |

---

# 🎯 **Exam Definition (Short Answer)**

**DHTML is a combination of HTML, CSS, JavaScript, and DOM used to create interactive and dynamic web pages where elements can be changed without reloading the page.**

---
