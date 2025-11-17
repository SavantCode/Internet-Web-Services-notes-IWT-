

---

# 🌐 **Features of a Web Server**

A **web server** is software (and sometimes hardware) that handles **HTTP/HTTPS requests** and serves content to clients (like web browsers). The key **features** are:

---

### **1️⃣ Handling HTTP/HTTPS Requests**

* Web servers communicate using **HTTP (Hypertext Transfer Protocol)** and **HTTPS (secure HTTP)**.
* They receive requests from clients (browsers, apps) and send back responses.
* Supports **GET, POST, PUT, DELETE** methods.

**Example:**
A browser requests `index.html`, the server sends the HTML page back.

---

### **2️⃣ Serving Static Content**

* Can deliver **static files** like:

  * HTML pages
  * CSS files
  * JavaScript files
  * Images, videos, and PDFs

**Static content** doesn’t change unless manually updated on the server.

---

### **3️⃣ Serving Dynamic Content**

* Can generate **dynamic content** using server-side scripts.
* Works with languages like **PHP, Python, Node.js, Java (JSP)**.
* Can query **databases** to create personalized pages.

**Example:**
A user logs in, and the server fetches their name from the database to show “Welcome, Anushka!”.

---

### **4️⃣ Virtual Hosting**

* Allows hosting **multiple websites** on a **single web server**.
* Each site can have its **own domain name** but share the same server resources.

**Example:**
`example1.com` and `example2.com` hosted on the same server using Apache or Nginx.

---

### **5️⃣ Logging and Monitoring**

* Web servers maintain **logs of all requests**:

  * Access logs → who visited, when, and what page.
  * Error logs → failed requests or server issues.
* Helps in **debugging, analytics, and security audits**.

---

### **6️⃣ Security Features**

* Supports **SSL/TLS** for encrypted HTTPS connections.
* Can implement:

  * Authentication (username/password)
  * IP restrictions
  * Firewalls
* Protects websites from **unauthorized access** and **data theft**.

---

### **7️⃣ Load Balancing**

* Can distribute incoming requests across **multiple servers**.
* Ensures **better performance, fault tolerance, and scalability**.
* Used in **high-traffic websites**.

---

### **8️⃣ URL Redirection and Rewriting**

* Can **redirect users** from one page to another.
* Helps with **SEO, domain changes, and user navigation**.

**Example:**
Redirect `http://example.com` → `https://www.example.com`.

---

### **9️⃣ Support for Web Applications**

* Web servers can **run scripts or applications** that process user input.
* Works with frameworks like:

  * Django (Python)
  * Express.js (Node.js)
  * Laravel (PHP)

---

### **10️⃣ Caching**

* Can **store frequently accessed data** to improve speed.
* Reduces server load and improves **user experience**.

**Example:**
Images, CSS, or HTML pages can be cached in memory for faster delivery.

---

### **11️⃣ Modular Architecture (Optional Feature)**

* Many web servers allow **modules/plugins** to add extra features.
* Example: Apache modules for SSL, authentication, URL rewriting.

---