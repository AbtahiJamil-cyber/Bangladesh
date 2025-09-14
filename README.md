<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bangladesh: The Complete Guide</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Slab:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        :root {
            --primary: #006a4e;
            --secondary: #f42a41;
            --accent: #ff9933;
            --light: #f8f8f8;
            --dark: #333;
            --darker: #1a1a1a;
            --transition: all 0.3s ease;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header Styles */
        header {
            background: linear-gradient(to right, var(--primary), #008060);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.2);
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
            font-size: 0.95rem;
        }

        nav a:hover, nav a.active {
            background-color: rgba(255, 255, 255, 0.2);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1582573618381-932f6a8f3875?ixlib=rb-4.0.3') no-repeat center center/cover;
            color: white;
            text-align: center;
            padding: 100px 20px;
            margin-bottom: 40px;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            font-family: 'Roboto Slab', serif;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 14px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            font-size: 1.1rem;
            margin: 10px;
        }

        .btn:hover {
            background-color: #e21a32;
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid white;
        }

        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }

        /* Section Styles */
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--primary);
            position: relative;
            padding-bottom: 15px;
            font-size: 2.2rem;
            font-family: 'Roboto Slab', serif;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 5px;
            background-color: var(--secondary);
            border-radius: 2px;
        }

        .content-section {
            display: none;
            padding: 50px 0;
        }

        .content-section.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Card Styles */
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
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            height: 100%;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
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
            padding: 25px;
        }

        .card h3 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.4rem;
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
            transition: var(--transition);
        }

        .card-btn:hover {
            color: var(--secondary);
        }

        /* Quick Facts */
        .quick-facts {
            background-color: var(--primary);
            color: white;
            padding: 70px 0;
            margin: 70px 0;
        }

        .facts-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
        }

        .fact-box {
            text-align: center;
            padding: 20px;
        }

        .fact-box i {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .fact-box h3 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        /* Timeline */
        .history-timeline {
            margin: 50px 0;
            position: relative;
            padding: 20px 0;
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
            margin-bottom: 30px;
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
            width: 24px;
            height: 24px;
            background-color: var(--secondary);
            border-radius: 50%;
            border: 4px solid var(--primary);
        }

        .timeline-item:nth-child(odd)::after {
            right: -12px;
        }

        .timeline-item:nth-child(even)::after {
            left: -12px;
        }

        .timeline-content {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .timeline-content h3 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        /* Culture Grid */
        .culture-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }

        .culture-item {
            background: white;
            padding: 25px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .culture-item h3 {
            color: var(--primary);
            margin-bottom: 15px;
            font-size: 1.4rem;
        }

        /* Tabs */
        .tab-container {
            margin: 40px 0;
        }

        .tabs {
            display: flex;
            list-style: none;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .tabs li {
            margin-right: 5px;
        }

        .tabs a {
            display: block;
            padding: 12px 25px;
            background: #e0e0e0;
            color: #555;
            text-decoration: none;
            border-radius: 5px 5px 0 0;
            transition: var(--transition);
        }

        .tabs a.active {
            background: var(--primary);
            color: white;
        }

        .tab-content {
            display: none;
            background: white;
            padding: 30px;
            border-radius: 0 10px 10px 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .tab-content.active {
            display: block;
        }

        /* Table Styles */
        .data-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .data-table th, .data-table td {
            padding: 15px;
            text-align: left;
            border-bottom: 1px solid #eee;
        }

        .data-table th {
            background-color: var(--primary);
            color: white;
            font-weight: 600;
        }

        .data-table tr:hover {
            background-color: #f9f9f9;
        }

        /* Footer */
        footer {
            background-color: var(--darker);
            color: white;
            padding: 70px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-section h3 {
            color: var(--accent);
            margin-bottom: 20px;
            font-size: 1.5rem;
        }

        .footer-section p {
            margin-bottom: 15px;
            opacity: 0.9;
        }

        .social-icons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-icons a {
            color: white;
            font-size: 1.5rem;
            transition: var(--transition);
        }

        .social-icons a:hover {
            color: var(--accent);
            transform: translateY(-5px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid #555;
            opacity: 0.8;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .header-content {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                gap: 5px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero h1 {
                font-size: 2.8rem;
            }

            .hero p {
                font-size: 1.1rem;
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

        @media (max-width: 576px) {
            .logo-text {
                font-size: 1.5rem;
            }

            nav a {
                padding: 8px 12px;
                font-size: 0.85rem;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .btn {
                padding: 12px 25px;
                font-size: 1rem;
            }

            .section-title {
                font-size: 1.8rem;
            }
        }

        /* Back to Top Button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--primary);
            color: white;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
            transition: var(--transition);
            opacity: 0;
            visibility: hidden;
            z-index: 999;
        }

        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }

        .back-to-top:hover {
            background: var(--secondary);
            transform: translateY(-5px);
        }

        /* Search Box */
        .search-container {
            margin: 20px 0;
            display: flex;
            justify-content: center;
        }

        .search-box {
            display: flex;
            width: 100%;
            max-width: 500px;
        }

        .search-box input {
            flex: 1;
            padding: 12px 20px;
            border: 2px solid var(--primary);
            border-radius: 5px 0 0 5px;
            font-size: 1rem;
        }

        .search-box button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 0 20px;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            transition: var(--transition);
        }

        .search-box button:hover {
            background: var(--secondary);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: white;
            padding: 30px;
            border-radius: 10px;
            max-width: 500px;
            width: 90%;
            max-height: 80vh;
            overflow-y: auto;
        }

        .close-modal {
            float: right;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Accordion */
        .accordion {
            margin: 20px 0;
        }

        .accordion-item {
            margin-bottom: 10px;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .accordion-header {
            background: var(--primary);
            color: white;
            padding: 15px 20px;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .accordion-content {
            background: white;
            padding: 0;
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .accordion-content.active {
            padding: 20px;
            max-height: 300px;
        }

        /* Gallery */
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 15px;
            margin: 30px 0;
        }

        .gallery-item {
            height: 200px;
            overflow: hidden;
            border-radius: 8px;
            position: relative;
            cursor: pointer;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.1);
        }

        /* Map */
        .map-container {
            height: 400px;
            margin: 30px 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* Statistics */
        .stats-bar {
            background: #f0f0f0;
            height: 30px;
            border-radius: 15px;
            margin: 10px 0;
            overflow: hidden;
            position: relative;
        }

        .stats-progress {
            height: 100%;
            background: var(--primary);
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: flex-end;
            padding: 0 10px;
            color: white;
            font-weight: 600;
            min-width: 30%;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <div class="logo">
                <i class="fas fa-landmark"></i>
                <div class="logo-text">Bangladesh Explorer</div>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="nav-link active" data-section="home">Home</a></li>
                    <li><a href="#" class="nav-link" data-section="history">History</a></li>
                    <li><a href="#" class="nav-link" data-section="culture">Culture</a></li>
                    <li><a href="#" class="nav-link" data-section="geography">Geography</a></li>
                    <li><a href="#" class="nav-link" data-section="economy">Economy</a></li>
                    <li><a href="#" class="nav-link" data-section="tourism">Tourism</a></li>
                    <li><a href="#" class="nav-link" data-section="travel">Travel Info</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Discover the Beauty of Bangladesh</h1>
            <p>Explore the rich history, vibrant culture, and natural wonders of this South Asian gem. A complete guide for travelers and enthusiasts.</p>
            <a href="#" class="btn">Start Exploring</a>
            <a href="#" class="btn btn-outline">Travel Guide</a>
        </div>
    </section>

    <!-- Search Box -->
    <div class="container search-container">
        <div class="search-box">
            <input type="text" placeholder="Search for information about Bangladesh...">
            <button><i class="fas fa-search"></i></button>
        </div>
    </div>

    <!-- Main Content -->
    <main class="container">
        <!-- Home Section -->
        <section id="home" class="content-section active">
            <h2 class="section-title">Welcome to Bangladesh</h2>
            <p>Bangladesh, officially the People's Republic of Bangladesh, is a country in South Asia. It is the eighth-most populous country in the world, with a population exceeding 169 million people. Despite its small size, Bangladesh has a rich cultural heritage, diverse ecosystems, and a rapidly growing economy.</p>
            
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1591637333184-19aa84b3e01f?ixlib=rb-4.0.3" alt="Bangladesh Landscape">
                    </div>
                    <div class="card-content">
                        <h3>Geography & Nature</h3>
                        <p>Bangladesh is a riverine country located in South Asia with a coastline of 580 km along the Bay of Bengal. It is the 8th most populous country in the world and one of the most densely populated..</p>
                        <a href="#" class="card-btn">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1581988115590-baab13b4c6bb?ixlib=rb-4.0.3" alt="Bangladesh Culture">
                    </div>
                    <div class="card-content">
                        <h3>Rich Culture</h3>
                        <p>Bangladesh has a rich cultural heritage that encompasses literature, music, art, dance, and drama. The Bengali language has a rich literary heritage shared with the Indian state of West Bengal.</p>
                        <a href="#" class="card-btn">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1573588028698-9a9a6dae2c17?ixlib=rb-4.0.3" alt="Bangladesh Economy">
                    </div>
                    <div class="card-content">
                        <h3>Growing Economy</h3>
                        <p>Bangladesh is one of the fastest growing economies in the world. It has made significant strides in human development and poverty reduction. The garment industry is a major economic driver.</p>
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
            <h2 class="section-title">Must-Visit Attractions</h2>
            <div class="card-container">
                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1566549952257-37b685a5edf2?ixlib=rb-4.0.3" alt="Cox's Bazar">
                    </div>
                    <div class="card-content">
                        <h3>Cox's Bazar</h3>
                        <p>The world's longest natural sea beach, stretching 120 km along the Bay of Bengal. It's one of the most popular tourist destinations in Bangladesh with beautiful sandy beaches.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1592409065737-1d8f0c634b70?ixlib=rb-4.0.3" alt="Sundarbans">
                    </div>
                    <div class="card-content">
                        <h3>Sundarbans</h3>
                        <p>The largest mangrove forest in the world, home to the Royal Bengal Tiger. It's a UNESCO World Heritage Site shared between Bangladesh and India with unique biodiversity.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="card">
                    <div class="card-img">
                        <img src="https://images.unsplash.com/photo-1615551043360-33f08e6c9b0c?ixlib=rb-4.0.3" alt="Historical Sites">
                    </div>
                    <div class="card-content">
                        <h3>Historical Sites</h3>
                        <p>Bangladesh has numerous historical sites including the Sixty Dome Mosque, Lalbagh Fort, and Mahasthangarh - one of the earliest urban archaeological sites in South Asia.</p>
                        <a href="#" class="card-btn">Explore <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>

            <!-- Image Gallery -->
            <h2 class="section-title">Beautiful Bangladesh</h2>
            <div class="gallery">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3" alt="Rural Bangladesh">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1592409065737-1d8f0c634b70?ixlib=rb-4.0.3" alt="Sundarbans">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1582573618381-932f6a8f3875?ixlib=rb-4.0.3" alt="Cox's Bazar">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1615551043360-33f08e6c9b0c?ixlib=rb-4.0.3" alt="Historical Mosque">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1581988115590-baab13b4c6bb?ixlib=rb-4.0.3" alt="Tea Gardens">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3" alt="River Life">
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
                        <h3>Ancient Period (Pre-8th Century)</h3>
                        <p>Evidence of human settlement in Bangladesh dates back 4,000 years. The region was known as Gangaridai to the ancient Greeks and Romans. It was an important center of trade and culture.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Medieval Period (8th-18th Century)</h3>
                        <p>Islam was introduced in the 8th century. The Bengal Sultanate (1352–1576) was a major trading nation and one of Asia's wealthiest regions. The Mughal Empire later incorporated Bengal.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Colonial Era (1757-1947)</h3>
                        <p>The British East India Company established control in 1757 after the Battle of Plassey. Bengal was partitioned in 1905, creating the province of East Bengal and Assam.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Partition & Pakistan (1947-1971)</h3>
                        <p>Following the partition of India in 1947, Bangladesh became East Pakistan, separated by 1,600 km of Indian territory. Economic and cultural disparities led to growing tensions.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Liberation War (1971)</h3>
                        <p>The Bangladesh Liberation War in 1971 led to independence from Pakistan after nine months of conflict. Approximately 3 million people died during the war.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Modern Bangladesh (1971-Present)</h3>
                        <p>Since independence, Bangladesh has developed into a democratic, secular republic with significant economic growth despite political challenges and natural disasters.</p>
                    </div>
                </div>
            </div>

            <h3 class="section-title">Key Historical Events</h3>
            
            <div class="accordion">
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>Language Movement (1952)</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>The Bengali Language Movement was a political movement in East Pakistan advocating for the recognition of the Bengali language. On February 21, 1952, students protesting for the right to use their mother tongue were shot and killed by police. This day is now commemorated as International Mother Language Day.</p>
                    </div>
                </div>
                
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>Six-Point Movement (1966)</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>The Six Point Movement was led by Sheikh Mujibur Rahman and called for greater autonomy for East Pakistan. The six points included demands for a federal government, separate currencies, and separate military for East Pakistan.</p>
                    </div>
                </div>
                
                <div class="accordion-item">
                    <div class="accordion-header">
                        <span>Liberation War (1971)</span>
                        <i class="fas fa-chevron-down"></i>
                    </div>
                    <div class="accordion-content">
                        <p>The Bangladesh Liberation War was a revolution and armed conflict sparked by the rise of the Bengali nationalist and self-determination movement in East Pakistan. The war resulted in the independence of Bangladesh. The conflict saw widespread atrocities and genocide.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Culture Section -->
        <section id="culture" class="content-section">
            <h2 class="section-title">Culture of Bangladesh</h2>
            
বাংলাদেশের সংস্কৃতি
ভূমিকা
বাংলাদেশ—নদীমাতৃক, সবুজে ঘেরা, প্রাণবন্ত এক দেশ। প্রাকৃতিক সৌন্দর্যের পাশাপাশি এই দেশ সমৃদ্ধ তার ঐতিহ্য, ভাষা, সাহিত্য, শিল্পকলা, সংগীত, উৎসব ও আচার-অনুষ্ঠানে। শত শত বছরের ইতিহাস, সংগ্রাম আর সৃজনশীলতা বাংলাদেশের সংস্কৃতিকে দিয়েছে এক অনন্য রূপ। এই সংস্কৃতি একই সাথে ঐক্যের প্রতীক এবং বৈচিত্র্যের সৌন্দর্য।

অধ্যায় ১: ভাষা ও পরিচয়
বাংলা ভাষা: আমাদের সংস্কৃতির প্রাণকেন্দ্র।

১৯৫২ সালের ভাষা আন্দোলন: মাতৃভাষার অধিকার প্রতিষ্ঠায় শহীদের আত্মত্যাগ বিশ্বজুড়ে উদাহরণ। এই সংগ্রামের ফলেই ২১ ফেব্রুয়ারি এখন আন্তর্জাতিক মাতৃভাষা দিবস।

বাংলা সাহিত্যে রবীন্দ্রনাথ ঠাকুর, কাজী নজরুল ইসলাম, জীবনানন্দ দাশ, জসীমউদ্দীন প্রমুখ কবি-সাহিত্যিকের অবদান বিশ্বমানের।

অধ্যায় ২: ধর্ম ও আধ্যাত্মিকতা
বাংলাদেশের সংখ্যাগরিষ্ঠ জনগণ মুসলিম; তাই ঈদ-উল-ফিতর ও ঈদ-উল-আযহা আমাদের জাতীয় জীবনের প্রধান উৎসব।

হিন্দু সম্প্রদায়ের দুর্গাপূজা, সরস্বতী পূজা ও জন্মাষ্টমী সমানভাবে গুরুত্ব পায়।

বৌদ্ধ ও খ্রিস্টান ধর্মাবলম্বীরাও নিজস্ব উৎসব—বুদ্ধ পূর্ণিমা, বড়দিন ইত্যাদি পালন করেন।

লোকবিশ্বাস, পীর-আউলিয়ার মাজার সংস্কৃতি এবং গ্রামীণ আচার-অনুষ্ঠানও আধ্যাত্মিক জীবনের গুরুত্বপূর্ণ অংশ।

অধ্যায় ৩: উৎসব ও আনন্দ
পহেলা বৈশাখ: বাংলা নববর্ষের উৎসব—ঢাকায় মঙ্গল শোভাযাত্রা, গ্রামে-গঞ্জে মেলা, পান্তা-ইলিশের আয়োজন।

ঈদ উৎসব: পরিবার-পরিজন একত্রিত হয়ে আনন্দ ভাগাভাগি করার সময়।

দুর্গাপূজা: শিল্পকলা, ভক্তি ও আনন্দের মেলবন্ধন।

স্থানীয় নবান্ন, পৌষসংক্রান্তি, চড়ক পূজা ইত্যাদিও গ্রামীণ সংস্কৃতির রঙিন অংশ।

অধ্যায় ৪: লোকসংস্কৃতি ও শিল্পকলা
লোকসংগীত: ভাটিয়ালি, বাউল, জারি-সারি, ভাওয়াইয়া—যা গ্রামীণ জীবনের কথা বলে।

নৃত্য: জাতিগত গোষ্ঠীগুলোর নাচ যেমন—চাকমা, গারো, মারমা ইত্যাদির নৃত্য।

হস্তশিল্প: জামদানি, নকশিকাঁথা, মৃৎশিল্প, বেত ও বাঁশের কাজ।

চিত্রকলা ও আধুনিক শিল্প: জয়নুল আবেদীন ও কামরুল হাসান প্রমুখ শিল্পীর সৃষ্টিকর্ম আন্তর্জাতিক খ্যাতি পেয়েছে।

অধ্যায় ৫: খাদ্যসংস্কৃতি
ভাত ও মাছ বাঙালির প্রধান খাদ্য।

পান্তা-ইলিশ, খিচুড়ি, ভর্তা, পিঠা-পুলি আমাদের বিশেষ ঐতিহ্য।

মিষ্টি—রসগোল্লা, সন্দেশ, মিষ্টি দই ইত্যাদি আন্তর্জাতিকভাবে সমাদৃত।

অধ্যায় ৬: পোশাক ও জীবনধারা
নারীদের ঐতিহ্যবাহী পোশাক শাড়ি, পুরুষদের জন্য লুঙ্গি ও পাঞ্জাবি।

আধুনিক প্রভাবেও পোশাকে পরিবর্তন এসেছে, তবে উৎসব ও বিশেষ দিনে ঐতিহ্যবাহী পোশাক এখনো জনপ্রিয়।

উপসংহার
বাংলাদেশের সংস্কৃতি মূলত এক প্রাণবন্ত মিলনমেলা—ভাষা, ধর্ম, শিল্প, সংগীত, উৎসব, খাদ্য, ও লোকঐতিহ্যের। এই সংস্কৃতি আমাদের পরিচয়, আমাদের শক্তি, আর আমাদের গর্ব।


            <p>Bangladesh has a rich, diverse cultural heritage that encompasses literature, music, dance, drama, art, craft, folklore, and philosophy. The culture of Bangladesh is influenced by Hindu, Buddhist, and Islamic traditions.</p>
            
            <div class="culture-grid">
                <div class="culture-item">
                    <h3><i class="fas fa-utensils"></i> Cuisine</h3>
                    <p>.</p>
                </div>
                <div class="culture-item">
                    <h3><i class="fas fa-tshirt"></i> Traditional Clothing</h3>
                    <p>Traditional attire includes sarees for women and lungi or panjabi for men. The nakshi kantha is a traditional embroidered quilt. During festivals, people often wear traditional dresses like sharis for women and punjabis for men.</p>
                </div>
                <div class="culture-item">
                    <h3><i class="fas fa-music"></i> Music & Dance</h3>
                    <p>Traditional music includes Baul, Bhatiali, and folk songs. Rabindra Sangeet (songs by Rabindranath Tagore) and Nazrul Geeti (songs by Kazi Nazrul Islam) are also popular. Traditional dances include the manipuri and santal dances.</p>
                </div>
                <div class="culture-item">
                    <h3><i class="fas fa-glass-cheers"></i> Festivals</h3>
                    <p>Major festivals include Pohela Boishakh (Bengali New Year), Eid ul-Fitr, Eid ul-Adha, Durga Puja, and Language Movement Day. These festivals are celebrated with great enthusiasm across the country.</p>
                </div>
                <div class="culture-item">
                    <h3><i class="fas fa-book"></i> Literature</h3>
                    <p>Bengali literature has a rich heritage with Nobel laureate Rabindranath Tagore and national poet Kazi Nazrul Islam. The Ekushey Book Fair is the largest book fair in the Bengali-speaking world.</p>
                </div>
                <div class="culture-item">
                    <h3><i class="fas fa-handshake"></i> Social Customs</h3>
                    <p>
