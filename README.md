<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Brand Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }
        header {
            background-color: #333;
            color: white;
            padding: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header .logo {
            font-size: 24px;
            font-weight: bold;
        }
        nav {
            margin-left: auto;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
        }
        .container {
            padding: 20px;
        }
        .product-card {
            border: 1px solid #ddd;
            background: white;
            padding: 15px;
            margin: 10px 0;
            border-radius: 5px;
        }
        .product-card h2 {
            margin: 0 0 10px;
        }
        .product-card p {
            margin: 5px 0;
        }
        .product-card button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        .product-card button:hover {
            background-color: #218838;
        }
        footer {
            background-color: #333;
            color: white;
            padding: 10px;
            text-align: center;
            margin-top: 20px;
        }
        footer a {
            color: #ffc107;
            text-decoration: none;
        }
        .social-icons a {
            margin: 0 5px;
            color: white;
            text-decoration: none;
        }
        .edit-btn {
            float: right;
            margin-top: -40px;
            margin-right: 10px;
            background-color: #ffc107;
            color: black;
            padding: 5px 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">Your Brand</div>
        <nav>
            <a href="#products">Products</a>
            <a href="#services">Services</a>
            <a href="#blog">Blog</a>
            <a href="#ads">Ads</a>
        </nav>
    </header>

    <div class="container">
        <section id="products">
            <h1>Products</h1>
            <div class="product-card">
                <button class="edit-btn">Edit</button>
                <h2>Product Name</h2>
                <p>Description of the product goes here.</p>
                <p><strong>Price:</strong> $100</p>
                <button onclick="placeOrder('Product Name', '$100')">Buy Now</button>
            </div>
        </section>

        <section id="services">
            <h1>Services</h1>
            <div class="product-card">
                <button class="edit-btn">Edit</button>
                <h2>Service Name</h2>
                <p>Description of the service goes here.</p>
                <button onclick="placeOrder('Service Name', 'Contact for pricing')">Order Now</button>
            </div>
        </section>

        <section id="blog">
            <h1>Blog</h1>
            <p>Space for blog content goes here.</p>
        </section>

        <section id="ads">
            <h1>Advertisements</h1>
            <p>Space for ads goes here.</p>
        </section>
    </div>

    <footer>
        <p>Business Address: 123 Printing Lane, Nigeria</p>
        <p>Email: <a href="mailto:FBIintelligence123@gmail.com">FBIintelligence123@gmail.com</a></p>
        <p class="social-icons">
            <a href="#">Facebook</a> | <a href="#">Twitter</a> | <a href="#">Instagram</a>
        </p>
        <p><a href="https://wa.me/2349054665813" target="_blank">Chat with us on WhatsApp</a></p>
    </footer>

    <script>
        function placeOrder(item, price) {
            const name = prompt("Enter your name:");
            const address = prompt("Enter your address:");
            const description = `Order for: ${item}\nPrice: ${price}\nName: ${name}\nAddress: ${address}`;
            alert("Order placed successfully!");

            // Redirect to WhatsApp
            const whatsappUrl = `https://wa.me/2349054665813?text=${encodeURIComponent(description)}`;
            window.open(whatsappUrl, "_blank");
        }
    </script>
</body>
</html>
