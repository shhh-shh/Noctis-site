<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Noctis - Find the best deals on electronics, home goods, and more. Save money with our exclusive affiliate offers.">
    <meta name="keywords" content="deals, discounts, affiliate, shopping, save money">
    <title>Noctis - Best Deals Online</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="logo">Noctis</div>
        
        <!-- Search Bar -->
        <div class="search-container">
            <input type="text" placeholder="Search products..." id="search-input">
            <button id="search-button">Search</button>
        </div>
        
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="#" onclick="filterProducts('electronics')">Electronics</a></li>
                <li><a href="#" onclick="filterProducts('home')">Home</a></li>
                <li><a href="#" onclick="filterProducts('fashion')">Fashion</a></li>
            </ul>
        </nav>
        
        <div class="user-actions" id="user-actions">
            <!-- Will be filled by JavaScript -->
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section class="hero">
            <h1>Welcome to Noctis!</h1>
            <p>Your one-stop shop for the best deals online</p>
            
            <!-- Newsletter Signup -->
            <div class="newsletter">
                <h3>Get exclusive deals!</h3>
                <input type="email" placeholder="Your email address" id="newsletter-email">
                <button onclick="subscribeNewsletter()">Subscribe</button>
                <p id="newsletter-message" class="newsletter-message"></p>
            </div>
        </section>

        <!-- Product Categories -->
        <section class="categories">
            <h2>Shop by Category</h2>
            <div class="category-grid">
                <div class="category-card" onclick="filterProducts('electronics')">
                    <img src="https://m.media-amazon.com/images/I/61L1ItFgFHL._AC_UF1000,1000_QL80_.jpg" alt="Electronics">
                    <h3>Electronics</h3>
                </div>
                <div class="category-card" onclick="filterProducts('home')">
                    <img src="https://m.media-amazon.com/images/I/71VOYf6SHDL._AC_UF1000,1000_QL80_.jpg" alt="Home">
                    <h3>Home</h3>
                </div>
                <div class="category-card" onclick="filterProducts('fashion')">
                    <img src="https://m.media-amazon.com/images/I/61-8GlaVQ5L._AC_UF1000,1000_QL80_.jpg" alt="Fashion">
                    <h3>Fashion</h3>
                </div>
                <div class="category-card" onclick="filterProducts('all')">
                    <img src="https://m.media-amazon.com/images/I/71XPG5QPddL._AC_UF1000,1000_QL80_.jpg" alt="All Products">
                    <h3>All Products</h3>
                </div>
            </div>
        </section>

        <!-- Products Section -->
        <section class="products">
            <h2>Featured Products</h2>
            <div class="product-grid" id="product-container">
                <!-- Products will be added by JavaScript -->
            </div>
        </section>
    </main>

    <!-- Payment Methods -->
    <section class="payment-methods">
        <h2>We Accept</h2>
        <div class="payment-icons">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Visa_Inc._logo.svg/2560px-Visa_Inc._logo.svg.png" alt="Visa">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Mastercard-logo.svg/1280px-Mastercard-logo.svg.png" alt="Mastercard">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/30/American_Express_logo.svg/1200px-American_Express_logo.svg.png" alt="American Express">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/PayPal.svg/1200px-PayPal.svg.png" alt="PayPal">
        </div>
    </section>

    <footer>
        <div class="footer-links">
            <a href="privacy.html">Privacy Policy</a>
            <a href="#">Terms of Service</a>
            <a href="#">Contact Us</a>
        </div>
        <p>&copy; 2023 Noctis. All rights reserved.</p>
        <p class="affiliate-disclosure">As an Amazon Associate I earn from qualifying purchases.</p>
    </footer>

    <!-- Login/Signup Modal -->
    <div class="modal" id="auth-modal">
        <div class="modal-content">
            <span class="close-modal" onclick="closeModal()">&times;</span>
            <div id="auth-forms">
                <!-- Will be filled by JavaScript -->
            </div>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login - Noctis</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="logo">Noctis</div>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="#">Categories</a></li>
                <li><a href="#">Top Deals</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
        <div class="user-actions">
            <a href="login.html" class="login">Login</a>
            <a href="signup.html" class="signup">Sign Up</a>
        </div>
    </header>

    <main class="auth-page">
        <div class="auth-container">
            <h1>Welcome Back!</h1>
            
            <form id="login-form">
                <div class="form-group">
                    <label for="login-email">Email</label>
                    <input type="email" id="login-email" required>
                </div>
                
                <div class="form-group">
                    <label for="login-password">Password</label>
                    <input type="password" id="login-password" required>
                </div>
                
                <button type="submit" class="auth-button">Log In</button>
            </form>
            
            <p class="auth-link">Don't have an account? <a href="signup.html">Sign up</a></p>
        </div>
    </main>

    <footer>
        <div class="footer-links">
            <a href="privacy.html">Privacy Policy</a>
            <a href="#">Terms of Service</a>
            <a href="#">Contact Us</a>
        </div>
        <p>&copy; 2023 Noctis. All rights reserved.</p>
    </footer>

    <script>
        document.getElementById('login-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // In a real app, you would check with your server
            alert('Logged in successfully!');
            window.location.href = 'index.html';
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Noctis</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="logo">Noctis</div>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="#" onclick="filterProducts('electronics')">Electronics</a></li>
                <li><a href="#" onclick="filterProducts('home')">Home</a></li>
                <li><a href="#" onclick="filterProducts('fashion')">Fashion</a></li>
            </ul>
        </nav>
        <div class="user-actions">
            <button class="login" onclick="showLoginForm()">Login</button>
            <button class="signup" onclick="showSignupForm()">Sign Up</button>
        </div>
    </header>

    <main class="privacy-policy">
        <h1>Privacy Policy</h1>
        
        <section>
            <h2>Information Collection</h2>
            <p>We collect information when you:</p>
            <ul>
                <li>Create an account (name, email, password)</li>
                <li>Subscribe to our newsletter (email)</li>
                <li>Browse our products (anonymous usage data)</li>
            </ul>
        </section>
        
        <section>
            <h2>How We Use Information</h2>
            <p>Your information helps us to:</p>
            <ul>
                <li>Provide personalized product recommendations</li>
                <li>Improve our website</li>
                <li>Send you deals if you subscribed</li>
            </ul>
        </section>
        
        <section>
            <h2>Data Storage</h2>
            <p>All data is stored locally in your browser using localStorage. We don't use cookies or external databases.</p>
        </section>
        
        <section>
            <h2>Affiliate Disclosure</h2>
            <p>Noctis contains links to products on Amazon. As an Amazon Associate, we may earn from qualifying purchases.</p>
        </section>
        
        <section>
            <h2>Your Choices</h2>
            <p>You can:</p>
            <ul>
                <li>Delete your account anytime</li>
                <li>Unsubscribe from emails</li>
                <li>Clear your browser data to remove all information</li>
            </ul>
        </section>
    </main>

    <footer>
        <div class="footer-links">
            <a href="privacy.html">Privacy Policy</a>
            <a href="#">Terms of Service</a>
            <a href="#">Contact Us</a>
        </div>
        <p>&copy; 2023 Noctis. All rights reserved.</p>
        <p class="affiliate-disclosure">As an Amazon Associate I earn from qualifying purchases.</p>
    </footer>

    <script>
        // Simple functions to show login/signup forms
        function showLoginForm() {
            alert("Please login from the home page");
            window.location.href = "index.html";
        }
        
        function showSignupForm() {
            alert("Please sign up from the home page");
            window.location.href = "index.html";
        }
        
        function filterProducts(category) {
            window.location.href = "index.html";
        }
    </script>
</body>
</html>
// User Account System (using localStorage)
let currentUser = JSON.parse(localStorage.getItem('currentUser')) || null;
const users = JSON.parse(localStorage.getItem('users')) || [];

// Real Affiliate Products (using Amazon links that don't require affiliate signup)
const products = [
    {
        id: 1,
        title: "Apple AirPods Pro (2nd Generation)",
        price: 199.00,
        originalPrice: 249.00,
        description: "Active Noise Cancellation, Adaptive Transparency, Personalized Spatial Audio",
        category: "electronics",
        image: "https://m.media-amazon.com/images/I/61SUj2aKoEL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Alex", rating: 5, text: "Best wireless earbuds I've ever used!" },
            { author: "Sam", rating: 4, text: "Great noise cancellation" }
        ],
        affiliateLink: "https://www.amazon.com/Apple-AirPods-Pro-2nd-Generation/dp/B0CHWKQQJ3/"
    },
    {
        id: 2,
        title: "Instant Pot Duo 7-in-1 Electric Pressure Cooker",
        price: 79.95,
        originalPrice: 99.95,
        description: "7-in-1 functionality: pressure cooker, slow cooker, rice cooker, steamer, sauté pan, yogurt maker, and warmer",
        category: "home",
        image: "https://m.media-amazon.com/images/I/71Ie3JXGfVL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Jordan", rating: 5, text: "Changed my cooking game completely!" },
            { author: "Taylor", rating: 4, text: "Saves so much time in the kitchen" }
        ],
        affiliateLink: "https://www.amazon.com/Instant-Pot-Duo-Evo-Plus/dp/B07W55DDFB/"
    },
    {
        id: 3,
        title: "Levi's Men's 501 Original Fit Jeans",
        price: 49.50,
        originalPrice: 69.50,
        description: "Classic straight leg jeans with button fly",
        category: "fashion",
        image: "https://m.media-amazon.com/images/I/91XxL3gT+ZL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Casey", rating: 5, text: "Perfect fit and very comfortable" },
            { author: "Riley", rating: 4, text: "Great quality denim" }
        ],
        affiliateLink: "https://www.amazon.com/Levis-Mens-501-Original-Stonewash/dp/B001P29XJY/"
    },
    {
        id: 4,
        title: "Kindle Paperwhite (16 GB)",
        price: 139.99,
        originalPrice: 159.99,
        description: "Now with a 6.8\" display and adjustable warm light",
        category: "electronics",
        image: "https://m.media-amazon.com/images/I/61X6a4sEwmL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Morgan", rating: 5, text: "Perfect for reading at night" },
            { author: "Jamie", rating: 5, text: "Battery lasts forever" }
        ],
        affiliateLink: "https://www.amazon.com/All-new-Kindle-Paperwhite-adjustable-Waterproof/dp/B08KTZ8249/"
    },
    {
        id: 5,
        title: "Ninja Professional Blender",
        price: 89.99,
        originalPrice: 129.99,
        description: "1000-watt motor with 72 oz. pitcher",
        category: "home",
        image: "https://m.media-amazon.com/images/I/71Swqqe7XAL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Pat", rating: 4, text: "Blends everything smoothly" },
            { author: "Quinn", rating: 5, text: "Great value for the price" }
        ],
        affiliateLink: "https://www.amazon.com/Ninja-BL610-Professional-Countertop-Single-Serve/dp/B00939FV8K/"
    },
    {
        id: 6,
        title: "Adidas Men's Ultraboost Running Shoes",
        price: 119.99,
        originalPrice: 180.00,
        description: "Responsive cushioning with a snug, sock-like fit",
        category: "fashion",
        image: "https://m.media-amazon.com/images/I/71zGZ4N1OIL._AC_UF1000,1000_QL80_.jpg",
        reviews: [
            { author: "Runner1", rating: 5, text: "Most comfortable running shoes ever" },
            { author: "Runner2", rating: 5, text: "Worth every penny" }
        ],
        affiliateLink: "https://www.amazon.com/adidas-Ultraboost-Running-Shoes-Core/dp/B09Q5VKZ4H/"
    }
];

// Display Products
function displayProducts(productsToShow) {
    const container = document.getElementById('product-container');
    container.innerHTML = '';
    
    productsToShow.forEach(product => {
        const productCard = document.createElement('div');
        productCard.className = 'product-card';
        
        // Create reviews HTML
        let reviewsHTML = '';
        product.reviews.forEach(review => {
            reviewsHTML += `
                <div class="review">
                    <div class="review-author">${review.author}</div>
                    <div class="review-rating">${'★'.repeat(review.rating)}${'☆'.repeat(5 - review.rating)}</div>
                    <div class="review-text">${review.text}</div>
                </div>
            `;
        });
        
        productCard.innerHTML = `
            <img src="${product.image}" alt="${product.title}">
            <div class="product-info">
                <h3 class="product-title">${product.title}</h3>
                <p class="product-price">$${product.price} <span class="original-price">$${product.originalPrice}</span></p>
                <p class="product-description">${product.description}</p>
                <div class="reviews">${reviewsHTML}</div>
                <a href="${product.affiliateLink}" class="buy-button" target="_blank">Buy Now</a>
            </div>
        `;
        
        container.appendChild(productCard);
    });
}

// Filter Products by Category
function filterProducts(category) {
    if (category === 'all') {
        displayProducts(products);
    } else {
        const filteredProducts = products.filter(product => product.category === category);
        displayProducts(filteredProducts);
    }
}

// Search Products
function searchProducts() {
    const searchTerm = document.getElementById('search-input').value.toLowerCase();
    const filteredProducts = products.filter(product => 
        product.title.toLowerCase().includes(searchTerm) || 
        product.description.toLowerCase().includes(searchTerm)
    );
    displayProducts(filteredProducts);
}

// Newsletter Signup
function subscribeNewsletter() {
    const email = document.getElementById('newsletter-email').value;
    const message = document.getElementById('newsletter-message');
    
    if (email.includes('@')) {
        // Store in localStorage
        const subscribers = JSON.parse(localStorage.getItem('newsletterSubscribers')) || [];
        subscribers.push(email);
        localStorage.setItem('newsletterSubscribers', JSON.stringify(subscribers));
        
        message.textContent = 'Thanks for subscribing!';
        message.style.color = 'green';
        document.getElementById('newsletter-email').value = '';
    } else {
        message.textContent = 'Please enter a valid email address.';
        message.style.color = 'red';
    }
}

// User Account Functions
function updateUserDisplay() {
    const userActions = document.getElementById('user-actions');
    
    if (currentUser) {
        userActions.innerHTML = `
            <span>Welcome, ${currentUser.name}</span>
            <button onclick="logout()">Logout</button>
        `;
    } else {
        userActions.innerHTML = `
            <button onclick="showLoginForm()">Login</button>
            <button onclick="showSignupForm()">Sign Up</button>
        `;
    }
}

function showLoginForm() {
    const authForms = document.getElementById('auth-forms');
    authForms.innerHTML = `
        <h2>Login</h2>
        <form id="login-form">
            <div class="form-group">
                <label for="login-email">Email</label>
                <input type="email" id="login-email" required>
            </div>
            <div class="form-group">
                <label for="login-password">Password</label>
                <input type="password" id="login-password" required>
            </div>
            <button type="submit" class="auth-button">Log In</button>
            <p class="auth-link">Don't have an account? <a href="#" onclick="showSignupForm()">Sign up</a></p>
        </form>
    `;
    
    document.getElementById('login-form').addEventListener('submit', function(e) {
        e.preventDefault();
        const email = document.getElementById('login-email').value;
        const password = document.getElementById('login-password').value;
        
        const user = users.find(u => u.email === email && u.password === password);
        
        if (user) {
            currentUser = user;
            localStorage.setItem('currentUser', JSON.stringify(currentUser));
            updateUserDisplay();
            closeModal();
            alert('Logged in successfully!');
        } else {
            alert('Invalid email or password!');
        }
    });
    
    document.getElementById('auth-modal').style.display = 'block';
}

function showSignupForm() {
    const authForms = document.getElementById('auth-forms');
    authForms.innerHTML = `
        <h2>Sign Up</h2>
        <form id="signup-form">
            <div class="form-group">
                <label for="signup-name">Full Name</label>
                <input type="text" id="signup-name" required>
            </div>
            <div class="form-group">
                <label for="signup-email">Email</label>
                <input type="email" id="signup-email" required>
            </div>
            <div class="form-group">
                <label for="signup-password">Password</label>
                <input type="password" id="signup-password" required>
            </div>
            <button type="submit" class="auth-button">Sign Up</button>
            <p class="auth-link">Already have an account? <a href="#" onclick="showLoginForm()">Log in</a></p>
        </form>
    `;
    
    document.getElementById('signup-form').addEventListener('submit', function(e) {
        e.preventDefault();
        const name = document.getElementById('signup-name').value;
        const email = document.getElementById('signup-email').value;
        const password = document.getElementById('signup-password').value;
        
        // Check if user already exists
        if (users.some(u => u.email === email)) {
            alert('Email already in use!');
            return;
        }
        
        // Create new user
        const newUser = { name, email, password };
        users.push(newUser);
        localStorage.setItem('users', JSON.stringify(users));
        
        currentUser = newUser;
        localStorage.setItem('currentUser', JSON.stringify(currentUser));
        
        updateUserDisplay();
        closeModal();
        alert('Account created successfully!');
    });
    
    document.getElementById('auth-modal').style.display = 'block';
}

function logout() {
    currentUser = null;
    localStorage.removeItem('currentUser');
    updateUserDisplay();
    alert('Logged out successfully!');
}

function closeModal() {
    document.getElementById('auth-modal').style.display = 'none';
}

// Track Affiliate Links
function trackAffiliateLinks() {
    document.addEventListener('click', function(e) {
        if (e.target.classList.contains('buy-button')) {
            // In a real app, you might track this click in your analytics
            console.log('Affiliate link clicked: ' + e.target.href);
        }
    });
}

// Initialize the page
document.addEventListener('DOMContentLoaded', function() {
    // Display all products initially
    displayProducts(products);
    
    // Setup search
    document.getElementById('search-button').addEventListener('click', searchProducts);
    document.getElementById('search-input').addEventListener('keypress', function(e) {
        if (e.key === 'Enter') {
            searchProducts();
        }
    });
    
    // Update user display
    updateUserDisplay();
    
    // Track affiliate links
    trackAffiliateLinks();
    
    // Close modal if clicked outside
    window.addEventListener('click', function(e) {
        if (e.target === document.getElementById('auth-modal')) {
            closeModal();
        }
    });
});
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up - Noctis</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="logo">Noctis</div>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="#">Categories</a></li>
                <li><a href="#">Top Deals</a></li>
                <li><a href="#">About</a></li>
            </ul>
        </nav>
        <div class="user-actions">
            <a href="login.html" class="login">Login</a>
            <a href="signup.html" class="signup">Sign Up</a>
        </div>
    </header>

    <main class="auth-page">
        <div class="auth-container">
            <h1>Create Your Account</h1>
            
            <form id="signup-form">
                <div class="form-group">
                    <label for="name">Full Name</label>
                    <input type="text" id="name" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" required>
                </div>
                
                <div class="form-group">
                    <label for="password">Password</label>
                    <input type="password" id="password" required>
                </div>
                
                <div class="form-group">
                    <label for="confirm-password">Confirm Password</label>
                    <input type="password" id="confirm-password" required>
                </div>
                
                <button type="submit" class="auth-button">Sign Up</button>
            </form>
            
            <p class="auth-link">Already have an account? <a href="login.html">Log in</a></p>
        </div>
    </main>

    <footer>
        <div class="footer-links">
            <a href="privacy.html">Privacy Policy</a>
            <a href="#">Terms of Service</a>
            <a href="#">Contact Us</a>
        </div>
        <p>&copy; 2023 Noctis. All rights reserved.</p>
    </footer>

    <script>
        document.getElementById('signup-form').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const password = document.getElementById('password').value;
            const confirmPassword = document.getElementById('confirm-password').value;
            
            if (password !== confirmPassword) {
                alert("Passwords don't match!");
                return;
            }
            
            // In a real app, you would send this data to your server
            alert('Account created successfully! You can now log in.');
            window.location.href = 'login.html';
        });
    </script>
</body>
</html>
* Basic Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Arial', sans-serif;
}

body {
    background-color: #f8f9fa;
    color: #333;
    line-height: 1.6;
}

/* Header Styles */
header {
    background-color: #1a1a2e;
    color: white;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
}

.logo {
    font-size: 2rem;
    font-weight: bold;
    color: #4cc9f0;
}

/* Search Bar */
.search-container {
    flex-grow: 1;
    margin: 0 1rem;
    display: flex;
    min-width: 250px;
}

#search-input {
    padding: 0.5rem;
    border: none;
    border-radius: 4px 0 0 4px;
    width: 70%;
}

#search-button {
    padding: 0.5rem 1rem;
    background-color: #4cc9f0;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

/* Navigation */
nav ul {
    display: flex;
    list-style: none;
    flex-wrap: wrap;
    justify-content: center;
}

nav ul li {
    margin-left: 1.5rem;
}

nav ul li a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
}

nav ul li a:hover {
    color: #4cc9f0;
}

/* User Actions */
.user-actions {
    display: flex;
    align-items: center;
    gap: 1rem;
}

.user-actions button, .user-actions .login, .user-actions .signup {
    padding: 0.5rem 1rem;
    border-radius: 4px;
    font-weight: bold;
    cursor: pointer;
}

.user-actions button, .user-actions .signup {
    background-color: #4cc9f0;
    color: white;
    border: none;
}

.user-actions .login {
    background-color: transparent;
    color: white;
    border: 1px solid white;
}

.user-actions span {
    color: white;
    margin-right: 1rem;
}

/* Hero Section */
.hero {
    text-align: center;
    padding: 4rem 1rem;
    background: linear-gradient(135deg, #16213e, #1a1a2e);
    color: white;
}

.hero h1 {
    font-size: 2.5rem;
    margin-bottom: 1rem;
}

/* Newsletter */
.newsletter {
    margin: 2rem auto 0;
    max-width: 500px;
}

.newsletter input {
    padding: 0.7rem;
    width: 60%;
    border: none;
    border-radius: 4px 0 0 4px;
}

.newsletter button {
    padding: 0.7rem 1rem;
    background-color: #4cc9f0;
    color: white;
    border: none;
    border-radius: 0 4px 4px 0;
    cursor: pointer;
}

.newsletter-message {
    margin-top: 0.5rem;
    font-size: 0.9rem;
}

/* Categories */
.categories {
    padding: 3rem 2rem;
    text-align: center;
}

.category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.category-card {
    background-color: white;
    border-radius: 8px;
    padding: 1rem;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    cursor: pointer;
    transition: transform 0.3s;
}

.category-card:hover {
    transform: translateY(-5px);
}

.category-card img {
    width: 100%;
    height: 150px;
    object-fit: cover;
    border-radius: 4px;
}

/* Products */
.products {
    padding: 2rem;
}

.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.product-card {
    background-color: white;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    transition: transform 0.3s;
}

.product-card:hover {
    transform: translateY(-5px);
}

.product-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.product-info {
    padding: 1rem;
}

.product-title {
    font-size: 1.1rem;
    margin-bottom: 0.5rem;
}

.product-price {
    font-weight: bold;
    color: #e63946;
    margin-bottom: 0.5rem;
}

.original-price {
    text-decoration: line-through;
    color: #777;
    font-size: 0.9rem;
    margin-left: 0.5rem;
}

.product-description {
    color: #555;
    font-size: 0.9rem;
    margin-bottom: 1rem;
}

.buy-button {
    display: block;
    padding: 0.7rem;
    background-color: #4cc9f0;
    color: white;
    text-align: center;
    text-decoration: none;
    border-radius: 4px;
    font-weight: bold;
    transition: background-color 0.3s;
}

.buy-button:hover {
    background-color: #3aa8d8;
}

/* Reviews */
.reviews {
    margin-top: 1rem;
    border-top: 1px solid #eee;
    padding-top: 1rem;
}

.review {
    margin-bottom: 1rem;
}

.review-author {
    font-weight: bold;
    font-size: 0.9rem;
}

.review-text {
    font-size: 0.9rem;
    color: #555;
}

.review-rating {
    color: #f4a261;
    font-size: 0.9rem;
}

/* Payment Methods */
.payment-methods {
    text-align: center;
    padding: 2rem;
    background-color: #f1faee;
}

.payment-icons {
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap;
    margin-top: 1rem;
}

.payment-icons img {
    height: 40px;
    object-fit: contain;
}

/* Footer */
footer {
    text-align: center;
    padding: 2rem;
    background-color: #1a1a2e;
    color: white;
}

.footer-links {
    margin-bottom: 1rem;
}

.footer-links a {
    color: white;
    margin: 0 1rem;
    text-decoration: none;
}

.affiliate-disclosure {
    font-size: 0.8rem;
    margin-top: 1rem;
    color: #aaa;
}

/* Modal */
.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,0.7);
    z-index: 100;
}

.modal-content {
    background-color: white;
    margin: 10% auto;
    padding: 2rem;
    border-radius: 8px;
    width: 90%;
    max-width: 400px;
    position: relative;
}

.close-modal {
    position: absolute;
    top: 1rem;
    right: 1rem;
    font-size: 1.5rem;
    cursor: pointer;
}

/* Auth Forms */
.auth-forms h2 {
    text-align: center;
    margin-bottom: 1.5rem;
    color: #1a1a2e;
}

.form-group {
    margin-bottom: 1rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
}

.form-group input {
    width: 100%;
    padding: 0.7rem;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.auth-button {
    width: 100%;
    padding: 0.8rem;
    background-color: #4cc9f0;
    color: white;
    border: none;
    border-radius: 4px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 1rem;
}

.auth-button:hover {
    background-color: #3aa8d8;
}

.auth-link {
    text-align: center;
    margin-top: 1.5rem;
}

.auth-link a {
    color: #4cc9f0;
    text-decoration: none;
}

/* Responsive Design */
@media (max-width: 768px) {
    header {
        flex-direction: column;
        gap: 1rem;
    }
    
    .search-container {
        margin: 1rem 0;
        width: 100%;
    }
    
    nav ul {
        margin-top: 1rem;
        flex-wrap: wrap;
        justify-content: center;
    }
    
    .user-actions {
        margin-top: 1rem;
    }
    
    .newsletter input {
        width: 100%;
        border-radius: 4px;
        margin-bottom: 0.5rem;
    }
    
    .newsletter button {
        width: 100%;
        border-radius: 4px;
    }
    
    .modal-content {
        margin: 20% auto;
    }
}
