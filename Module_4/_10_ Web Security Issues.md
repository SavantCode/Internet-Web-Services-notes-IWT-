
---

# **Web Security Issues**

**Definition:**
Web security issues are **vulnerabilities or threats in a website** that can allow hackers to steal data, damage the site, or harm users. Websites are often targeted because they are **public and handle sensitive information** like usernames, passwords, and payment details.

---

## **A. Common Web Security Issues with Simple Examples**

1. **SQL Injection (SQLi)**

   * **What it is:** Hackers insert malicious SQL code into input fields to access or manipulate the database.
   * **Real Example:** Login page asks for username and password. Hacker enters:

     ```
     Username: ' OR '1'='1
     Password: anything
     ```

     This tricks the database into logging in without valid credentials.
   * **Impact:** Unauthorized access to user accounts, personal data theft.

2. **Cross-Site Scripting (XSS)**

   * **What it is:** Hackers inject malicious scripts into web pages, which run in other users’ browsers.
   * **Real Example:** In a blog comment box, someone enters:

     ```html
     <script>alert("Your cookies are stolen")</script>
     ```

     This script can steal login cookies of users visiting the page.
   * **Impact:** Identity theft, session hijacking, spreading malware.

3. **Cross-Site Request Forgery (CSRF)**

   * **What it is:** Tricks a logged-in user into performing actions they didn’t intend.
   * **Real Example:** A user is logged into a banking site. Hacker sends a malicious link:

     ```
     http://bank.com/transfer?amount=1000&to=Hacker
     ```

     When the user clicks, money is transferred without their knowledge.
   * **Impact:** Unauthorized transactions or changes on user accounts.

4. **Phishing Attacks**

   * **What it is:** Fake websites or emails trick users into giving sensitive info.
   * **Real Example:** An email pretending to be from Gmail says: “Your account is suspended. Click here to reactivate.” Users enter their password on the fake page.
   * **Impact:** Password theft, identity fraud, financial loss.

5. **Denial of Service (DoS / DDoS) Attacks**

   * **What it is:** Overloads a website with traffic, making it unavailable.
   * **Real Example:** A popular e-commerce site suddenly crashes because thousands of fake requests flood the server.
   * **Impact:** Website downtime, loss of revenue, frustrated users.

6. **Weak Authentication / Poor Passwords**

   * **What it is:** Easy-to-guess passwords or lack of multi-factor authentication.
   * **Real Example:** A user sets password `123456`. Hacker easily guesses it using brute-force tools.
   * **Impact:** Unauthorized access to accounts, data theft.

7. **Insecure File Uploads**

   * **What it is:** Websites allowing file uploads without proper checks can be exploited.
   * **Real Example:** A forum allows users to upload `.php` files. Hacker uploads malicious code that runs on the server.
   * **Impact:** Complete server compromise, data theft, malware distribution.

8. **Unpatched Software Vulnerabilities**

   * **What it is:** Using outdated CMS, plugins, or server software with known vulnerabilities.
   * **Real Example:** Running an old version of WordPress with a security hole that hackers exploit.
   * **Impact:** Unauthorized access, website defacement, malware injection.

---

## **B. Table of Security Issues with Simple Examples**

| Security Issue        | Simple Example                                  | Impact                            |
| --------------------- | ----------------------------------------------- | --------------------------------- |
| SQL Injection         | Login bypass with `' OR '1'='1`                 | Data theft, unauthorized access   |
| XSS                   | `<script>alert("Hacked")</script>` in a comment | Session hijacking, malware spread |
| CSRF                  | Malicious bank transfer via link                | Unauthorized actions on accounts  |
| Phishing              | Fake Gmail login page                           | Password theft, identity fraud    |
| DoS / DDoS            | Website crashes due to fake traffic floods      | Downtime, revenue loss            |
| Weak Passwords        | Password = `123456`                             | Account compromise                |
| Insecure File Uploads | Uploading `.php` scripts on forums              | Server compromise, malware        |
| Unpatched Software    | Old WordPress version with known exploit        | Hackers exploit vulnerability     |

---

### **C. Key Points to Remember**

1. Web security issues **target data, users, and website functionality**.
2. They often exploit **human error (weak passwords) or technical flaws (XSS, SQLi)**.
3. Proper **validation, strong passwords, updated software, and HTTPS** can prevent most issues.

---
