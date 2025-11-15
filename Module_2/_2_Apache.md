

---

# **Apache Web Server **

---

## **1. Introduction to Apache**

**Definition:**

* Apache HTTP Server is a **free, open-source web server software** developed by the **Apache Software Foundation**.
* It is one of the **most widely used web servers in the world**.
* Runs on **Linux, Windows, MacOS**, and supports a variety of programming languages (PHP, Python, Perl, etc.).

**History:**

* Released in **1995**.
* The name “Apache” comes from **“a patchy server”**, because it started as a series of patches to the NCSA HTTPd web server.

**Purpose:**

* To **serve web pages and web applications** to clients over **HTTP/HTTPS**.

---

## **2. Key Features of Apache**

1. **Cross-Platform Support**

   * Works on Linux, Windows, and MacOS.

2. **Open Source & Free**

   * No license fee; source code available for modification.

3. **Module-Based Architecture**

   * Core server + optional modules (for SSL, PHP, caching, authentication).
   * Example modules: `mod_ssl` (HTTPS), `mod_rewrite` (URL rewriting).

4. **Support for Dynamic Content**

   * Can execute server-side scripts (PHP, Perl, Python).

5. **Virtual Hosting**

   * Host multiple websites/domains on a single server.

6. **Security Features**

   * Supports authentication, SSL/TLS encryption, access control, IP blocking.

7. **Logging & Monitoring**

   * Access logs and error logs for **tracking server activity**.

8. **Caching Support**

   * Speeds up content delivery by storing **frequently accessed pages**.

9. **Flexible URL Management**

   * Can rewrite URLs, redirect pages, and handle custom error pages.

---

## **3. Apache Architecture**

Apache has a **modular architecture** consisting of:

1. **Core Server**

   * Handles basic HTTP request/response operations.

2. **Multi-Processing Modules (MPMs)**

   * Determines how Apache handles multiple requests.
   * Common MPMs:

     * `prefork` – multiple processes (no threading), good for stability.
     * `worker` – multi-threaded, efficient for high traffic.

3. **Modules**

   * Extend functionality:

     * **mod_ssl** → HTTPS support
     * **mod_rewrite** → URL rewriting
     * **mod_proxy** → proxy/gateway support
     * **mod_headers** → manage HTTP headers

4. **Configuration Files**

   * `httpd.conf` → main configuration file
   * `.htaccess` → per-directory configuration

5. **Logging System**

   * `access.log` → records every request
   * `error.log` → records server errors

---

## **4. Installation of Apache**

**Linux (Ubuntu example):**

```bash
sudo apt update
sudo apt install apache2
```

**Windows:**

* Use **XAMPP** or **WAMP** packages.

**Start & Stop Server:**

* Linux:

  ```bash
  sudo systemctl start apache2
  sudo systemctl stop apache2
  sudo systemctl restart apache2
  ```
* Windows: Use **XAMPP/WAMP control panel**.

---

## **5. Apache Configuration Basics**

**Key Configuration Parameters (httpd.conf):**

| Directive      | Purpose                               |
| -------------- | ------------------------------------- |
| `DocumentRoot` | Folder where website files are stored |
| `Listen`       | Port number (default 80 for HTTP)     |
| `ServerName`   | Hostname of server (e.g., localhost)  |
| `LoadModule`   | Loads a module (PHP, SSL, etc.)       |
| `<Directory>`  | Access rules for a folder             |
| `ErrorLog`     | Location of error log file            |
| `CustomLog`    | Location of access log file           |

**.htaccess File:**

* A **directory-level configuration file** for:

  * URL rewriting
  * Password protection
  * Custom error pages
  * Redirection

**Example (.htaccess):**

```apache
# Redirect all HTTP to HTTPS
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}/$1 [R=301,L]
```

---

## **6. Advantages of Apache**

1. **Open-source and free** → cost-effective.
2. **Highly configurable** with modules and `.htaccess`.
3. **Cross-platform** → works on Linux, Windows, Mac.
4. **Secure** → supports SSL/TLS encryption and authentication.
5. **Supports multiple languages** → PHP, Perl, Python, etc.
6. **Reliable and widely used** → large community and documentation.
7. **Virtual hosting support** → multiple websites on one server.

---

## **7. Common Use Cases**

1. Hosting **personal or corporate websites**.
2. Running **web applications** (PHP, Python, Node.js).
3. Serving **static content** like HTML, CSS, images.
4. Acting as a **reverse proxy** or load balancer.
5. Educational purposes – learning web technologies and server management.

---

## **8. Mini Example for Exam Notes**

**Apache Folder Structure (Linux typical):**

```
/etc/apache2/
   ├── apache2.conf      # main config
   ├── sites-available/  # websites config
   ├── sites-enabled/    # enabled websites
   ├── mods-available/   # modules
   └── mods-enabled/     # active modules
/var/www/html/            # default website files
```

**Request Flow Diagram:**

```
Browser ----HTTP Request---> Apache Web Server ----> Fetch File/Run Script ----HTTP Response---> Browser
```

---

## **9. Exam Tips (10–15 Marks)**

* Define Apache clearly (open-source, HTTP server).
* Explain **features and modular architecture**.
* Mention **installation & configuration basics**.
* Include **advantages and use cases**.
* Draw a **mini diagram of request-response flow**.

---
