
---

# **Displaying XML Using CSS and XSL**

## **1. Displaying XML Using CSS**

XML can be styled using a **CSS stylesheet**, just like HTML.
This method applies basic formatting (colors, fonts, spacing) but **cannot change layout** (like tables).

### **How it works:**

* Create a CSS file.
* Link it to the XML file using `<?xml-stylesheet?>`.

### **Example:**

**XML File**

```xml
<?xml-stylesheet type="text/css" href="style.css"?>
<note>
    <to>Ali</to>
    <from>Sara</from>
    <message>Hello!</message>
</note>
```

**CSS File (style.css)**

```css
note { display: block; font-size: 20px; }
to { color: blue; }
from { color: green; }
message { color: red; }
```

✔ Simple styling
✘ Cannot transform XML into HTML layout

---

## **2. Displaying XML Using XSL (XSLT)**

XSLT (Extensible Stylesheet Language Transformations) is used to **convert XML into HTML** so it can be displayed nicely in a browser.

### **How it works:**

* Create an XSL file with rules for transforming XML.
* Link it to the XML file.

### **Example:**

**XSL File**

```xml
<xsl:stylesheet version="1.0"
 xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
<html>
<body>
<h2>Student List</h2>
<xsl:for-each select="students/student">
<p>Name: <xsl:value-of select="name"/> | Age: <xsl:value-of select="age"/></p>
</xsl:for-each>
</body>
</html>
</xsl:template>
</xsl:stylesheet>
```

✔ Powerful
✔ Can produce full HTML
✔ Best for complex layouts

---

## **Summary**

* **CSS** → Styles XML directly (colors/fonts).
* **XSL/XSLT** → Converts XML into HTML for full display control.
