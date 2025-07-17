<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NOCTIS</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">
                <h1>NOCTIS</h1>
                <p>Dark Mode Elegance</p>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#shop">Shop</a></li>
                    <li><a href="#collections">Collections</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
            <div class="cart-icon">
                <i class="fas fa-shopping-cart"></i>
                <span class="cart-count">0</span>
            </div>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h2>Embrace the Darkness</h2>
            <p>Premium products designed for those who appreciate the night</p>
            <a href="#shop" class="btn">Shop Now</a>
        </div>
    </section>

    <section class="featured-products" id="shop">
        <div class="container">
            <h2 class="section-title">Featured Products</h2>
            <div class="products-grid">
                <!-- Product cards will be added by JavaScript -->
            </div>
        </div>
    </section>

    <section class="collections" id="collections">
        <div class="container">
            <h2 class="section-title">Our Collections</h2>
            <div class="collection-grid">
                <div class="collection-card">
                    <img src="https://via.placeholder.com/400x300/111111/555555?text=Midnight" alt="Midnight Collection">
                    <h3>Midnight</h3>
                    <p>Essentials for the night owl</p>
                </div>
                <div class="collection-card">
                    <img src="https://via.placeholder.com/400x300/222222/555555?text=Obsidian" alt="Obsidian Collection">
                    <h3>Obsidian</h3>
                    <p>Luxury with an edge</p>
                </div>
                <div class="collection-card">
                    <img src="https://via.placeholder.com/400x300/333333/555555?text=Noir" alt="Noir Collection">
                    <h3>Noir</h3>
                    <p>Classic black elegance</p>
                </div>
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <h2 class="section-title">About NOCTIS</h2>
                <p>NOCTIS was born from a love of the night and all its mysteries. We curate products that embody the elegance and sophistication of darkness, offering premium items for those who appreciate the finer things in life.</p>
                <p>Our mission is to provide exceptional quality with a distinctive aesthetic that stands apart from the ordinary.</p>
            </div>
        </div>
    </section>

    <section class="newsletter">
        <div class="container">
            <h3>Join the Night</h3>
            <p>Subscribe to our newsletter for exclusive offers and new arrivals</p>
            <form id="newsletter-form">
                <input type="email" placeholder="Your email address" required>
                <button type="submit" class="btn">Subscribe</button>
            </form>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-col">
                    <h3>NOCTIS</h3>
                    <p>Dark Mode Elegance</p>
                </div>
                <div class="footer-col">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#shop">Shop</a></li>
                        <li><a href="#collections">Collections</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-col">
                    <h4>Contact</h4>
                    <p>contact@noctis.com</p>
                    <p>+1 (555) 123-4567</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 NOCTIS. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* Global Styles */
:root {
    --primary: #0a0a0a;
    --secondary: #1a1a1a;
    --accent: #6d28d9;
    --accent-light: #8b5cf6;
    --text: #f8f8f8;
    --text-secondary: #a1a1aa;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: var(--primary);
    color: var(--text);
    line-height: 1.6;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

.btn {
    display: inline-block;
    background-color: var(--accent);
    color: white;
    padding: 12px 24px;
    border-radius: 4px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    border: none;
    cursor: pointer;
}

.btn:hover {
    background-color: var(--accent-light);
    transform: translateY(-2px);
}

.section-title {
    font-size: 2.5rem;
    margin-bottom: 2rem;
    position: relative;
    display: inline-block;
}

.section-title::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 0;
    width: 60px;
    height: 4px;
    background-color: var(--accent);
}

/* Header Styles */
header {
    background-color: rgba(10, 10, 10, 0.9);
    position: fixed;
    width: 100%;
    z-index: 1000;
    padding: 20px 0;
    backdrop-filter: blur(10px);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo h1 {
    font-size: 2rem;
    font-weight: 700;
    letter-spacing: 2px;
}

.logo p {
    font-size: 0.8rem;
    color: var(--text-secondary);
    letter-spacing: 1px;
}

nav ul {
    display: flex;
    list-style: none;
}

nav ul li {
    margin-left: 30px;
}

nav ul li a {
    color: var(--text);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
    position: relative;
}

nav ul li a:hover {
    color: var(--accent-light);
}

nav ul li a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: var(--accent-light);
    transition: width 0.3s ease;
}

nav ul li a:hover::after {
    width: 100%;
}

.cart-icon {
    position: relative;
    cursor: pointer;
    font-size: 1.2rem;
}

.cart-count {
    position: absolute;
    top: -10px;
    right: -10px;
    background-color: var(--accent);
    color: white;
    border-radius: 50%;
    width: 20px;
    height: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 0.7rem;
    font-weight: bold;
}

/* Hero Section */
.hero {
    height: 100vh;
    background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') no-repeat center center/cover;
    display: flex;
    align-items: center;
    padding-top: 80px;
}

.hero-content {
    max-width: 600px;
}

.hero h2 {
    font-size: 3.5rem;
    margin-bottom: 20px;
    line-height: 1.2;
}

.hero p {
    font-size: 1.2rem;
    margin-bottom: 30px;
    color: var(--text-secondary);
}

/* Products Section */
.featured-products {
    padding: 100px 0;
}

.products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 30px;
}

.product-card {
    background-color: var(--secondary);
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    position: relative;
}

.product-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
}

.product-image {
    height: 300px;
    overflow: hidden;
}

.product-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.product-card:hover .product-image img {
    transform: scale(1.05);
}

.product-info {
    padding: 20px;
}

.product-title {
    font-size: 1.2rem;
    margin-bottom: 10px;
}

.product-price {
    font-size: 1.1rem;
    font-weight: 600;
    color: var(--accent-light);
    margin-bottom: 15px;
}

.product-description {
    color: var(--text-secondary);
    margin-bottom: 15px;
    font-size: 0.9rem;
}

.add-to-cart {
    width: 100%;
    padding: 10px;
    background-color: transparent;
    border: 1px solid var(--accent);
    color: var(--accent);
    border-radius: 4px;
    cursor: pointer;
    transition: all 0.3s ease;
    font-weight: 600;
}

.add-to-cart:hover {
    background-color: var(--accent);
    color: white;
}

/* Collections Section */
.collections {
    padding: 100px 0;
    background-color: var(--secondary);
}

.collection-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
}

.collection-card {
    position: relative;
    height: 400px;
    border-radius: 8px;
    overflow: hidden;
}

.collection-card img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
}

.collection-card:hover img {
    transform: scale(1.05);
}

.collection-card h3 {
    position: absolute;
    bottom: 60px;
    left: 20px;
    font-size: 1.8rem;
}

.collection-card p {
    position: absolute;
    bottom: 30px;
    left: 20px;
    color: var(--text-secondary);
}

/* About Section */
.about {
    padding: 100px 0;
}

.about-content {
    max-width: 800px;
    margin: 0 auto;
    text-align: center;
}

.about-content p {
    margin-bottom: 20px;
    color: var(--text-secondary);
}

/* Newsletter Section */
.newsletter {
    padding: 80px 0;
    background-color: var(--secondary);
    text-align: center;
}

.newsletter h3 {
    font-size: 2rem;
    margin-bottom: 20px;
}

.newsletter p {
    color: var(--text-secondary);
    margin-bottom: 30px;
}

#newsletter-form {
    display: flex;
    max-width: 500px;
    margin: 0 auto;
}

#newsletter-form input {
    flex: 1;
    padding: 15px;
    border: none;
    border-radius: 4px 0 0 4px;
    background-color: var(--primary);
    color: var(--text);
}

#newsletter-form button {
    border-radius: 0 4px 4px 0;
}

/* Footer */
footer {
    background-color: var(--primary);
    padding: 60px 0 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 40px;
    margin-bottom: 40px;
}

.footer-col h4 {
    font-size: 1.2rem;
    margin-bottom: 20px;
    position: relative;
}

.footer-col h4::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 0;
    width: 40px;
    height: 2px;
    background-color: var(--accent);
}

.footer-col ul {
    list-style: none;
}

.footer-col ul li {
    margin-bottom: 10px;
}

.footer-col ul li a {
    color: var(--text-secondary);
    text-decoration: none;
    transition: color 0.3s ease;
}

.footer-col ul li a:hover {
    color: var(--accent-light);
}

.footer-col p {
    color: var(--text-secondary);
    margin-bottom: 15px;
}

.social-icons {
    display: flex;
    gap: 15px;
}

.social-icons a {
    color: var(--text-secondary);
    font-size: 1.2rem;
    transition: color 0.3s ease;
}

.social-icons a:hover {
    color: var(--accent-light);
}

.copyright {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    color: var(--text-secondary);
    font-size: 0.9rem;
}

/* Responsive Styles */
@media (max-width: 768px) {
    header .container {
        flex-direction: column;
        text-align: center;
    }

    nav ul {
        margin-top: 20px;
        justify-content: center;
    }

    nav ul li {
        margin: 0 10px;
    }

    .hero h2 {
        font-size: 2.5rem;
    }

    .section-title {
        font-size: 2rem;
    }

    .footer-grid {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .footer-col h4::after {
        left: 50%;
        transform: translateX(-50%);
    }

    .social-icons {
        justify-content: center;
    }

    #newsletter-form {
        flex-direction: column;
    }

    #newsletter-form input {
        border-radius: 4px;
        margin-bottom: 10px;
    }

    #newsletter-form button {
        border-radius: 4px;
        width: 100%;
    }
}

@media (max-width: 480px) {
    nav ul {
        flex-direction: column;
        align-items: center;
    }

    nav ul li {
        margin: 5px 0;
    }

    .hero h2 {
        font-size: 2rem;
    }

    .hero p {
        font-size: 1rem;
    }
}
// Sample product data
const products = [
    {
        id: 1,
        title: "Midnight Watch",
        price: 299.99,
        description: "Elegant timepiece with luminous hands for nighttime visibility",
        image: "https://via.placeholder.com/400x300/111111/555555?text=Midnight+Watch"
    },
    {
        id: 2,
        title: "Obsidian Bracelet",
        price: 149.99,
        description: "Handcrafted black obsidian stone bracelet",
        image: "https://via.placeholder.com/400x300/222222/555555?text=Obsidian+Bracelet"
    },
    {
        id: 3,
        title: "Noir Sunglasses",
        price: 179.99,
        description: "Premium polarized lenses with matte black frames",
        image: "https://via.placeholder.com/400x300/333333/555555?text=Noir+Sunglasses"
    },
    {
        id: 4,
        title: "Dark Matter Hoodie",
        price: 89.99,
        description: "Ultra-soft hoodie with subtle NOCTIS branding",
        image: "https://via.placeholder.com/400x300/444444/555555?text=Dark+Matter+Hoodie"
    },
    {
        id: 5,
        title: "Eclipse Backpack",
        price: 129.99,
        description: "Water-resistant backpack with hidden compartments",
        image: "https://via.placeholder.com/400x300/555555/555555?text=Eclipse+Backpack"
    },
    {
        id: 6,
        title: "Nightfall Candle",
        price: 34.99,
        description: "Scented candle with notes of sandalwood and amber",
        image: "https://via.placeholder.com/400x300/666666/555555?text=Nightfall+Candle"
    }
];

// Shopping cart functionality
let cart = [];

// DOM elements
const productsGrid = document.querySelector('.products-grid');
const cartCount = document.querySelector('.cart-count');

// Display products
function displayProducts() {
    productsGrid.innerHTML = '';
    
    products.forEach(product => {
        const productCard = document.createElement('div');
        productCard.className = 'product-card';
        
        productCard.innerHTML = `
            <div class="product-image">
                <img src="${product.image}" alt="${product.title}">
            </div>
            <div class="product-info">
                <h3 class="product-title">${product.title}</h3>
                <p class="product-price">$${product.price.toFixed(2)}</p>
                <p class="product-description">${product.description}</p>
                <button class="add-to-cart" data-id="${product.id}">Add to Cart</button>
            </div>
        `;
        
        productsGrid.appendChild(productCard);
    });
    
    // Add event listeners to all "Add to Cart" buttons
    document.querySelectorAll('.add-to-cart').forEach(button => {
        button.addEventListener('click', addToCart);
    });
}

// Add product to cart
function addToCart(e) {
    const productId = parseInt(e.target.getAttribute('data-id'));
    const product = products.find(p => p.id === productId);
    
    // Check if product is already in cart
    const existingItem = cart.find(item => item.id === productId);
    
    if (existingItem) {
        existingItem.quantity += 1;
    } else {
        cart.push({
            ...product,
            quantity: 1
        });
    }
    
    updateCartCount();
    
    // Show feedback
    e.target.textContent = 'Added!';
    e.target.style.backgroundColor = '#10b981';
    setTimeout(() => {
        e.target.textContent = 'Add to Cart';
        e.target.style.backgroundColor = 'transparent';
    }, 1000);
}

// Update cart count display
function updateCartCount() {
    const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
    cartCount.textContent = totalItems;
}

// Newsletter form submission
const newsletterForm = document.getElementById('newsletter-form');
if (newsletterForm) {
    newsletterForm.addEventListener('submit', function(e) {
        e.preventDefault();
        const email = this.querySelector('input').value;
        
        // In a real app, you would send this to your server
        console.log('Subscribed email:', email);
        
        // Show success message
        alert('Thank you for subscribing to NOCTIS!');
        this.reset();
    });
}

// Smooth scrolling for anchor links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
        e.preventDefault();
        
        const targetId = this.getAttribute('href');
        const targetElement = document.querySelector(targetId);
        
        if (targetElement) {
            window.scrollTo({
                top: targetElement.offsetTop - 80,
                behavior: 'smooth'
            });
        }
    });
});

// Initialize the page
document.addEventListener('DOMContentLoaded', () => {
    displayProducts();
    
    // In a real app, you might check localStorage for existing cart
    // cart = JSON.parse(localStorage.getItem('noctis-cart')) || [];
    // updateCartCount();
});