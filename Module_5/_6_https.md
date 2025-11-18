

---

## **HTTPS (HyperText Transfer Protocol Secure)**

**Definition:**
HTTPS is a **secure version of HTTP**. It encrypts the data exchanged between the **web browser (client)** and the **web server** using **SSL/TLS protocols**, making it safe from eavesdropping, tampering, or theft.

In simple words:

> HTTPS = HTTP + Security

---

### **Key Features of HTTPS**

1. **Encryption:**

   * Data sent between browser and server is **encrypted**, so attackers cannot read sensitive information like passwords or credit card numbers.
   * Example: When you submit a payment form on `https://www.amazon.com`, your card details are encrypted.

2. **Authentication:**

   * Confirms that the website is **genuine** and not a fake (prevents phishing).
   * Achieved via **SSL/TLS certificates** issued by trusted authorities.

3. **Data Integrity:**

   * Ensures data is **not altered or corrupted** during transmission.

4. **Uses TCP Port 443** (HTTP uses port 80).

---

### **HTTPS vs HTTP**

| Feature         | HTTP                   | HTTPS                            |
| --------------- | ---------------------- | -------------------------------- |
| Security        | No encryption          | Encrypted using SSL/TLS          |
| Port            | 80                     | 443                              |
| Data Protection | Vulnerable to attacks  | Secure from eavesdropping        |
| Authentication  | None                   | Website identity verified        |
| Typical Use     | Informational websites | Banking, e-commerce, login pages |

---

### **How HTTPS Works (Simplified)**

1. Browser connects to a website (HTTPS).
2. Server sends its **SSL/TLS certificate**.
3. Browser verifies the certificate.
4. A **secure encrypted connection** is established.
5. Data (like login info, payments) is transmitted securely.

---

### **Example Scenario**

* Visiting `https://www.gmail.com`:

  * All emails you send and receive are encrypted.
  * Hackers cannot intercept your messages even if they access the network.

---

### **Advantages of HTTPS**

1. Secure transmission of sensitive data.
2. Builds **trust with users** (shows padlock icon in browsers).
3. Helps in **SEO ranking** – Google prefers HTTPS sites.
4. Prevents **man-in-the-middle attacks**.

---

### **HTTP Response Codes Recap**

* HTTPS still uses the **same HTTP response codes** as HTTP:

  * **2xx:** Success (200 OK)
  * **3xx:** Redirection (301 Moved Permanently)
  * **4xx:** Client Error (404 Not Found)
  * **5xx:** Server Error (500 Internal Server Error)

---

✅ **Exam Tip:**

* Remember: **HTTPS = HTTP + SSL/TLS**
* **HTTP → insecure, HTTPS → secure**
* Look for **padlock icon** in browsers to verify HTTPS.

---
