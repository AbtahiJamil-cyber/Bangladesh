<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bangladesh: Official Information Portal</title>
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
            --transition: all 0.3s ease;
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
            gap: 5px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            padding: 10px 15px;
            border-radius: 5px;
            transition: var(--transition);
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
            transition: var(--transition);
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

        .content-section {
            display: none;
            padding: 30px 0;
        }

        .content-section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
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

        .history-timeline {
            margin: 40px 0;
            position: relative;
        }

        .history-timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 100%;
            background-color: var(--primary);
        }

        .timeline-item {
            width: 50%;
            padding: 20px 40px;
            position: relative;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            top: 30px;
            width: 20px;
            height: 20px;
            background-color: var(--secondary);
            border-radius: 50%;
        }

        .timeline-item:nth-child(odd)::after {
            right: -10px;
        }

        .timeline-item:nth-child(even)::after {
            left: -10px;
        }

        .timeline-content {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .timeline-content h3 {
            color: var(--primary);
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
                gap: 5px;
                flex-wrap: wrap;
                justify-content: center;
            }

            nav a {
                padding: 8px 12px;
                font-size: 0.9rem;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .history-timeline::before {
                left: 20px;
            }

            .timeline-item {
                width: 100%;
                padding-left: 50px;
                padding-right: 20px;
            }

            .timeline-item:nth-child(even) {
                left: 0;
            }

            .timeline-item:nth-child(odd)::after,
            .timeline-item:nth-child(even)::after {
                left: 10px;
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
                    <li><a href="#" class="nav-link active" data-section="home">Home</a></li>
                    <li><a href="#" class="nav-link" data-section="history">History</a></li>
                    <li><a href="#" class="nav-link" data-section="culture">Culture</a></li>
                    <li><a href="#" class="nav-link" data-section="geography">Geography</a></li>
                    <li><a href="#" class="nav-link" data-section="economy">Economy</a></li>
                    <li><a href="#" class="nav-link" data-section="tourism">Tourism</a></li>
                    <li><a href="#" class="nav-link" data-section="education">Education</a></li>
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
        <!-- Home Section -->
        <section id="home" class="content-section active">
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
                        <img src="https://images.unsplash.com/photo-1581988115590-baab13b4c6bb?ixlib=rb-4.0.3" alt="Bangladesh Culture">
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

            <!-- Quick Facts Section -->
            <div class="quick-facts">
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

            <!-- Tourism Section -->
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

        <!-- History Section -->
        <section id="history" class="content-section">
            <h2 class="section-title">History of Bangladesh</h2>
            <p>Bangladesh has a rich historical heritage dating back millennia. The region was part of various ancient kingdoms and empires, including the Mauryan Empire, the Gupta Empire, the Pala Empire, and the Bengal Sultanate.</p>
            
            <div class="history-timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Ancient Period</h3>
                        <p>Evidence of human settlement in Bangladesh dates back 4,000 years. The region was known as Gangaridai to the ancient Greeks and Romans.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Medieval Period</h3>
                        <p>Islam was introduced in the 12th century. The Bengal Sultanate (1352–1576) was a major trading nation and one of Asia's wealthiest regions.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Colonial Era</h3>
                        <p>The British East India Company established control in 1757. Bengal was partitioned in 1905, creating the province of East Bengal and Assam.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Partition & Pakistan</h3>
                        <p>Following the partition of India in 1947, Bangladesh became East Pakistan, separated by 1,600 km of Indian territory.</p>
                    </div>
                </div>
                great
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Liberation War</h3>
                        <p>The Bangladesh Liberation War in 1971 led to independence from Pakistan after nine months of conflict.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Modern Bangladesh</h3>
                        <p>Since independence, Bangladesh has developed into a democratic, secular republic with significant economic growth.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Culture Section -->
        <section id="culture" class="content-section">
            <h2 class="section-title">Culture of Bangladesh</h2>
            <p>Bangladesh has a rich, diverse cultural heritage that encompasses literature, music, dance, drama, art, craft, folklore, and philosophy.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1550684848-fac1c5b4e853?ixlib=rb-4.0.3" alt="Bengali Cuisine">
                    </div>
                    <div class="card-content">
                        <h3>Cuisine</h3>
                        <p>Bangladeshi cuisine is known for its rice, fish, and use of spices. Popular dishes include biryani, hilsa fish curry, and various sweets like roshogolla.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-164119 Adel-1b9a5c42a167?ixlib=rb-4.0.3" alt="Traditional Clothing">
                    </div>
                    <div class="card-content">
                        <h3>Traditional Clothing</h3>
                        <p>Traditional attire includes sarees for women and lungi or panjabi for men. The nakshi kantha is a traditional embroidered quilt.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1618669254010-6a10c64b5a4d?ixlib=rb-4.0.3" alt="Festivals">
                    </div>
                    <div class="card-content">
                        <h3>Festivals</h3>
                        <p>Major festivals include Pohela Boishakh (Bengali New Year), Eid ul-Fitr, Eid ul-Adha, Durga Puja, and Language Movement Day.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Geography Section -->
        <section id="geography" class="content-section">
            <h2 class="section-title">Geography of Bangladesh</h2>
            <p>Bangladesh is a low-lying riverine country located on the fertile Bengal delta, with a largely marshy jungle coastline of 580 km along the Bay of Bengal.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1597589827221-9abc0c7f5cc6?ixlib=rb-4.0.3" alt="Rivers">
                    </div>
                    <div class="card-content">
                        <h3>River System</h3>
                        <p>Bangladesh is known as the "land of rivers" with over 700 rivers including the Ganges, Brahmaputra, and Meghna forming the world's largest delta.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1587517415894-87d13be53ff4?ixlib=rb-4.0.3" alt="Climate">
                    </div>
                    <div class="card-content">
                        <h3>Climate</h3>
                        <p>Bangladesh has a tropical monsoon climate with six distinct seasons. It's vulnerable to climate change, with frequent cyclones and flooding.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1592409065737-1d8f0c634b70?ixlib=rb-4.0.3" alt="Wildlife">
                    </div>
                    <div class="card-content">
                        <h3>Biodiversity</h3>
                        <p>The Sundarbans mangrove forest is home to the Royal Bengal Tiger. Bangladesh has numerous species of birds, fish, and the national animal is the Bengal tiger.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Economy Section -->
        <section id="economy" class="content-section">
            <h2 class="section-title">Economy of Bangladesh</h2>
            <p>Bangladesh has one of the fastest growing economies in the world. It has transformed from a primarily agricultural economy to one with significant manufacturing and service sectors.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1581988115590-baab13b4c6bb?ixlib=rb-4.0.3" alt="Garment Industry">
                    </div>
                    <div class="card-content">
                        <h3>Garment Industry</h3>
                        <p>Bangladesh is the world's second-largest apparel exporter after China. The ready-made garments sector accounts for more than 80% of exports.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1586511348099-32ae1ce1f5ff?ixlib=rb-4.0.3" alt="Agriculture">
                    </div>
                    <div class="card-content">
                        <h3>Agriculture</h3>
                        <p>Rice, jute, tea, wheat, sugarcane, potatoes, tobacco, and fruits are major agricultural products. Bangladesh is the fourth largest rice producer globally.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1573588028698-9a9a6dae2c17?ixlib=rb-4.0.3" alt="Remittance">
                    </div>
                    <div class="card-content">
                        <h3>Remittance</h3>
                        <p>Remittances from Bangladeshis working abroad, especially in the Middle East, play a significant role in the economy, accounting for about 6% of GDP.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Tourism Section -->
        <section id="tourism" class="content-section">
            <h2 class="section-title">Tourism in Bangladesh</h2>
            <p>Bangladesh offers diverse attractions including archaeological sites, historical mosques, beaches, forests, and wildlife sanctuaries.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1566549952257-37b685a5edf2?ixlib=rb-4.0.3" alt="Cox's Bazar">
                    </div>
                    <div class="card-content">
                        <h3>Cox's Bazar</h3>
                        <p>The world's longest natural sea beach, stretching 120 km along the Bay of Bengal. It's one of the most popular tourist destinations in Bangladesh.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1592409065737-1d8f0c634b70?ixlib=rb-4.0.3" alt="Sundarbans">
                    </div>
                    <div class="card-content">
                        <h3>Sundarbans</h3>
                        <p>The largest mangrove forest in the world, home to the Royal Bengal Tiger. It's a UNESCO World Heritage Site shared between Bangladesh and India.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1615551043360-33f08e6c9b0c?ixlib=rb-4.0.3" alt="Historical Sites">
                    </div>
                    <div class="card-content">
                        <h3>Historical Sites</h3>
                        <p>Bangladesh has numerous historical sites including the Sixty Dome Mosque, Lalbagh Fort, and Mahasthangarh - one of the earliest urban archaeological sites.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Education Section -->
        <section id="education" class="content-section">
            <h2 class="section-title">Education in Bangladesh</h2>
            <p>Bangladesh has made significant progress in education, with near universal primary education enrollment and gender parity in primary and secondary education.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-4.0.3" alt="Education System">
                    </div>
                    <div class="card-content">
                        <h3>Education System</h3>
                        <p>The education system is divided into primary, secondary, and higher education levels. The literacy rate has risen to over 74% as of 2020.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1524178232400-38d816f003ae?ixlib=rb-4.0.3" alt="Universities">
                    </div>
                    <div class="card-content">
                        <h3>Higher Education</h3>
                        <p>Bangladesh has over 150 universities, including the University of Dhaka, Bangladesh University of Engineering and Technology, and North South University.</p>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1584697964358-3e14ca57658b?ixlib=rb-4.0.3" alt="Digital Education">
                    </div>
                    <div class="card-content">
                        <h3>Digital Education</h3>
                        <p>The government has implemented digital education initiatives, including multimedia classrooms and online learning platforms to enhance education quality.</p>
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
                    <p><a href="#" class="nav-link" data-section="history">History</a></p>
                    <p><a href="#" class="nav-link" data-section="culture">Culture</a></p>
                    <p><a href="#" class="nav-link" data-section="geography">Geography</a></p>
                    <p><a href="#" class="nav-link" data-section="economy">Economy</a></p>
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
        // JavaScript for section navigation
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const contentSections = document.querySelectorAll('.content-section');
            
            // Function to show a specific section
            function showSection(sectionId) {
                contentSections.forEach(section => {
                    section.classList.remove('active');
                });
                
                document.getElementById(sectionId).classList.add('active');
                
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if(link.getAttribute('data-section') === sectionId) {
                        link.classList.add('active');
                    }
                });
            }
            
            // Add click event to navigation links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const sectionId = this.getAttribute('data-section');
                    showSection(sectionId);
                    
                    // Scroll to top
                    window.scrollTo({
                        top: 0,
                        behavior: 'smooth'
                    });
                });
            });
            
            // Make cards interactive
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
