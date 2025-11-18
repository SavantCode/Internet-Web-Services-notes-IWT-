
---

### **1️⃣ SSL vs HTTPS (Which is more secure?)**

* **SSL (Secure Sockets Layer):**

  * A protocol that **encrypts data** exchanged between a browser and server.
  * Ensures **confidentiality** (data cannot be read by attackers) and **integrity** (data is not altered in transit).

* **HTTPS (HyperText Transfer Protocol Secure):**

  * HTTP running **over SSL/TLS**, making the communication secure.
  * Protects data like **passwords, credit card info, and personal details**.

**Key Point:**

* **HTTPS is more practical and secure** for websites because it **actually implements SSL/TLS encryption** in web communication.
* SSL alone is just the encryption standard; HTTPS is what users see in browsers as the secure protocol.

*Example:*

* Banking websites always use **HTTPS**, showing a padlock icon in the browser → Ensures secure transactions.
* HTTP sites (without HTTPS) can be hacked with **data interception**.

---

### **2️⃣ HTTPS / HTTP Response Codes**

* These are **codes sent by a web server** to indicate the result of a user’s request.
* Helps **users and developers understand what happened** with the request.

**Common Response Codes:**

| Code | Meaning                    | Example/Use Case                                         |
| ---- | -------------------------- | -------------------------------------------------------- |
| 200  | OK – Request succeeded     | Page loaded successfully                                 |
| 301  | Moved Permanently          | URL permanently changed, browser redirects automatically |
| 302  | Found / Temporary Redirect | Temporary redirect to another page                       |
| 400  | Bad Request                | User sent invalid data                                   |
| 401  | Unauthorized               | Login required to access page                            |
| 403  | Forbidden                  | Access denied, even if logged in                         |
| 404  | Not Found                  | Page doesn’t exist                                       |
| 500  | Internal Server Error      | Server encountered a problem                             |
| 503  | Service Unavailable        | Server temporarily down                                  |

*Example:*

* Typing the wrong URL → **404 Not Found**
* Server working normally → **200 OK**
* Redirecting old URL → **301 Moved Permanently**

---
