    

---

# **Configuring Web Servers**

---

## **1. Introduction**

* **Web Server Configuration** refers to the process of setting up a server to **host websites, handle requests, and serve content efficiently and securely**.
* Proper configuration ensures **performance, security, and scalability**.
* Common web servers: **Apache, IIS, Nginx**.

---

## **2. Configuring Apache Web Server**

**Installation:**

* Linux: `sudo apt install apache2`
* Windows: Use **XAMPP** or **WAMP**.

**Key Configuration Files:**

1. `httpd.conf` – Main server configuration.
2. `.htaccess` – Directory-level settings.
3. `sites-available` / `sites-enabled` – Manage multiple websites (virtual hosts).

**Important Steps:**

1. **Set DocumentRoot** – Folder containing website files.
2. **Configure Virtual Hosts** – Host multiple websites on same server.

   ```apache
   <VirtualHost *:80>
       ServerName example.com
       DocumentRoot /var/www/example
   </VirtualHost>
   ```
3. **Enable Modules** – PHP, SSL, Rewrite.
4. **Configure Security** – Password protection, HTTPS, IP restrictions.
5. **Logging** – Define error and access log locations.
6. **Restart Apache** – Apply changes: `sudo systemctl restart apache2`.

**Key Directives:**

| Directive    | Purpose                  |
| ------------ | ------------------------ |
| DocumentRoot | Path to website files    |
| Listen       | Port number (usually 80) |
| ServerName   | Domain name or hostname  |
| ErrorLog     | Path for error logs      |
| CustomLog    | Path for access logs     |

---

## **3. Configuring IIS (Internet Information Services)**

**Installation:**

* Control Panel → Programs → Turn Windows Features on/off → Enable IIS.

**Steps to Configure a Website:**

1. **Add a Website:**

   * Open IIS Manager → Right-click Sites → Add Website.
   * Enter **Site Name, Physical Path, Port (80 or 443)**.

2. **Assign Application Pool:**

   * Each website runs in its own application pool for **stability and isolation**.

3. **Configure Security:**

   * Enable SSL for HTTPS.
   * Set Authentication: Anonymous, Windows, Basic.
   * Restrict access by IP if required.

4. **Enable Logging & Monitoring:**

   * Logs saved in `C:\inetpub\logs\LogFiles`.
   * Monitor website requests and performance using IIS Manager.

---

## **4. Important Configuration Tips**

* **Virtual Hosts / Multiple Sites:** Host several sites on one server using virtual hosts (Apache) or separate application pools (IIS).
* **Security:** Always enable **HTTPS**, use authentication, and filter unsafe requests.
* **Performance:** Enable caching for static content, optimize modules.
* **Backup Configurations:** Keep backup copies of `httpd.conf` or `applicationHost.config` before making changes.

---

## **5. Mini Exam Diagram**

```
Browser
   |
HTTP Request
   |
Web Server (Apache / IIS)
   |
Configuration (Virtual Host / App Pool)
   |
Website / Web Application
   |
Response to Browser
```

---

### **Summary Table (for 20-mark answers)**

| Server | Key Config Files                       | Steps to Configure                                       | Security                             | Logging              |
| ------ | -------------------------------------- | -------------------------------------------------------- | ------------------------------------ | -------------------- |
| Apache | httpd.conf, .htaccess, sites-available | Set DocumentRoot, Virtual Hosts, Enable Modules, Restart | HTTPS, Passwords, IP restrictions    | ErrorLog, CustomLog  |
| IIS    | applicationHost.config, web.config     | Add Website, Assign App Pool, Configure Security         | SSL, Authentication, IP restrictions | Logs in inetpub\logs |

---
