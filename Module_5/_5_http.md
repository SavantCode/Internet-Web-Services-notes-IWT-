

---

## **HTTP (HyperText Transfer Protocol)**

**Definition:**
HTTP is a **protocol** used for **communication between a web browser (client) and a web server**. It defines how messages are **formatted, transmitted, and responded to** on the web.

In simple terms:

> HTTP is the “language” that browsers and servers use to talk to each other.

---

### **Key Features of HTTP**

1. **Client-Server Model:**

   * Browser (client) sends a request.
   * Web server sends a response.
   * Example: When you type `www.example.com`, your browser sends an HTTP request to the server, which responds with the website’s content.

2. **Stateless Protocol:**

   * HTTP does **not remember previous requests**.
   * Each request is independent.
   * Example: If you log in and open a new page, the server doesn’t automatically know it’s you unless sessions or cookies are used.

3. **Request-Response Mechanism:**

   * **Request:** Sent by the client (GET, POST, PUT, DELETE).
   * **Response:** Sent by the server (HTML, JSON, XML, images).

4. **Flexible & Extensible:**

   * Can handle text, images, videos, or any kind of web content.

---

### **Common HTTP Methods**

| Method | Purpose       | Example Use         |
| ------ | ------------- | ------------------- |
| GET    | Retrieve data | Open a web page     |
| POST   | Send data     | Submit a form       |
| PUT    | Update data   | Update profile info |
| DELETE | Remove data   | Delete an account   |

---

### **Example Scenario**

1. You type `www.shop.com/products` in your browser.
2. Browser sends an **HTTP GET request** to the server.
3. Server responds with HTML/CSS/JS for the products page.
4. Your browser displays the page.

---

### **HTTP Response Codes**

* **1xx – Informational:** Request received.
* **2xx – Success:** Request successful. (e.g., 200 OK)
* **3xx – Redirection:** Resource moved. (e.g., 301 Moved Permanently)
* **4xx – Client Error:** Problem with request. (e.g., 404 Not Found)
* **5xx – Server Error:** Problem at server. (e.g., 500 Internal Server Error)

---

### **Limitations of HTTP**

* **Not Secure:** Data is sent in plain text → can be intercepted.
* **Stateless:** Doesn’t remember user sessions without extra mechanisms (cookies, sessions).

---
## Here’s a concise list of **HTTP disadvantages**:

1. **No security** – Data is sent in plain text, easy to intercept.
2. **Vulnerable to attacks** – Susceptible to eavesdropping, tampering, and session hijacking.
3. **Stateless** – Doesn’t remember previous interactions; needs cookies/sessions.
4. **No data integrity guarantee** – Data can be corrupted or altered without detection.
5. **Less efficient for large/real-time data** – Not optimized for streaming or multiple simultaneous requests.


✅ **Summary for Exams:**

* HTTP = Communication protocol between browser and server.
* Stateless, request-response model.
* Methods: GET, POST, PUT, DELETE.
* Response codes: 2xx (success), 4xx (client error), 5xx (server error).
* Limitation: Not secure → use HTTPS for encrypted communication.

---
