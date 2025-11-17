
---

# 🌐 **Static HTML vs Dynamic HTML**

Web pages can either be **static** or **dynamic**, depending on how they behave when users interact with them.

---

## **1️⃣ Static HTML**

### **Definition:**

* A **static HTML page** displays **fixed content**.
* Once written and loaded, the content **does not change** unless the developer manually edits the HTML file.
* It **cannot respond** to user actions automatically.

### **Features:**

* Simple to create and understand
* Faster to load
* Works in all browsers
* No interactivity
* Good for simple web pages like brochures, contact info, or company info pages

### **Example:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Static Page</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a static web page. Content will not change automatically.</p>
</body>
</html>
```

**Behavior:**

* The page will always display the same text: “Welcome to My Website”
* User actions like clicks or typing will **not change the page content**.

---

## **2️⃣ Dynamic HTML (DHTML)**

### **Definition:**

* A **dynamic HTML page** can **change its content and style on the fly**, without reloading the page.
* It responds to **user actions** like clicks, mouse movements, or keyboard input.

### **Features:**

* Interactive and responsive
* Uses **HTML + CSS + JavaScript + DOM**
* Can update content **instantly**
* Animations, hover effects, moving images, pop-ups, interactive forms are possible
* Slower to load if too many scripts are used

### **Example:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>Dynamic Page</title>
  <style>
    #message {
      color: blue;
      font-size: 20px;
    }
  </style>
  <script>
    function changeMessage() {
      document.getElementById("message").innerHTML = "You clicked the button! 🎉";
      document.getElementById("message").style.color = "green";
    }
  </script>
</head>
<body>
  <h1>Welcome to Dynamic Page</h1>
  <p id="message">Click the button below to see magic!</p>
  <button onclick="changeMessage()">Click Me</button>
</body>
</html>
```

**Behavior:**

* Initially shows: “Click the button below to see magic!”
* When user clicks the button:

  * Text changes to “You clicked the button! 🎉”
  * Text color changes to green
* **No page reload is needed**

---

## **3️⃣ Comparison Table**

| Feature           | Static HTML                    | Dynamic HTML (DHTML)                    |
| ----------------- | ------------------------------ | --------------------------------------- |
| Content           | Fixed                          | Can change dynamically                  |
| User Interaction  | No                             | Yes                                     |
| Technologies Used | HTML only                      | HTML + CSS + JavaScript + DOM           |
| Page Reload       | Required to update content     | Not required                            |
| Examples          | Company info page, resume page | Interactive form, hover menu, animation |
| Speed             | Faster                         | Slightly slower if many scripts         |

---

## **4️⃣ Summary for Exams**

* **Static HTML:** simple, fixed, no interactivity.
* **Dynamic HTML:** interactive, responsive, changes based on user action.
* **Remember:** DHTML = HTML + CSS + JavaScript + DOM → allows **dynamic behavior**.

---
