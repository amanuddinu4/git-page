# Visionary Creations - Static Website Documentation
Purpose
The "Visionary Creations" website is a static webpage designed to showcase professional services, a portfolio, and a contact form. It's built using HTML for structure and CSS for styling, and is deployable via GitHub Pages.

Tools Used
- HTML: To structure the website content.
- CSS: To style the website.
- GitHub Pages: To host and publish the website.

# Code Explanation
# 1. HTML Code
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Visionary Creations</title>
    <link href="img.png" rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="logo">
            <img src="img.png" alt="Visionary Creations Logo">
            <h1>Visionary Creations</h1>
        </div>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#portfolio">Portfolio</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section id="hero">
        <div class="hero-content">
            <h2>Empowering Your Digital Vision</h2>
            <p>Building professional solutions tailored to your success.</p>
            <a href="#services" class="btn">Discover Our Services</a>
        </div>
    </section>

    <main>
        <section id="services">
            <h2>Our Services</h2>
            <div class="service-cards">
                <div class="card">
                    <i class="icon">🌐</i>
                    <h3>Web Design</h3>
                    <p>Crafting stunning, user-friendly designs that captivate audiences.</p>
                </div>
                <div class="card">
                    <i class="icon">📈</i>
                    <h3>SEO Solutions</h3>
                    <p>Boosting visibility with cutting-edge optimization techniques.</p>
                </div>
                <div class="card">
                    <i class="icon">📣</i>
                    <h3>Marketing</h3>
                    <p>Driving growth with innovative marketing strategies tailored for impact.</p>
                </div>
            </div>
        </section>

        <section id="portfolio">
            <h2>Our Portfolio</h2>
            <div class="portfolio-gallery">
                <div class="gallery-item" style="background-image: url('portfolio1.jpg');"></div>
                <div class="gallery-item" style="background-image: url('portfolio2.jpg');"></div>
                <div class="gallery-item" style="background-image: url('portfolio3.jpg');"></div>
            </div>
        </section>

        <section id="contact">
            <h2>Contact Us</h2>
            <form>
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" placeholder="Your Name" required>
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" placeholder="Your Email" required>
                
                <label for="message">Message:</label>
                <textarea id="message" name="message" rows="5" placeholder="Your Message" required></textarea>
                
                <button type="submit">Send Message</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 MyWebsite | All Rights Reserved.</p>
    </footer>

    <script>
        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>

# 2. CSS Code
 
   /* General Styles */
body {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    background-color: whitesmoke;
    color: #333;
    line-height: 1.6;
}

h1, h2, h3 {
    font-family: 'Open Sans', sans-serif;
}

header {
    background: linear-gradient(90deg, #007bff, #0056b3);
    color: white;
    padding: 1em;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
header .logo {
    display: flex; /* Aligns elements in a row */
    align-items: center; /* Vertically centers the elements */
    gap: 10px; /* Optional: Space between logo and title */
}

header .logo img {
    height: 50px; /* Adjust size of the logo */
    width: auto; /* Maintain aspect ratio */
}

header h1 {
    font-family: 'Roboto', sans-serif; /* Ensures the font stays as you planned */
    font-size: 1.5rem; /* Customize title size */
    margin: 0; /* Remove default margin */
}
header .logo h1 {
    font-size: 1.8em;
    font-weight: 700;
}

nav ul {
    list-style: none;
    display: flex;
    padding: 0;
}

nav ul li {
    margin: 0 1em;
}

nav ul li a {
    color: wheat;
    text-decoration: none;
    font-weight: 600;
}

nav ul li a:hover {
    text-decoration: underline;
}

/* Hero Section */
#hero {
    background: url('hero-image.jpg') no-repeat center center/cover;
    color: maroon;
    text-align: center;
    padding: 10em 1em;
    position: relative;
}

#hero .btn {
    background-color: grey;
    color: white;
    padding: 12px 25px;
    text-decoration: none;
    font-weight: bold;
    border-radius: 5px;
    transition: all 0.3s ease-in-out;
}

#hero .btn:hover {
    background-color: #e64a19;
    transform: scale(1.1);
}

/* Services Section */
#services {
    padding: 2em;
    background: #fdfdfd;
    text-align: center;
}

.service-cards {
    display: flex;
    justify-content: space-evenly;
    margin-top: 2em;
}

.card {
    background: white;
    padding: 1.5em;
    border-radius: 8px;
    width: 30%;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.card:hover {
    transform: translateY(-10px);
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.card .icon {
    font-size: 2em;
    margin-bottom: 1em;
    color: #007bff;
}

/* Portfolio Section */
#portfolio {
    padding: 2em;
    background: #f4f4f4;
}

.portfolio-gallery {
    display: flex;
    justify-content: space-evenly;
    margin-top: 1.5em;
}

.gallery-item {
    width: 30%;
    height: 200px;
    border-radius: 8px;
    background-size: cover;
    background-position: center;
}

/* Contact Section */
#contact form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1em;
    max-width: 600px;
    margin: 0 auto;
    padding: 2em;
    background: white;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

form input, form textarea, form button {
    width: 100%;
    padding: 0.8em;
    border: 1px solid #ddd;
    border-radius: 4px;
}

form button {
    background: #007bff;
    color: white;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease-in-out;
}

form button:hover {
    background-color: #0056b3;
}

/* Footer */
footer {
    text-align: center;
    padding: 1em;
    background: #333;
    color: white;
    font-size: 0.9em;
}

/* Responsive Design */
@media (max-width: 768px) {
    .service-cards, .portfolio-gallery {
        flex-direction: column;
        align-items: center;
    }

    .card, .gallery-item {
        width: 80%;
    }

    nav ul {
        flex-direction: column;
    }
}

# Deployment Guide

- Prepare the Code:- Save the HTML code as index.html.
- Save the CSS code as style.css.
- Add any necessary images (e.g., hero-image.jpg).

 # Create a GitHub Repository:
- Go to GitHub and create a new repository.
- Upload the files to the repository.

#  Enable GitHub Pages:
- Go to the repository’s Settings.
- Under the Pages section, set the source to main branch and root folder.

 #  Access Your Website:-
- GitHub will provide a live link (e.g., https://<username>.github.io/<repo-name>).





