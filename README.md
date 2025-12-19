#index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Light Responsive Landing Page</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Navbar -->
    <nav id="navbar">
        <div class="logo">SkillCraft Technology</div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Sections -->
    <section id="home" class="section home">
        <h1>Welcome to SkillCraft</h1>
        <p>Build clean, responsive and modern web applications</p>
    </section>

    <section id="about" class="section about">
        <h1>About Us</h1>
        <p>We focus on simplicity, usability and performance.</p>
    </section>

    <section id="services" class="section services">
        <h1>Services</h1>
        <p>Web Design • Development • UI/UX Solutions</p>
    </section>

    <section id="contact" class="section contact">
        <h1>Contact</h1>
        <p>Let’s build something amazing together.</p>
    </section>

    <script src="script.js"></script>
</body>
</html>

#style.css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

/* Navbar */
nav {
    position: fixed;
    top: 0;
    width: 100%;
    height: 70px;
    background: #ffffff;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 40px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    z-index: 1000;
    transition: 0.3s;
}

nav.scrolled {
    background: #f5f7ff;
}

.logo {
    font-size: 24px;
    font-weight: bold;
    color: #4f46e5;
}

nav ul {
    list-style: none;
    display: flex;
    gap: 25px;
}

nav ul li a {
    color: #333;
    text-decoration: none;
    font-weight: 500;
    transition: 0.3s;
}

nav ul li a:hover {
    color: #4f46e5;
}

/* Sections */
.section {
    min-height: 100vh;
    padding-top: 70px; /* keeps section content below navbar */
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.section h1 {
    font-size: 42px;
    margin-bottom: 10px;
}

.section p {
    font-size: 18px;
    max-width: 500px;
}

/* Light color backgrounds */
.home {
    background: linear-gradient(135deg, #e0e7ff, #f0f9ff);
}

.about {
    background: linear-gradient(135deg, #fef3c7, #fff7ed);
}

.services {
    background: linear-gradient(135deg, #dcfce7, #ecfeff);
}

.contact {
    background: linear-gradient(135deg, #fce7f3, #fdf2f8);
}

/* Responsive */
@media (max-width: 768px) {
    nav ul {
        display: none;
    }

    .section h1 {
        font-size: 32px;
    }
}

#script.js
const navbar = document.getElementById("navbar");

window.addEventListener("scroll", () => {
    if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }
});
