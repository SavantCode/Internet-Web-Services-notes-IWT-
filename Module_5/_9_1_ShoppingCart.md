Ah, yes! For **exam purposes**, we can make it even **shorter and simpler**, just to demonstrate the concept of a shopping cart. No need for sessions or multiple files.

Here’s a **minimal example** you can write quickly:

---

## **Simplest PHP Shopping Cart Example**

```php
<!DOCTYPE html>
<html>
<head>
    <title>Simple Shopping Cart</title>
</head>
<body>
    <h1>Products</h1>
    <?php
    $products = ["Apple" => 50, "Banana" => 20, "Orange" => 30];

    echo "<ul>";
    foreach($products as $name => $price){
        echo "<li>$name - Rs $price</li>";
    }
    echo "</ul>";

    // Example of adding to cart (simplified)
    echo "<p>Example: Add Apple to cart → Cart has Apple (Qty 1)</p>";
    ?>
</body>
</html>
```
## Output:

```
=========================
       Simple Shopping Cart
=========================

Products
--------
- Apple - Rs 50
- Banana - Rs 20
- Orange - Rs 30

Example: Add Apple to cart → Cart has Apple (Qty 1)
```

This represents:

* **Heading** (Simple Shopping Cart)
* **List of products with prices**
* **Sample cart action message**

---
