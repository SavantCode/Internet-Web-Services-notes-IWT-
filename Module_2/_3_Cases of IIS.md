
---

# **Case Study: IIS (Internet Information Services)**

---

## **1. Introduction**

* **IIS (Internet Information Services)** is a **web server software developed by Microsoft**.
* It is designed to **host websites, web applications, and services** on **Windows Server operating systems**.
* IIS can serve both **static content (HTML, images)** and **dynamic content (ASP.NET, PHP, etc.)**.
* First released with **Windows NT 3.51**, IIS has evolved over many versions and is integrated with Windows Server.

**Purpose:**

* To provide a **secure, reliable, and high-performance platform** for hosting web applications.

---

## **2. Key Features of IIS**

1. **Windows Integration:**

   * Fully integrated with Windows Server, supports **Active Directory** for authentication.

2. **Dynamic Content Support:**

   * Can execute **ASP.NET, PHP, CGI scripts**, and other dynamic content.

3. **Application Pools:**

   * Each website or application runs in its **isolated application pool**, improving **stability and security**.

4. **Security Features:**

   * SSL/TLS encryption for HTTPS
   * IP address restrictions
   * Authentication modes: Anonymous, Windows, Basic, Digest

5. **Logging & Diagnostics:**

   * Detailed logging of requests and errors.
   * Provides **monitoring tools** to track server performance.

6. **FTP Support:**

   * Can host FTP sites alongside HTTP/HTTPS content.

7. **Scalability & Performance:**

   * Optimized to handle **large numbers of simultaneous requests**.
   * Supports **caching of static content**.

---

## **3. Architecture of IIS**

IIS uses a **modular and layered architecture**:

1. **HTTP.sys Kernel Mode Driver:**

   * Receives requests from clients and forwards them to IIS.

2. **IIS Worker Processes (w3wp.exe):**

   * Handles requests for each application pool.
   * Executes dynamic content like ASP.NET.

3. **Application Pools:**

   * Isolate websites to prevent one application from affecting another.

4. **Web Applications and Sites:**

   * Each site has its own **physical folder**, configuration, and application pool.

5. **Configuration Store (IIS Manager & XML config files):**

   * Settings stored in `applicationHost.config` and `web.config`.

**Diagram:**

```
Browser Request
     |
  HTTP.sys (Kernel Mode)
     |
IIS Worker Process (w3wp.exe)
     |
Application Pool
     |
Website / Web App
     |
Response to Browser
```

---

## **4. Configuring IIS**

**Step 1: Install IIS**

* Control Panel → Programs → Turn Windows Features on/off → Enable **Internet Information Services**.

**Step 2: Add a Website**

* Open **IIS Manager → Sites → Add Website**
* Enter:

  * **Site Name:** e.g., MyWebsite
  * **Physical Path:** Folder containing web files
  * **Port:** 80 (HTTP) or 443 (HTTPS)

**Step 3: Configure Application Pool**

* Assign a dedicated **application pool** to each website.
* Choose .NET version and pipeline mode.

**Step 4: Configure Security**

* Enable SSL if needed.
* Set authentication mode (Anonymous, Windows, Basic).
* Restrict access by IP if required.

**Step 5: Logging & Monitoring**

* IIS logs requests and errors in `C:\inetpub\logs\LogFiles`.
* Use **IIS Manager** to monitor performance and request statistics.

---

## **5. Advantages of IIS**

1. Integrated with Windows environment → easy management.
2. Supports dynamic content (.NET, PHP) and static content (HTML, CSS).
3. Application pools improve **stability and security**.
4. Easy to configure using **GUI (IIS Manager)**.
5. Secure and scalable → supports HTTPS and multiple websites.
6. Built-in logging and diagnostic tools for monitoring.

---

## **6. Use Cases of IIS**

1. Hosting **corporate websites** using ASP.NET and MS SQL Server.
2. Running **internal enterprise applications** with secure access.
3. Hosting **multiple websites** on a single Windows server using application pools.
4. Providing **FTP services** alongside HTTP content.
5. Serving web services for **Windows-based applications**.

---

## **7. Security Features**

* **SSL/TLS Encryption:** Protects data in transit.
* **Authentication:** Anonymous, Basic, Windows, Digest.
* **IP Restrictions:** Allow or block specific IP addresses.
* **Request Filtering:** Blocks unsafe requests to prevent attacks.
* **Application Pool Isolation:** Prevents one site from crashing others.

---

## **8. Summary for 20 Marks Exam**

| Topic         | Key Points                                                                          |
| ------------- | ----------------------------------------------------------------------------------- |
| Definition    | IIS is a Microsoft web server for hosting websites and web apps                     |
| Features      | Dynamic content, application pools, security, logging, FTP, caching                 |
| Architecture  | HTTP.sys → Worker Process → Application Pool → Website                              |
| Configuration | Install IIS → Add Website → Assign Application Pool → Configure Security → Logging  |
| Advantages    | Integrated with Windows, secure, stable, scalable, supports dynamic content         |
| Use Cases     | Corporate websites, internal apps, multiple websites, FTP, web services             |
| Security      | SSL, authentication, IP restrictions, request filtering, application pool isolation |

**Mini Diagram for Exams:**

```
Browser
   |
HTTP.sys (Kernel Mode)
   |
IIS Worker Process (w3wp.exe)
   |
Application Pool
   |
Website / Web Application
   |
Response to Browser
```

---

This note is **detailed, theoretical, and exam-friendly**, covering **definition, features, architecture, configuration, advantages, use cases, and security**. It can easily fetch **20 marks** in your theory exam.

---
