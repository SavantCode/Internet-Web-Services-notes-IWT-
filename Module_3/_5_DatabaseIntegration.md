
---

# 🌐 **Database Integration in Web Development**

**Definition:**
Database integration means **connecting a web application (like a website) to a database** so that it can **store, retrieve, update, and delete data** dynamically.

* Without a database, websites are **static** (fixed content).
* With database integration, websites become **dynamic** (interactive, data-driven).

---

## **1️⃣ Why Integrate a Database?**

* To **store user information** (like login details, registrations).
* To **display dynamic content** (like blog posts, product catalogs).
* To **manage large data** efficiently.
* To allow **CRUD operations**:

  * **C**reate → Add new data
  * **R**ead → Fetch/display data
  * **U**pdate → Modify data
  * **D**elete → Remove data

---

## **2️⃣ Common Databases Used in Web Development**

| Database   | Type       | Notes                                      |
| ---------- | ---------- | ------------------------------------------ |
| MySQL      | Relational | Popular, open-source, widely used with PHP |
| PostgreSQL | Relational | Open-source, advanced features             |
| SQLite     | Relational | Lightweight, file-based                    |
| MongoDB    | NoSQL      | Stores data in JSON-like format, flexible  |

---

## **3️⃣ Steps for Database Integration**

1. **Create a Database**

   * Example: `CREATE DATABASE university;`
   * Inside the database, create **tables** to store structured data.

2. **Connect the Website to the Database**

   * Use a **server-side scripting language** like **PHP, Python, or Node.js**.

   **Example using PHP:**

   ```php
   <?php
   $servername = "localhost";
   $username = "root";
   $password = "";
   $dbname = "university";

   // Create connection
   $conn = new mysqli($servername, $username, $password, $dbname);

   // Check connection
   if ($conn->connect_error) {
       die("Connection failed: " . $conn->connect_error);
   }
   echo "Connected successfully";
   ?>
   ```

3. **Perform CRUD Operations**

   * **Create:** `INSERT INTO students (name, age) VALUES ('Anushka', 20);`
   * **Read:** `SELECT * FROM students;`
   * **Update:** `UPDATE students SET age=21 WHERE name='Anushka';`
   * **Delete:** `DELETE FROM students WHERE name='Anushka';`

4. **Display Data on Web Pages**

   * Use server-side code to **fetch data from database** and **display in HTML**.

   **Example (PHP + HTML):**

   ```php
   <?php
   $result = $conn->query("SELECT * FROM students");
   while($row = $result->fetch_assoc()) {
       echo "<p>Name: " . $row["name"] . ", Age: " . $row["age"] . "</p>";
   }
   ?>
   ```

---

## **4️⃣ Key Points**

* Database integration allows **dynamic websites**.
* Requires **server-side scripting** (PHP, Python, Node.js).
* CRUD operations are the **core of database interaction**.
* **Security measures** like input validation and prepared statements are crucial to prevent **SQL injection attacks**.

---

## **5️⃣ Example Use Cases**

| Use Case                 | How Database Helps                        |
| ------------------------ | ----------------------------------------- |
| Online Registration Form | Stores user info in a database            |
| E-commerce Website       | Stores product details, prices, inventory |
| Blog Website             | Saves and fetches blog posts dynamically  |
| Login System             | Checks username/password in database      |

---

💡 **Simple Analogy:**

Think of the **website as a shop** and the **database as a storage room**:

* Website displays products (data) to customers.
* Database stores all the products.
* Server-side code is like the shopkeeper fetching and updating items.

---


## **Database Integration**

**Definition:**
Database integration refers to the process of **connecting a website to a database** so that it can **store, retrieve, update, and delete data dynamically**. This allows web applications to become interactive and responsive to user actions.

**Importance:**

* Makes web pages **dynamic instead of static**.
* Enables storage of user information, product details, orders, and other data.
* Facilitates data management in applications like e-commerce, social media, and content management systems.

---

## **Connecting Web Pages to Databases**

**Concept:**

* Web pages by themselves cannot store data permanently.
* **Server-side scripting languages** like **PHP, ASP.NET, JSP** are used to connect web pages to databases.
* The server-side script acts as a **bridge** between the web page and the database: it sends SQL queries to the database and retrieves the results to display on the webpage.

**Example (PHP connecting to MySQL):**

```php
<?php
$conn = mysqli_connect("localhost", "root", "", "school");
if(!$conn){
    die("Connection failed: " . mysqli_connect_error());
}
echo "Connected successfully";
?>
```

**Explanation:**

* `localhost` → Database server address
* `root` → Database username
* `school` → Database name

---

## **Server-side Scripting and Database Interaction**

**Definition:**
Server-side scripts are programs executed on the server that allow a web page to interact with a database.

**Popular server-side languages:**

* **PHP** – works well with MySQL
* **ASP.NET** – works with SQL Server or Oracle

**Function:**

* Receive user input from a web page
* Process the input and perform database operations
* Return results to the web page

**Example:** Displaying data from a table:

```php
$result = mysqli_query($conn, "SELECT * FROM students");
while($row = mysqli_fetch_assoc($result)){
    echo $row['name'] . " - " . $row['class'] . "<br>";
}
```

---

## **Basic CRUD Operations**

CRUD refers to the four basic operations performed on database data:

1. **Create:** Add new data

```php
INSERT INTO students (name, class) VALUES('Ali', '10');
```

2. **Read:** Retrieve data

```php
SELECT * FROM students;
```

3. **Update:** Modify existing data

```php
UPDATE students SET class='11' WHERE name='Ali';
```

4. **Delete:** Remove data

```php
DELETE FROM students WHERE name='Ali';
```

**Explanation:**

* These operations are performed using **SQL queries** executed by server-side scripts.
* They form the foundation of dynamic web applications.

---

## **Example Databases**

1. **MySQL:**

* Free and open-source.
* Widely used in small to medium-scale web applications.
* Works efficiently with PHP.

2. **Oracle:**

* Powerful and robust.
* Supports large-scale enterprise applications.
* Provides advanced features for complex queries and data management.

---

## **Web Page – Database Interaction Workflow**

1. User submits data on a web page.
2. Server-side script processes the data.
3. Script sends a query to the database.
4. Database executes the query and returns results.
5. Server-side script displays results on the web page.

**Example workflow diagram (textual for exam):**

```
Web Page → Server Script (PHP/ASP.NET) → Database (MySQL/Oracle) → Web Page
```

---

```
          +----------------+
          |   Web Page     |
          | (HTML / Forms) |
          +--------+-------+
                   |
                   | User input / request
                   v
          +----------------+
          | Server Script  |
          | (PHP / ASP.NET)|
          +--------+-------+
                   |
                   | SQL Query
                   v
          +----------------+
          |   Database     |
          | (MySQL/Oracle) |
          +----------------+
                   |
                   | Query Result
                   v
          +----------------+
          |   Web Page     |
          | (Display Data) |
          +----------------+



```

Sure! Let’s explain **Server-side Scripting and Database Interaction** in a **simple and detailed way** for your exams.

---

# 🌐 **Server-side Scripting and Database Interaction**

**Definition:**
Server-side scripting is when **code runs on the web server** instead of the user’s browser. It is used to **handle requests, process data, and interact with databases**.

Database interaction allows the server to **store, retrieve, update, and delete data** in a database based on user actions.

---

## **1️⃣ How It Works**

1. **User Requests a Page**

   * Example: User submits a form on a website.

2. **Server-side Script Executes**

   * Languages like **PHP, Python, Node.js, ASP.NET** run on the server.

3. **Database Interaction Happens**

   * Script communicates with the database to **fetch or store data**.

4. **Server Sends Response**

   * The processed data is sent back as **HTML, JSON, or other formats** to the user’s browser.

**Diagram (Simple Workflow):**

```
User → Browser → Server-side Script → Database → Script processes → Browser displays result
```

---

## **2️⃣ Common Server-side Languages**

| Language | Notes                              |
| -------- | ---------------------------------- |
| PHP      | Popular, works well with MySQL     |
| Python   | Often used with Django or Flask    |
| Node.js  | JavaScript runtime for server-side |
| ASP.NET  | Microsoft framework                |

---

## **3️⃣ Server-side Scripting with Database Example**

**Scenario:** Display a list of students from a database using **PHP and MySQL**.

**Step 1: Connect to Database**

```php
<?php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "university";

$conn = new mysqli($servername, $username, $password, $dbname);

if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>
```

**Step 2: Fetch Data**

```php
<?php
$sql = "SELECT * FROM students";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    while($row = $result->fetch_assoc()) {
        echo "Name: " . $row["name"] . " - Age: " . $row["age"] . "<br>";
    }
} else {
    echo "No records found";
}
$conn->close();
?>
```

---

## **4️⃣ CRUD Operations Using Server-side Scripting**

| Operation  | Example SQL                                             | Purpose       |
| ---------- | ------------------------------------------------------- | ------------- |
| **Create** | `INSERT INTO students(name, age) VALUES('Anushka', 20)` | Add new data  |
| **Read**   | `SELECT * FROM students`                                | Retrieve data |
| **Update** | `UPDATE students SET age=21 WHERE name='Anushka'`       | Modify data   |
| **Delete** | `DELETE FROM students WHERE name='Anushka'`             | Remove data   |

---

## **5️⃣ Benefits**

* Dynamic content on websites
* Real-time updates
* Data-driven web applications (login systems, e-commerce, blogs)
* Secure data management (data never exposed directly to the user)

---

💡 **Tip for Exams:**

* Remember the flow: **Browser → Server-side script → Database → Script processes → Browser**
* Always mention **CRUD operations** when asked about database interaction.
* Example snippets with PHP + MySQL are usually safe for reference.

---
