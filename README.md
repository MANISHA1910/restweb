# Ex.07 Restaurant Website
## Date:16.05.2025

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:
HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Little Lemon Restaurant</title>
    <meta name="description" content="A Brief Description">
    <meta name="author" content="Luxury Jewellery">

    <!-- Load static files -->
    {% load static %}

    <link rel="stylesheet" href="{% static 'styles.css' %}">
</head>
<body>

    <!-- Header section -->
    <header>
        <div class="logo">
            <img src="{% static 'images/logo.png' %}" alt="Client Logo">
        </div>
        <nav>
            <ul class="nav-menu">
                <li><a href="index.html">Home</a></li>
                <li><a href="services.html">Services</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main content section -->
    <main>
        <!-- Promotional Banner -->
        <section class="promo">
            <h1>Welcome to Little Lemon</h1>
            <p>Have your Favourite taste...</p>
            <img src="{% static 'images/img1.png' %}" alt="banner">
            <p>Savor the best of both worlds with our delicious veg and non-veg dishes, crafted to perfection. From mouthwatering starters to irresistible snacks, every bite is a burst of flavor. Join us for a dining experience that satisfies every craving!</p>
        </section>

        <!-- Three columns section -->
        <section class="three-columns">
            <article class="column">
                <h2>Starters and Snacks</h2>
                <img src="{% static 'images/img2.png' %}" alt="Starters&Snacks">
                <p>*  Kickstart your cravings with our irresistible starters and snacks, bursting with flavor in every bite.</p>
                <p>*  Perfectly crafted to tease your taste buds, our delicious selection is the ultimate treat for any occasion.</p> 
                <p>*  Indulge in the perfect bite-sized delights!</p>
            </article>
            <article class="column">
                <h2>Vegetarian</h2>
                <img src="{% static 'images/img3.png' %}" alt="Veg">
                <p>*  Delight in our fresh, flavorful vegetarian dishes that celebrate nature's finest ingredients.</p>
                <p>*  Each meal is crafted to nourish your body and satisfy your taste buds.</p>
                <p>*  Experience the vibrant taste of wholesome, plant-based goodness!</p>
            </article>
            <article class="column">
                <h2>Non-Vegetarian</h2>
                <img src="{% static 'images/img4.png' %}" alt="NonVeg">
                <p>*  Indulge in the rich, savory flavors of our premium non-veg dishes, expertly crafted for true food lovers.</p>
                <p>*  From tender meats to bold spices, every bite promises a taste of perfection.</p>
                <p>*  Satisfy your cravings with our irresistible non-veg delights!</p>
            </article>
        </section>
    </main>

    <!-- Footer section -->
    <footer>
        <div class="footer-left">
            <img src="{% static 'images/logo_footer.png' %}" alt="Client Logo">
        </div>
        <div class="footer-right">
            <p>&copy; 2024 Little Lemon. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>

CSS

/* General reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body styling */
body {
    font-family: 'Times New Roman', Times, serif;
    line-height: 1.6;
    background-color: #fafafa; /* Light background for a clean look */
}

/* Header section */
header {
    display: block;
    align-items: center;
    padding: 50px 30px;
    background-color: #333;
    color: #fff;
    text-align: center; /* Center the header content */
}

.logo img {
    display: block;
    width: 250px; /* Adjust size for better proportion */
    margin: 0 auto 20px auto; /* Center logo and add margin */
}

nav ul {
    list-style: none;
    display: flex;
    justify-content: center; /* Center navigation items */
    margin-top: 10px;
}

nav ul li {
    margin: 0 15px; /* Add space between nav items */
}

nav ul li a {
    text-decoration: none;
    color: #fff;
    padding: 15px 20px;
    transition: background 0.3s ease, transform 0.3s ease; /* Add transition for hover effects */
    font-size: 1.2rem;
    font-weight: bold; /* Make links more prominent */
}

nav ul li a:hover {
    background-color: #555;
    border-radius: 5px;
    transform: scale(1.1); /* Scale effect on hover */
}

/* Promo banner */
.promo {
    background-color: #f4f4f4;
    text-align: center;
    padding: 50px 20px;
    margin-bottom: 40px;
    border-top: 5px solid #333; /* Add top border for distinction */
}

.promo h1 {
    font-size: 3rem; /* Larger headline */
    margin-bottom: 15px;
    color: #333;
}

.promo p {
    font-size: 1.5rem;
    color: #e60000; /* Red text for promotional effect */
    margin-bottom: 25px;
    font-style: italic; /* Add a style effect */
}

.promo img {
    max-width: 100%; /* Make sure the banner image scales properly */
    height: auto;
    border-radius: 8px; /* Rounded corners for the banner */
}

/* Three columns layout */
.three-columns {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    gap: 20px; /* Provide spacing between columns */
}

.column {
    text-align: center;
    flex: 1;
    margin: 0 10px;
    background-color: #fff; /* Add background for each column */
    padding: 20px;
    border-radius: 8px; /* Rounded corners for each column */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add subtle shadow for depth */
}

.column img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    transition: transform 0.3s ease;
}

.column img:hover {
    transform: scale(1.05); /* Hover zoom effect on images */
}

.column h2 {
    margin: 15px 0;
    color: #333;
    font-size: 2rem; /* Larger headings for clarity */
}

.column p {
    font-size: 1rem;
    color: #555; /* Slightly lighter text */
}

/* Footer styling */
footer {
    background-color: #333;
    color: #fff;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.footer-left img {
    width: 150px; /* Smaller footer logo */
}

.footer-right p {
    margin: 0;
    font-size: 1.2rem;
    text-align: right; /* Align the copyright text to the right */
    color: #ccc; /* Light grey for footer text */
}

/* Responsive design */
@media (max-width: 768px) {
    .three-columns {
        flex-direction: column;
    }

    .column {
        margin-bottom: 20px;
    }

    nav ul {
        flex-direction: column;
        margin-top: 20px;
    }

    nav ul li {
        margin-bottom: 10px;
    }

    .promo {
        padding: 30px 20px; /* Adjust promo section padding for small screens */
    }
}




## OUTPUT
![Screenshot 2025-05-16 205312](https://github.com/user-attachments/assets/a41ebaa9-2f61-47a0-b8ee-a9789d2fa9f1)



## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
