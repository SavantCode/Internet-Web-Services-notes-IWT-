Absolutely! Let’s go **very detailed, exam-friendly, and simple** for **JavaScript**, so you could easily write **10-mark answers for each subtopic**. I’ll structure it **step by step with theory, examples, and explanation**.

---

# **4️⃣ Introduction to JavaScript**

---

## **4.1 Basics of JavaScript**

**Definition:**
JavaScript is a **client-side scripting language** used to make web pages **dynamic and interactive**. It allows you to **perform actions in the browser**, respond to events, and manipulate page content without reloading.

**Key Features:**

* Runs in the browser.
* Can interact with HTML elements.
* Supports variables, loops, conditions, functions, events.

---

### **a) Variables**

**Definition:**
Variables are **containers for storing data**.

**Syntax:**

```javascript
var name = "Ali";      // older way
let age = 20;          // modern way
const pi = 3.14;       // constant, cannot change
```

**Example:**

```javascript
let studentName = "Ali";
let studentAge = 18;
const schoolName = "XYZ School";
```

**Explanation:**

* `var` → old way, can be redeclared.
* `let` → modern, can be updated but not redeclared in the same scope.
* `const` → value cannot be changed.

---

### **b) Data Types**

1. **String:** Text → `"Hello"`
2. **Number:** Numeric → `100`, `3.14`
3. **Boolean:** True/False → `true`, `false`
4. **Array:** List of values → `[1,2,3]`
5. **Object:** Key-value pair → `{name:"Ali", age:18}`
6. **Undefined / Null:** Empty or no value

**Example:**

```javascript
let name = "Ali";       // String
let age = 20;           // Number
let isStudent = true;   // Boolean
let subjects = ["Math","Science"]; // Array
let student = {name:"Ali", age:20}; // Object
```

---

### **c) Operators**

1. **Arithmetic:** `+ - * / %`
2. **Assignment:** `=, +=, -=`
3. **Comparison:** `==, ===, !=, <, >`
4. **Logical:** `&&, ||, !`

**Example:**

```javascript
let a = 10;
let b = 5;
console.log(a + b);   // 15
console.log(a > b);   // true
```

---

## **4.2 Conditional Statements**

Conditional statements **perform actions based on conditions**.

### **a) If Statement**

```javascript
let age = 18;
if(age >= 18){
  console.log("You are an adult");
} else {
  console.log("You are a minor");
}
```

**Explanation:**

* Checks if condition is true, executes code inside `{ }`.
* `else` runs if condition is false.

---

### **b) Switch Statement**

```javascript
let day = 2;
switch(day){
  case 1: console.log("Monday"); break;
  case 2: console.log("Tuesday"); break;
  default: console.log("Other day");
}
```

**Explanation:**

* Used when **many conditions** are possible.
* `break` prevents running all cases.
* `default` runs if none matches.

---

## **4.3 Loops**

Loops **repeat code multiple times**.

### **a) For Loop**

```javascript
for(let i=1; i<=5; i++){
  console.log(i);  // prints 1,2,3,4,5
}
```

### **b) While Loop**

```javascript
let i = 1;
while(i<=5){
  console.log(i);
  i++;
}
```

**Explanation:**

* **For loop:** Best when you know the number of iterations.
* **While loop:** Best when you don’t know how many times it will run.

---

## **4.4 DOM Manipulation**

**Definition:**
DOM (Document Object Model) allows JavaScript to **access and modify HTML elements** dynamically.

 **Purpose:**

   * Makes web pages **interactive and dynamic**.
   * Allows **manipulation of content, styles, and structure** without reloading the page.
### **a) Accessing HTML Elements**

```html
<p id="demo">Hello</p>
```

```javascript
let para = document.getElementById("demo");
console.log(para.innerHTML);  // Hello
```

### **b) Modifying HTML Elements**

```javascript
para.innerHTML = "Hello World!";   // Changes text
para.style.color = "red";          // Changes text color
```

**Other Methods:**

* `document.querySelector()` → select using CSS selector
* `document.getElementsByClassName()` → select by class

**Example:**

```javascript
document.querySelector("h1").style.fontSize = "30px";
```

---

# **Cookies**
## **4.5 Cookies**

**Definition:**
Cookies are **small pieces of data stored in the user’s browser** to remember information like login or preferences.


---


1. **Definition:**

   * A **cookie** is a **small piece of data stored by a web browser** on a user’s computer.
   * It allows websites to **remember information about the user** across sessions.

2. **Purpose / Uses:**

   * **User Authentication:** Remember login sessions.
   * **Personalization:** Store user preferences like theme, language, or layout.
   * **Tracking:** Keep track of user behavior on the website for analytics.
   * **Shopping Carts:** Remember items added to cart in e-commerce websites.

3. **Key Features:**

   * Small in size (usually ~4KB).
   * Stored on the **client-side** (user’s browser).
   * Sent automatically to the server with each HTTP request to maintain **state**.

4. **Types of Cookies:**

   * **Session Cookies:** Temporary; deleted when browser is closed.
   * **Persistent Cookies:** Stored for a specified time; remain after closing the browser.
   * **Secure Cookies:** Sent only over secure (HTTPS) connections.
   * **HttpOnly Cookies:** Not accessible via JavaScript, used for security.

5. **Importance in Web Development:**

   * Helps create **personalized experiences** for users.
   * Enables websites to **remember user choices** without requiring repeated input.
   * Supports **state management** in web applications where HTTP is stateless.

6. **Advantages:**

   * Easy to implement and use.
   * Enhances user experience by storing preferences.
   * Lightweight storage mechanism.

7. **Limitations / Concerns:**

   * Limited storage size.
   * Can be disabled by the user.
   * Privacy concerns if used for tracking without consent.




### **a) Creating Cookies**

```javascript
document.cookie = "username=Ali; expires=Fri, 31 Dec 2025 12:00:00 UTC; path=/";
```

### **b) Reading Cookies**

```javascript
let x = document.cookie;
console.log(x);
```

### **c) Updating Cookies**

* Overwrite cookie with same name:

```javascript
document.cookie = "username=Ahmed; expires=Fri, 31 Dec 2025 12:00:00 UTC; path=/";
```

### **d) Deleting Cookies**

* Set expiry date to past:

```javascript
document.cookie = "username=Ali; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/";
```

---

