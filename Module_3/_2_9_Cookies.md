
---

# 🌐 **Cookies in Web Development**

**Definition:**
A **cookie** is a **small piece of data stored on the user’s browser** by a website. Cookies allow websites to **remember user information** and provide a **personalized experience**.

**Example Use Cases:**

* Remembering login credentials
* Storing user preferences (theme, language)
* Keeping track of items in a shopping cart

---

## **1️⃣ Types of Cookies**

| Type                   | Description                                                     |
| ---------------------- | --------------------------------------------------------------- |
| **Session Cookies**    | Temporary cookies that are deleted when the browser closes      |
| **Persistent Cookies** | Stored for a set period (days, months, years) until they expire |
| **Secure Cookies**     | Sent only over **HTTPS** connections                            |
| **HttpOnly Cookies**   | Not accessible via JavaScript; only sent to the server          |

---

## **2️⃣ Creating Cookies**

Cookies can be created **using JavaScript or server-side scripting (like PHP)**.

### **A. Using JavaScript**

**Syntax:**

```javascript
document.cookie = "username=Anushka; expires=Fri, 31 Dec 2025 12:00:00 UTC; path=/";
```

**Explanation:**

* `username=Anushka` → Name and value of the cookie
* `expires` → Optional; when the cookie should expire
* `path=/` → Optional; defines the path where the cookie is accessible

**Example:**

```javascript
// Create a cookie named "user" with value "Virat"
document.cookie = "user=Virat; expires=Fri, 31 Dec 2025 12:00:00 UTC; path=/";
```

---

### **B. Using PHP (Server-side)**

```php
<?php
// Create a cookie named "user" with value "Virat" that expires in 1 day
setcookie("user", "Virat", time() + 86400, "/"); // 86400 seconds = 1 day
?>
```

---

## **3️⃣ Reading Cookies**

### **A. Using JavaScript**

```javascript
// Get all cookies
console.log(document.cookie);

// Split and read individual cookies
let cookies = document.cookie.split("; ");
cookies.forEach(cookie => {
    let [name, value] = cookie.split("=");
    console.log(name + " = " + value);
});
```

**Example:**
If cookies are:

```
user=Virat; theme=dark
```

Output:

```
user = Virat
theme = dark
```

---

### **B. Using PHP**

```php
<?php
if(isset($_COOKIE["user"])) {
    echo "User is " . $_COOKIE["user"];
} else {
    echo "No cookie found";
}
?>
```

---

## **4️⃣ Deleting Cookies**

* In **JavaScript**: Set the `expires` date in the past:

```javascript
document.cookie = "user=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
```

* In **PHP**:

```php
setcookie("user", "", time() - 3600, "/");
```

---

## **5️⃣ Key Points for Exams**

1. Cookies **store small data on the client-side**.
2. Use **`document.cookie` in JavaScript** or **`setcookie()` in PHP** to create.
3. **Read cookies** using `document.cookie` (JS) or `$_COOKIE` (PHP).
4. **Expire or delete cookies** by setting the expiration in the past.
5. Cookies are used for **session management, personalization, and tracking**.

---

### **Simple Analogy:**

Think of a cookie as a **sticky note** a website leaves on your browser:

* It reminds the website **who you are** next time you visit.
* It can be **temporary (session)** or **long-term (persistent)**.

---
