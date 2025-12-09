# shopping
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dhruvi's TravelVerse - Your Journey Awaits</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(180deg, #f5e6f0 0%, #e8d5f2 50%, #f0e6f5 100%);
            color: #3a3a3a;
            overflow-x: hidden;
        }

        /* Header Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(255, 255, 255, 0.92);
            backdrop-filter: blur(10px);
            border-bottom: 2px solid rgba(200, 150, 200, 0.3);
            padding: 1.5rem 4rem;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 30px rgba(200, 150, 200, 0.1);
        }

        .logo {
            font-size: 2rem;
            font-weight: 900;
            background: linear-gradient(135deg, #b8568a, #a973c1, #b88cd4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: 2px;
            animation: logoBounce 2s ease-in-out infinite;
        }

        @keyframes logoBounce {
            0%, 100% { filter: drop-shadow(0 0 8px rgba(200, 150, 200, 0.3)); }
            50% { filter: drop-shadow(0 0 20px rgba(200, 150, 200, 0.7)); }
        }

        nav {
            display: flex;
            gap: 3rem;
            list-style: none;
        }

        nav a {
            color: #3a3a3a;
            text-decoration: none;
            font-size: 1rem;
            position: relative;
            transition: color 0.3s ease;
            font-weight: 500;
        }

        nav a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(135deg, #b8568a, #a973c1);
            transition: width 0.3s ease;
        }

        nav a:hover::before {
            width: 100%;
        }

        /* Hero Section - Two Column Layout */
        .hero {
            min-height: 100vh;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
            align-items: center;
            padding: 150px 80px 50px;
            background: linear-gradient(135deg, #f5e6f0 0%, #e8d5f2 50%, #f0e6f5 100%);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(200, 150, 200, 0.15) 0%, transparent 70%);
            border-radius: 50%;
            top: 10%;
            right: -100px;
            z-index: 0;
        }

        .hero::after {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(200, 150, 200, 0.08) 0%, transparent 70%);
            border-radius: 50%;
            bottom: 0;
            left: 5%;
            z-index: 0;
        }

        .hero-left {
            z-index: 1;
            animation: slideInLeft 0.8s ease-out;
        }

        @keyframes slideInLeft {
            from {
                opacity: 0;
                transform: translateX(-60px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .hero h1 {
            font-size: 5.5rem;
            font-weight: 900;
            margin-bottom: 25px;
            line-height: 1.1;
            background: linear-gradient(135deg, #b8568a, #a973c1, #b88cd4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            letter-spacing: -1px;
        }

        .hero p {
            font-size: 1.35rem;
            color: rgba(255, 255, 255, 0.85);
            margin-bottom: 40px;
            line-height: 1.8;
        }

        .btn {
            display: inline-block;
            padding: 18px 50px;
            background: linear-gradient(135deg, #b8568a, #a973c1);
            color: #3a3a3a;
            text-decoration: none;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 40px rgba(200, 150, 200, 0.3);
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 60px rgba(200, 150, 200, 0.6);
        }

        .btn:active {
            transform: scale(0.95);
        }

        .hero-right {
            z-index: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: slideInRight 0.8s ease-out 0.2s both;
        }

        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(60px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }

        .hero-image {
            width: 100%;
            max-width: 450px;
            height: 450px;
            background: url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=600&h=600&fit=crop');
            background-size: cover;
            background-position: center;
            border-radius: 25px;
            box-shadow: 0 30px 80px rgba(200, 150, 200, 0.35);
            border: 4px solid rgba(200, 150, 200, 0.3);
            position: relative;
            overflow: hidden;
            animation: imageFloat 3.5s ease-in-out infinite;
        }

        @keyframes imageFloat {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-30px); }
        }

        .hero-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(200, 150, 200, 0.1) 0%, transparent 100%);
            z-index: 1;
        }

        /* Destinations Section */
        .destinations {
            padding: 120px 80px;
            background: linear-gradient(180deg, rgba(26, 26, 46, 0.5) 0%, rgba(15, 22, 36, 0.5) 100%);
            position: relative;
        }

        .section-title {
            font-size: 3.8rem;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #b8568a, #a973c1);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            font-weight: 900;
            letter-spacing: -1px;
        }

        .section-subtitle {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 60px;
            max-width: 700px;
        }

        .destinations-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 35px;
        }

        .dest-card {
            background: rgba(255, 255, 255, 0.6);
            border: 2px solid rgba(200, 150, 200, 0.25);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.4s ease;
            cursor: pointer;
            backdrop-filter: blur(10px);
        }

        .dest-card:hover {
            transform: translateY(-15px);
            border-color: rgba(200, 150, 200, 0.6);
            box-shadow: 0 25px 60px rgba(200, 150, 200, 0.25);
        }

        .dest-image {
            width: 100%;
            height: 280px;
            background-size: cover;
            background-position: center;
            position: relative;
            overflow: hidden;
        }

        .dest-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(200, 150, 200, 0.2) 0%, transparent 100%);
        }

        .dest-info {
            padding: 28px 25px;
        }

        .dest-name {
            font-size: 1.9rem;
            margin-bottom: 8px;
            color: #b8568a;
            font-weight: 700;
        }

        .dest-rating {
            color: #b88cd4;
            font-size: 1.1rem;
            margin-bottom: 15px;
        }

        .dest-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .tag {
            display: inline-block;
            background: rgba(200, 150, 200, 0.15);
            color: #a973c1;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 0.85rem;
            border: 1px solid rgba(200, 150, 200, 0.3);
            transition: all 0.3s;
        }

        .tag:hover {
            background: rgba(200, 150, 200, 0.25);
            border-color: rgba(200, 150, 200, 0.5);
        }

        /* Videos Section */
        .videos {
            padding: 120px 80px;
            background: linear-gradient(180deg, rgba(15, 22, 36, 0.5) 0%, rgba(26, 26, 46, 0.5) 100%);
            position: relative;
        }

        .videos-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .video-card {
            background: rgba(255, 255, 255, 0.5);
            border: 2px solid rgba(200, 150, 200, 0.2);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .video-card:hover {
            border-color: rgba(200, 150, 200, 0.6);
            transform: scale(1.05);
            box-shadow: 0 20px 50px rgba(200, 150, 200, 0.25);
        }

        .video-wrapper {
            position: relative;
            width: 100%;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            background: #000;
        }

        .video-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }

        .video-info {
            padding: 22px;
            background: rgba(200, 150, 200, 0.08);
        }

        .video-info h3 {
            font-size: 1.5rem;
            color: #b8568a;
            margin-bottom: 8px;
            font-weight: 700;
        }

        .video-info p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.95rem;
            line-height: 1.5;
        }

        /* Features Section */
        .features {
            padding: 120px 80px;
            background: linear-gradient(180deg, rgba(26, 26, 46, 0.5) 0%, rgba(15, 22, 36, 0.5) 100%);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 35px;
            margin-top: 60px;
        }

        .feature-card {
            background: rgba(200, 150, 200, 0.06);
            border: 2px solid rgba(200, 150, 200, 0.2);
            border-radius: 18px;
            padding: 45px 30px;
            text-align: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }

        .feature-card:hover {
            border-color: rgba(200, 150, 200, 0.6);
            transform: translateY(-12px);
            box-shadow: 0 20px 50px rgba(200, 150, 200, 0.2);
        }

        .feature-icon {
            font-size: 4rem;
            margin-bottom: 20px;
            animation: iconPulse 2.5s ease-in-out infinite;
        }

        @keyframes iconPulse {
            0%, 100% { transform: translateY(0) scale(1); }
            50% { transform: translateY(-15px) scale(1.1); }
        }

        .feature-card h3 {
            font-size: 1.7rem;
            margin-bottom: 15px;
            color: #b8568a;
            font-weight: 700;
        }

        .feature-card p {
            color: rgba(255, 255, 255, 0.7);
            font-size: 1rem;
            line-height: 1.7;
        }

        /* Contact Section */
        .contact {
            padding: 120px 80px;
            background: linear-gradient(180deg, rgba(15, 22, 36, 0.5) 0%, rgba(26, 26, 46, 0.5) 100%);
            position: relative;
        }

        .contact::before {
            content: '';
            position: absolute;
            width: 600px;
            height: 600px;
            background: radial-gradient(circle, rgba(200, 150, 200, 0.1) 0%, transparent 70%);
            border-radius: 50%;
            top: -100px;
            right: -100px;
            z-index: 0;
        }

        .contact-container {
            position: relative;
            z-index: 1;
            max-width: 750px;
        }

        .contact form {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin-top: 50px;
        }

        .form-group.full {
            grid-column: 1 / -1;
        }

        .form-group input,
        .form-group textarea {
            padding: 16px;
            background: rgba(200, 150, 200, 0.08);
            border: 2px solid rgba(200, 150, 200, 0.3);
            color: #3a3a3a;
            border-radius: 10px;
            font-size: 1rem;
            font-family: inherit;
            transition: all 0.3s ease;
        }

        .form-group textarea {
            grid-column: 1 / -1;
            resize: vertical;
            min-height: 130px;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: rgba(200, 150, 200, 0.8);
            background: rgba(200, 150, 200, 0.12);
            box-shadow: 0 0 20px rgba(200, 150, 200, 0.2);
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255, 255, 255, 0.4);
        }

        /* Footer */
        footer {
            background: rgba(255, 255, 255, 0.95);
            border-top: 2px solid rgba(200, 150, 200, 0.4);
            padding: 70px 80px 30px;
            box-shadow: 0 -4px 30px rgba(200, 150, 200, 0.08);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 50px;
            margin-bottom: 50px;
        }

        .footer-section h3 {
            color: #b8568a;
            margin-bottom: 18px;
            font-size: 1.3rem;
            font-weight: 700;
        }

        .footer-section p,
        .footer-section a {
            color: rgba(255, 255, 255, 0.7);
            text-decoration: none;
            margin-bottom: 10px;
            transition: color 0.3s ease;
            font-size: 0.95rem;
            line-height: 1.8;
        }

        .footer-section a:hover {
            color: #b8568a;
        }

        .social-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .social-link {
            width: 45px;
            height: 45px;
            background: rgba(200, 150, 200, 0.15);
            border: 2px solid rgba(200, 150, 200, 0.4);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #b8568a;
            text-decoration: none;
            transition: all 0.3s ease;
            font-size: 1.3rem;
            font-weight: bold;
        }

        .social-link:hover {
            background: #b8568a;
            color: #3a3a3a;
            transform: scale(1.2) rotate(15deg);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(200, 150, 200, 0.2);
            color: rgba(255, 255, 255, 0.6);
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero {
                grid-template-columns: 1fr;
                padding: 150px 40px 50px;
                gap: 40px;
            }

            .hero h1 {
                font-size: 3rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .hero-image {
                max-width: 100%;
                height: 350px;
            }

            .destinations,
            .videos,
            .features,
            .contact,
            footer {
                padding: 80px 40px;
            }

            .section-title {
                font-size: 2.5rem;
            }

            nav {
                gap: 1.5rem;
                font-size: 0.85rem;
            }

            header {
                padding: 1rem 1.5rem;
            }

            .logo {
                font-size: 1.5rem;
            }

            .contact form {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="logo">🌍 Dhruvi's TravelVerse</div>
        <nav>
            <a href="#home">Home</a>
            <a href="#destinations">Destinations</a>
            <a href="#videos">Videos</a>
            <a href="#features">Why Us</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-left">
            <h1>Dhruvi's Journey Awaits</h1>
            <button class="btn">Start Exploring</button>
        </div>
        <div class="hero-right">
            <div class="hero-image"></div>
        </div>
    </section>

    <!-- Destinations Section -->
    <section class="destinations" id="destinations">
        <h2 class="section-title">Dhruvi's Favorite Destinations</h2>
        <p class="section-subtitle">Explore the world's most beautiful and enchanting destinations. Each one offers unique experiences and unforgettable memories curated by Dhruvi.</p>
        <div class="destinations-grid">
            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1537225228614-56cc3556d7ed?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Bali, Indonesia</h3>
                    <div class="dest-rating">⭐⭐⭐⭐⭐ (4.8/5)</div>
                    <div class="dest-tags">
                        <span class="tag">🏖️ Beaches</span>
                        <span class="tag">🎭 Culture</span>
                        <span class="tag">🥾 Hiking</span>
                    </div>
                </div>
            </div>

            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1511632765486-a01980e01a18?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Maldives</h3>
                    <div class="dest-rating">⭐⭐⭐⭐⭐ (4.9/5)</div>
                    <div class="dest-tags">
                        <span class="tag">🤿 Diving</span>
                        <span class="tag">💎 Luxury</span>
                        <span class="tag">🏝️ Tropical</span>
                    </div>
                </div>
            </div>

            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1502602898657-3e91760cbb34?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Paris, France</h3>
                    <div class="dest-rating">⭐⭐⭐⭐⭐ (4.7/5)</div>
                    <div class="dest-tags">
                        <span class="tag">🏛️ Museums</span>
                        <span class="tag">💕 Romance</span>
                        <span class="tag">🍷 Wine</span>
                    </div>
                </div>
            </div>

            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1540959375944-7049f642e9e0?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Tokyo, Japan</h3>
                    <div class="dest-rating">⭐⭐⭐⭐☆ (4.6/5)</div>
                    <div class="dest-tags">
                        <span class="tag">🏯 Culture</span>
                        <span class="tag">🍜 Food</span>
                        <span class="tag">🎆 Tech</span>
                    </div>
                </div>
            </div>

            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Swiss Alps</h3>
                    <div class="dest-rating">⭐⭐⭐⭐⭐ (4.8/5)</div>
                    <div class="dest-tags">
                        <span class="tag">⛷️ Skiing</span>
                        <span class="tag">⛰️ Mountains</span>
                        <span class="tag">🏔️ Nature</span>
                    </div>
                </div>
            </div>

            <div class="dest-card">
                <div class="dest-image" style="background-image: url('https://images.unsplash.com/photo-1570077189670-e3a8d69ac5ff?w=400&h=300&fit=crop');"></div>
                <div class="dest-info">
                    <h3 class="dest-name">Santorini, Greece</h3>
                    <div class="dest-rating">⭐⭐⭐⭐⭐ (4.9/5)</div>
                    <div class="dest-tags">
                        <span class="tag">🌅 Sunsets</span>
                        <span class="tag">⛵ Sailing</span>
                        <span class="tag">🏛️ History</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Videos Section -->
    <section class="videos" id="videos">
        <h2 class="section-title">Dhruvi's Travel Inspiration</h2>
        <p class="section-subtitle">Watch stunning travel videos and get inspired for your next journey around the world with Dhruvi's curated collection.</p>
        <div class="videos-grid">
            <div class="video-card">
                <div class="video-wrapper">
                    <iframe src="https://www.youtube.com/embed/2l9sJZl5Dgc" allowfullscreen="" loading="lazy"></iframe>
                </div>
                <div class="video-info">
                    <h3>Majestic Waterfalls</h3>
                    <p>Experience the power and beauty of nature's greatest waterfalls from around the globe.</p>
                </div>
            </div>

            <div class="video-card">
                <div class="video-wrapper">
                    <iframe src="https://www.youtube.com/embed/zSgiXGELjbc" allowfullscreen="" loading="lazy"></iframe>
                </div>
                <div class="video-info">
                    <h3>Mountain Peaks</h3>
                    <p>Discover breathtaking mountain landscapes and the adventurers who conquer them.</p>
                </div>
            </div>

            <div class="video-card">
                <div class="video-wrapper">
                    <iframe src="https://www.youtube.com/embed/i8LhIUHJyN8" allowfullscreen="" loading="lazy"></iframe>
                </div>
                <div class="video-info">
                    <h3>Tropical Paradise</h3>
                    <p>Escape to paradise with stunning tropical islands and crystal-clear waters.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features" id="features">
        <h2 class="section-title">Why Choose Dhruvi's TravelVerse?</h2>
        <p class="section-subtitle">We provide the best travel experiences with exclusive offers and expert guidance for all your adventures. Dhruvi's personal touch makes every journey special.</p>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">💰</div>
                <h3>Best Deals</h3>
                <p>Get exclusive discounts and special offers on flights, hotels, and tours worldwide.</p>
            </div>

            <div class="feature-card">
                <div class="feature-icon">🗺️</div>
                <h3>Expert Guides</h3>
                <p>Our travel experts help you plan the perfect itinerary for your dream destination.</p>
            </div>

            <div class="feature-card">
                <div class="feature-icon">🛡️</div>
                <h3>Safe & Secure</h3>
                <p>Travel with confidence with full protection and 24/7 customer support.</p>
            </div>

            <div class="feature-card">
                <div class="feature-icon">🌍</div>
                <h3>Global Coverage</h3>
                <p>Access to over 200 destinations with local expertise and international reach.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="contact-container">
            <h2 class="section-title">Plan Your Journey with Dhruvi</h2>
            <p class="section-subtitle">Get in touch with Dhruvi to start planning your next unforgettable adventure with personalized guidance.</p>
            <form>
                <div class="form-group">
                    <input type="text" placeholder="Full Name" required>
                </div>
                <div class="form-group">
                    <input type="email" placeholder="Email Address" required>
                </div>
                <div class="form-group">
                    <input type="tel" placeholder="Phone Number" required>
                </div>
                <div class="form-group">
                    <input type="text" placeholder="Dream Destination" required>
                </div>
                <div class="form-group full">
                    <textarea placeholder="Tell us about your travel preferences and dream vacation..." required></textarea>
                </div>
                <div class="form-group full">
                    <button type="submit" class="btn">Send My Inquiry</button>
                </div>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-grid">
            <div class="footer-section">
                <h3>About Dhruvi's TravelVerse</h3>
                <p>Dhruvi's ultimate destination for travel inspiration, planning, and unforgettable adventures around the world. We make travel accessible and magical for everyone.</p>
                <div class="social-links">
                    <a href="#" class="social-link">f</a>
                    <a href="#" class="social-link">𝕏</a>
                    <a href="#" class="social-link">📷</a>
                    <a href="#" class="social-link">▶️</a>
                </div>
            </div>

            <div class="footer-section">
                <h3>Quick Links</h3>
                <a href="#home">Home</a>
                <a href="#destinations">Destinations</a>
                <a href="#videos">Travel Videos</a>
                <a href="#features">Why Choose Us</a>
                <a href="#contact">Contact Us</a>
            </div>

            <div class="footer-section">
                <h3>Popular Routes</h3>
                <a href="#">Europe Explorer Pass</a>
                <a href="#">Asia Adventure Tour</a>
                <a href="#">Caribbean Cruise</a>
                <a href="#">Safari Experience</a>
                <a href="#">Mountain Expedition</a>
            </div>

            <div class="footer-section">
                <h3>Contact Information</h3>
                <p>📧 info@travelverse.com</p>
                <p>📞 +1 (800) 555-TRAVEL</p>
                <p>📍 123 Adventure Boulevard, Explorer City, EC 12345</p>
                <p>🕐 24/7 Customer Support Available</p>
            </div>
        </div>

        <div class="footer-bottom">
            <p>&copy; 2025 Dhruvi's TravelVerse. All Rights Reserved. | <a href="#" style="color: rgba(122,107,143,0.7);">Privacy Policy</a> | <a href="#" style="color: rgba(122,107,143,0.7);">Terms of Service</a></p>
        </div>
    </footer>

    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you! We will contact you with a custom quote soon.');
            this.reset();
        });
    </script>
</body>
</html>
