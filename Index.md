HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Navigation Bar</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header Container -->
    <header class="navbar-container">
        <!-- Logo -->
        <div class="logo">
            <a href="#">BrandLogo</a>
        </div>

        <!-- Navigation Links -->
        <nav>
            <ul class="nav-links">
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>

        <!-- Action Button -->
        <div class="nav-btn">
            <a href="#" class="btn">Get Started</a>
        </div>
    </header>

</body>
</html>

CSS
/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f4f7f6;
}

/* 1 & 2. Header and Flex Container */
.navbar-container {
    display: flex;
    background-color: #ffffff;
    padding: 1rem 5%;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
    
    /* 3. Set spacing between items */
    justify-content: space-between;
    
    /* 4. Align vertically */
    align-items: center;
}

/* Logo Styling */
.logo a {
    font-size: 1.5rem;
    font-weight: bold;
    color: #2c3e50;
    text-decoration: none;
}

/* 5. Navigation Links Styling */
.nav-links {
    display: flex;
    list-style: none;
    gap: 2rem; /* Modern alternative to spacing list items */
}

.nav-links a {
    text-decoration: none;
    color: #555555;
    font-size: 1rem;
    font-weight: 500;
    transition: color 0.3s ease;
}

.nav-links a:hover {
    color: #3498db;
}

/* Button Styling */
.btn {
    background-color: #3498db;
    color: #ffffff;
    padding: 0.6rem 1.2rem;
    border-radius: 4px;
    text-decoration: none;
    font-weight: 500;
    transition: background-color 0.3s ease;
}

.btn:hover {
    background-color: #2980b9;
}

/* 6. Responsive Design (Inspect by changing browser width) */
@media (max-width: 768px) {
    .navbar-container {
        flex-direction: column;
        gap: 1rem;
        padding: 1rem;
    }

    .nav-links {
        flex-direction: column;
        align-items: center;
        gap: 1rem;
    }
}