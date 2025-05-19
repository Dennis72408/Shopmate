# Shopmate
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce Website</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 1rem;
        }
        nav ul {
            list-style-type: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin-right: 1rem;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
        }
        main {
            padding: 1rem;
        }
        .product-list {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
        }
        .product-item {
            border: 1px solid #ddd;
            padding: 1rem;
            width: 200px;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 1rem;
            margin-top: 1rem;
        }
    </style>
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const cartSection = document.querySelector("#cart p");
            const buttons = document.querySelectorAll(".product-item button");
            let cart = [];

            buttons.forEach((button, index) => {
                button.addEventListener("click", () => {
                    const productName = button.parentElement.querySelector("h3").textContent;
                    cart.push(productName);
                    cartSection.textContent = "Items in cart: " + cart.length;
                    alert(productName + " added to cart!");
                });
            });
        });
    </script>
</head>
<body>
    <header>
        <nav>
            <h1>ShopMate</h1>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#cart">Cart</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home">
            <h2>Welcome to ShopMate</h2>
            <p>Your one-stop shop for the latest products.</p>
        </section>

        <section id="products">
            <h2>Our Products</h2>
            <div class="product-list">
                <div class="product-item">
                    <h3>Product 1</h3>
                    <p>Price: $10</p>
                    <button>Add to Cart</button>
                </div>
                <div class="product-item">
                    <h3>Product 2</h3>
                    <p>Price: $20</p>
                    <button>Add to Cart</button>
                </div>
            </div>
        </section>

        <section id="cart">
            <h2>Your Cart</h2>
            <p>No items in cart.</p>
        </section>

        <section id="contact">
            <h2>Contact Us</h2>
            <form>
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                <textarea placeholder="Your message"></textarea>
                <button type="submit">Send</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 ShopMate. All rights reserved.</p>
    </footer>
</body>
</html>
