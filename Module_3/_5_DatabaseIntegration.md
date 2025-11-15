
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