# Bangladesh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bangladesh: A Land of Diversity</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #006a4e;
            --secondary: #f42a41;
            --accent: #ff9933;
            --light: #f8f8f8;
            --dark: #333;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: linear-gradient(to right, var(--primary), #008060);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-text {
            font-size: 1.8rem;
            font-weight: 700;
        }

        .logo i {
            font-size: 2.2rem;
            color: var(--accent);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 5px 10px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        nav a:hover, nav a.active {
            background-color: rgba(255, 255, 255, 0.2);
        }

        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1582573618381-932f6a8f3875?ixlib=rb-4.0.3') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 80px 20px;
            margin-bottom: 40px;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background-color: #e21a32;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary);
            position: relative;
            padding-bottom: 15px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
        }

        .card-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 50px;
        }

        .card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-10px);
        }

        .card-img {
            height: 200px;
            overflow: hidden;
        }

        .card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .card:hover .card-img img {
            transform: scale(1.1);
        }

        .card-content {
            padding: 20px;
        }

        .card h3 {
            color: var(--primary);
            margin-bottom: 15px;
        }

        .card p {
            color: #666;
            margin-bottom: 20px;
        }

        .card-btn {
            display: inline-block;
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
        }

        .card-btn:hover {
            color: var(--secondary);
        }

        .quick-facts {
            background-color: var(--primary);
            color: white;
            padding: 50px 0;
            margin: 50px 0;
        }

        .facts-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .fact-box {
            text-align: center;
            padding: 20px;
        }

        .fact-box i {
            font-size: 2.5rem;
            color: var(--accent);
            margin-bottom: 15px;
        }

        .fact-box h3 {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }

        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-section h3 {
            color: var(--accent);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-section p {
            margin-bottom: 15px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s ease;
        }

        .social-icons a:hover {
            color: var(--accent);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #555;
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                gap: 10px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-landmark"></i>
                <div class="logo-text">Bangladesh</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active">Home</a></li>
                    <li><a href="#">History</a></li>
                    <li><a href="#">Culture</a></li>
                    <li><a href="#">Geography</a></li>
                    <li><a href="#">Economy</a></li>
                    <li><a href="#">Tourism</a></li>
                    <li><a href="#">Education</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Discover the Beauty of Bangladesh</h1>
            <p>Explore the rich history, vibrant culture, and natural wonders of this South Asian gem</p>
            <a href="#" class="btn">Explore Now</a>
        </div>
    </section>

    <!-- Main Content -->
    <main class="container">
        <!-- About Section -->
        <section>
            <h2 class="section-title">About Bangladesh</h2>
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1591637333184-19aa84b3e01f?ixlib=rb-4.0.3" alt="Bangladesh Landscape">
                    </div>
                    <div class="card-content">
                        <h3>Geography & Nature</h3>
                        <p>Bangladesh is a riverine country located in South Asia with a coastline of 580 km along the Bay of Bengal. It is the 8th most populous country in the world.</p>
                        <a href="#" class="card-btn">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-15819 rama-1b9a5c42a167?ixlib=rb-4.0.3" alt="Bangladesh Culture">
                    </div>
                    <div class="card-content">
                        <h3>Rich Culture</h3>
                        <p>Bangladesh has a rich cultural heritage that encompasses literature, music, art, dance, and drama. The Bengali language has a rich literary heritage.</p>
                        <a href="#" class="card-btn">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1573588028698-9a9a6dae2c17?ixlib=rb-4.0.3" alt="Bangladesh Economy">
                    </div>
                    <div class="card-content">
                        <h3>Growing Economy</h3>
                        <p>Bangladesh is one of the fastest growing economies in the world. It has made significant strides in human development and poverty reduction.</p>
                        <a href="#" class="card-btn">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Quick Facts Section -->
        <section class="quick-facts">
            <div class="container">
                <h2 class="section-title" style="color: white;">Quick Facts</h2>
                <div class="facts-container">
                    <div class="fact-box">
                        <i class="fas fa-users"></i>
                        <h3>169 Million</h3>
                        <p>Population</p>
                    </div>
                    <div class="fact-box">
                        <i class="fas fa-globe-asia"></i>
                        <h3>147,570 km²</h3>
                        <p>Total Area</p>
                    </div>
                    <div class="fact-box">
                        <i class="fas fa-city"></i>
                        <h3>Dhaka</h3>
                        <p>Capital City</p>
                    </div>
                    <div class="fact-box">
                        <i class="fas fa-language"></i>
                        <h3>Bengali</h3>
                        <p>Official Language</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Tourism Section -->
        <section>
            <h2 class="section-title">Tourist Attractions</h2>
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1566549952257-37b685a5edf2?ixlib=rb-4.0.3" alt="Cox's Bazar">
                    </div>
                    <div class="card-content">
                        <h3>Cox's Bazar</h3>
                        <p>The world's longest natural sea beach, stretching 120 km along the Bay of Bengal. It's one of the most popular tourist destinations in Bangladesh.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1592409065737-1d8f0c634b70?ixlib=rb-4.0.3" alt="Sundarbans">
                    </div>
                    <div class="card-content">
                        <h3>Sundarbans</h3>
                        <p>The largest mangrove forest in the world, home to the Royal Bengal Tiger. It's a UNESCO World Heritage Site shared between Bangladesh and India.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1615551043360-33f08e6c9b0c?ixlib=rb-4.0.3" alt="Historical Sites">
                    </div>
                    <div class="card-content">
                        <h3>Historical Sites</h3>
                        <p>Bangladesh has numerous historical sites including the Sixty Dome Mosque, Lalbagh Fort, and Mahasthangarh - one of the earliest urban archaeological sites.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About Us</h3>
                    <p>We are dedicated to providing accurate and comprehensive information about Bangladesh, its culture, history, and people.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <p><a href="#">History</a></p>
                    <p><a href="#">Culture</a></p>
                    <p><a href="#">Geography</a></p>
                    <p><a href="#">Economy</a></p>
                </div>
                <div class="footer-section">
                    <h3>Contact Us</h3>
                    <p><i class="fas fa-envelope"></i> info@bangladesh.com</p>
                    <p><i class="fas fa-phone"></i> +880 XXXX-XXXXXX</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2023 Bangladesh Information Portal. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('nav a');
            
            navLinks.forEach(link => {
                link.addEventListener('click', function() {
                    navLinks.forEach(l => l.classList.remove('active'));
                    this.classList.add('active');
                });
            });
            
            const cards = document.querySelectorAll('.card');
            cards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    this.style.transition = 'transform 0.3s ease';
                });
            });
        });
    </script>
</body>
</html>
