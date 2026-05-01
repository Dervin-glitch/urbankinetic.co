<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Urbankinetic - Streetwear Indonesia</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Bebas+Neue&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #1a1a1a;
            --secondary: #ff6b35;
            --accent: #f8f9fa;
            --text: #333;
            --text-light: #666;
            --white: #fff;
            --shadow: 0 10px 30px rgba(0,0,0,0.1);
            --shadow-lg: 0 25px 50px rgba(0,0,0,0.15);
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text);
            overflow-x: hidden;
        }

        /* ========================================
           DESKTOP HEADER (1024px+) 
        ======================================== */
        @media (min-width: 1024px) {
            .header {
                position: fixed;
                top: 0;
                width: 100%;
                background: rgba(255,255,255,0.98);
                backdrop-filter: blur(20px);
                z-index: 1000;
                padding: 1.5rem 0;
                transition: all 0.3s ease;
                box-shadow: 0 2px 20px rgba(0,0,0,0.08);
            }

            .nav-container {
                max-width: 1600px;
                margin: 0 auto;
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 0 4rem;
            }

            .logo {
                font-size: 2.5rem;
                font-weight: 800;
                background: linear-gradient(135deg, var(--primary), var(--secondary));
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
                font-family: 'Bebas Neue', sans-serif;
                letter-spacing: 2px;
                text-decoration: none;
            }

            .nav-menu {
                display: flex !important;
                list-style: none;
                gap: 3rem;
            }

            .nav-menu a {
                text-decoration: none;
                color: var(--text);
                font-weight: 600;
                font-size: 1.1rem;
                position: relative;
                transition: all 0.3s ease;
                padding: 0.5rem 0;
            }

            .nav-menu a::after {
                content: '';
                position: absolute;
                width: 0;
                height: 3px;
                bottom: 0;
                left: 50%;
                background: var(--secondary);
                transition: all 0.3s ease;
                transform: translateX(-50%);
            }

            .nav-menu a:hover::after {
                width: 100%;
            }

            .header-actions {
                display: flex;
                align-items: center;
                gap: 2rem;
            }

            .header-actions button {
                background: var(--secondary);
                color: white;
                border: none;
                padding: 0.8rem 2rem;
                border-radius: 50px;
                font-weight: 600;
                cursor: pointer;
                transition: all 0.3s ease;
            }

            .header-actions button:hover {
                transform: translateY(-2px);
                box-shadow: var(--shadow);
            }
        }

        /* ========================================
           MOBILE HEADER (1023px-) 
        ======================================== */
        @media (max-width: 1023px) {
            .header {
                position: fixed;
                top: 0;
                width: 100%;
                background: rgba(26,26,26,0.95);
                backdrop-filter: blur(20px);
                z-index: 1000;
                padding: 1rem 0;
            }

            .nav-container {
                max-width: 1400px;
                margin: 0 auto;
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 0 1.5rem;
            }

            .logo {
                font-size: 1.8rem;
                font-weight: 800;
                color: white;
                font-family: 'Bebas Neue', sans-serif;
                letter-spacing: 1px;
            }

            .mobile-menu-btn {
                display: flex !important;
                flex-direction: column;
                cursor: pointer;
                gap: 5px;
                z-index: 1001;
            }

            .mobile-menu-btn span {
                width: 28px;
                height: 3px;
                background: white;
                transition: 0.3s;
                border-radius: 2px;
            }

            .mobile-menu-btn.active span:nth-child(1) {
                transform: rotate(45deg) translate(6px, 6px);
            }

            .mobile-menu-btn.active span:nth-child(2) {
                opacity: 0;
            }

            .mobile-menu-btn.active span:nth-child(3) {
                transform: rotate(-45deg) translate(6px, -6px);
            }

            .mobile-menu {
                position: fixed;
                top: 0;
                right: -100%;
                width: 80%;
                max-width: 400px;
                height: 100vh;
                background: var(--primary);
                transition: right 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
                z-index: 1000;
                padding: 5rem 2rem 2rem;
            }

            .mobile-menu.active {
                right: 0;
            }

            .mobile-menu ul {
                list-style: none;
            }

            .mobile-menu a {
                display: block;
                color: white;
                text-decoration: none;
                font-size: 1.3rem;
                font-weight: 600;
                padding: 1rem 0;
                border-bottom: 1px solid rgba(255,255,255,0.1);
            }

            .mobile-actions {
                margin-top: 2rem;
                display: flex;
                flex-direction: column;
                gap: 1rem;
            }

            .mobile-actions button {
                background: var(--secondary);
                color: white;
                border: none;
                padding: 1rem;
                border-radius: 12px;
                font-size: 1.1rem;
                font-weight: 600;
            }
        }

        /* ========================================
           DESKTOP HERO (1024px+) 
        ======================================== */
        @media (min-width: 1024px) {
            .hero {
                height: 100vh;
                background: linear-gradient(135deg, rgba(26,26,26,0.8), rgba(0,0,0,0.6)), 
                            url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1920 1080"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="25" cy="25" r="1" fill="%23fff" opacity="0.1"/><circle cx="75" cy="75" r="0.5" fill="%23ff6b35" opacity="0.2"/></pattern></defs><rect width="1920" height="1080" fill="url(%23grain)"/><rect fill="%231a1a1a" width="1920" height="1080" opacity="0.9"/><text x="50%" y="45%" font-family="Bebas Neue, sans-serif" font-size="140" fill="%23ff6b35" text-anchor="middle" font-weight="700" letter-spacing="0.1em">URBANKINETIC</text><text x="50%" y="55%" font-family="Inter, sans-serif" font-size="32" fill="%23fff" text-anchor="middle" opacity="0.9">STREETWEAR FROM INDONESIA</text></svg>');
                background-size: cover;
                background-position: center;
                display: flex;
                align-items: center;
                justify-content: center;
                text-align: center;
                color: white;
                position: relative;
            }

            .hero-content {
                max-width: 800px;
                padding: 0 2rem;
            }

            .hero-content h1 {
                font-size: clamp(4rem, 10vw, 8rem);
                font-weight: 800;
                margin-bottom: 1.5rem;
                font-family: 'Bebas Neue', sans-serif;
                letter-spacing: 0.05em;
                text-shadow: 0 4px 20px rgba(0,0,0,0.5);
                line-height: 0.9;
            }

            .hero-content p {
                font-size: 1.8rem;
                margin-bottom: 3rem;
                opacity: 0.95;
                font-weight: 300;
            }

            .hero-buttons {
                display: flex;
                gap: 1.5rem;
                justify-content: center;
                flex-wrap: wrap;
            }
        }

        /* ========================================
           MOBILE HERO (1023px-) 
        ======================================== */
        @media (max-width: 1023px) {
            .hero {
                height: 100vh;
                background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 50%, #ff6b35 100%);
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                text-align: center;
                color: white;
                padding: 0 1.5rem;
                position: relative;
                overflow: hidden;
            }

            .hero::before {
                content: '';
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 400"><circle cx="100" cy="100" r="3" fill="%23ff6b35" opacity="0.3"/><circle cx="300" cy="200" r="2" fill="white" opacity="0.4"/><circle cx="50" cy="300" r="1.5" fill="%23ff6b35" opacity="0.2"/></svg>');
                animation: float 20s infinite linear;
            }

            @keyframes float {
                0%, 100% { transform: translateY(0px) rotate(0deg); }
                33% { transform: translateY(-20px) rotate(120deg); }
                66% { transform: translateY(-10px) rotate(240deg); }
            }

            .hero-content h1 {
                font-size: clamp(2.5rem, 12vw, 4rem);
                font-weight: 800;
                margin-bottom: 1rem;
                font-family: 'Bebas Neue', sans-serif;
            }

            .hero-content p {
                font-size: 1.2rem;
                margin-bottom: 2rem;
                opacity: 0.9;
            }

            .cta-button {
                display: block;
                background: var(--secondary);
                color: white;
                padding: 1.2rem 3rem;
                text-decoration: none;
                font-weight: 700;
                border-radius: 50px;
                font-size: 1.1rem;
                transition: all 0.3s ease;
                box-shadow: 0 10px 30px rgba(255,107,53,0.4);
                text-transform: uppercase;
                letter-spacing: 1px;
            }

            .cta-button:hover {
                transform: scale(1.05);
            }
        }

        /* ========================================
           PRODUCTS SECTION - DESKTOP 
        ======================================== */
        @media (min-width: 1024px) {
            .products-section {
                padding: 10rem 4rem 6rem;
                max-width: 1600px;
                margin: 0 auto;
            }

            .section-header {
                text-align: center;
                margin-bottom: 5rem;
            }

            .section-title {
                font-size: 4rem;
                font-weight: 800;
                margin-bottom: 1rem;
                background: linear-gradient(135deg, var(--primary), var(--secondary));
                -webkit-background-clip: text;
                -webkit-text-fill-color: transparent;
                font-family: 'Bebas Neue', sans-serif;
                letter-spacing: 0.02em;
            }

            .section-subtitle {
                font-size: 1.3rem;
                color: var(--text-light);
                font-weight: 300;
            }

            .products-grid {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
                gap: 3rem;
            }

            .product-card {
                background: white;
                border-radius: 24px;
                overflow: hidden;
                box-shadow: var(--shadow);
                transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
                position: relative;
                height: 520px;
            }

            .product-card:hover {
                transform: translateY(-15px) scale(1.02);
                box-shadow: var(--shadow-lg);
            }

            .product-image {
                height: 350px;
                position: relative;
                overflow: hidden;
            }

            .product-image img {
                width: 100%;
                height: 100%;
                object-fit: cover;
                transition: transform 0.6s ease;
            }

            .product-card:hover .product-image img {
                transform: scale(1.1);
            }

            .product-badge {
                position: absolute;
                top: 20px;
                left: 20px;
                background: var(--secondary);
                color: white;
                padding: 0.5rem 1rem;
                border-radius: 20px;
                font-size: 0.8rem;
                font-weight: 700;
                text-transform: uppercase;
                letter-spacing: 0.5px;
            }

            .product-info {
                padding: 2rem;
            }

            .product-name {
                font-size: 1.4rem;
                font-weight: 700;
                margin-bottom: 0.5rem;
                line-height: 1.3;
            }

            .product-price {
                font-size: 1.8rem;
                font-weight: 800;
                color: var(--primary);
                margin-bottom: 1rem;
            }

            .add-to-cart {
                width: 100%;
                background: var(--secondary);
                color: white;
                border: none;
                padding: 1rem;
                border-radius: 12px;
                font-weight: 600;
                font-size: 1rem;
                cursor: pointer;
                transition: all 0.3s ease;
            }

            .add-to-cart:hover {
                background: #e55a2b;
                transform: translateY(-2px);
            }
        }

        /* ========================================
           PRODUCTS SECTION - MOBILE 
        ======================================== */
        @media (max-width: 1023px) {
            .products-section {
                padding: 6rem 1.5rem 4rem;
            }

            .section-title {
                font-size: 2.5rem;
                margin-bottom: 2rem;
            }

            .products-grid {
                display: flex;
                flex-direction: column;
                gap: 2rem;
            }

            .product-card {
                border-radius: 20px;
                height: 420px;
                box-shadow: var(--shadow);
            }

            .product-image {
                height: 280px;
            }

            .product-info {
                padding: 1.5rem;
            }

            .product-name {
                font-size: 1.2rem;
            }

            .product-price {
                font-size: 1.5rem;
            }
        }

        /* ========================================
           COLLECTIONS - DESKTOP 
        ======================================== */
        @media (min-width: 1024px) {
            .collections {
                padding: 10rem 4rem;
                background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            }

            .collections-grid {
                display: grid;
                grid-template-columns: repeat(3, 1fr);
                gap: 3rem;
                margin-top: 5rem;
            }

            .collection-card {
                height: 500px;
                border-radius: 24px;
                overflow: hidden;
                position: relative;
                cursor: pointer;
                transition: all 0.5s ease;
            }

            .collection-card:hover {
                transform: translateY(-10px) scale(1.02);
            }

            .collection-overlay {
                position: absolute;
                inset: 0;
                background: linear-gradient(135deg, rgba(26,26,26,0.9), rgba(0,0,0,0.7));
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                color: white;
                opacity: 0;
                transition: opacity 0.4s ease;
                text-align: center;
                padding: 0 2rem;
            }

            .collection-card:hover .collection-overlay {
                opacity: 1;
            }

            .collection-title {
                font-size: 3.5rem;
                font-weight: 800;
                margin-bottom: 1rem;
                font-family: 'Bebas Neue', sans-serif;
                letter-spacing: 0.02em;
            }
        }

        /* ========================================
           COLLECTIONS - MOBILE 
        ======================================== */
        @media (max-width: 1023px) {
            .collections {
                padding: 6rem 1.5rem;
            }

            .collections-grid {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            .collection-card {
                height: 400px;
            }

            .collection-title {
                font-size: 2.5rem;
            }
        }

        /* ========================================
           FOOTER - DESKTOP 
        ======================================== */
        @media (min-width: 1024px) {
            .footer {
                background: var(--primary);
                color: white;
                padding: 6rem 4rem 3rem;
            }

            .footer-content {
                display: grid;
                grid-template-columns: repeat(4, 1fr);
                gap: 4rem;
                margin-bottom: 3rem;
                max-width: 1600px;
                margin: 0 auto 3rem;
            }
        }

        /* ========================================
           FOOTER - MOBILE 
        ======================================== */
        @media (max-width: 1023px) {
            .footer {
                padding: 4rem 1.5rem 2rem;
            }

            .footer-content {
                grid-template-columns: 1fr;
                gap: 2rem;
                text-align: center;
            }

            .newsletter-form {
                display: flex;
                flex-direction: column;
                gap: 1rem;
                max-width: 400px;
                margin: 0 auto;
            }

            .newsletter-form input {
                padding: 1rem;
                border: 2px solid #444;
                border-radius: 12px;
                background: rgba(255,255,255,0.1);
                color: white;
                font-size: 1rem;
            }

            .newsletter-form input::placeholder {
                color: #ccc;
            }

            .newsletter-form button {
                background: var(--secondary);
                color: white;
                border: none;
                padding: 1rem;
                border-radius: 12px;
                font-weight: 600;
                font-size: 1rem;
            }
        }

        /* ========================================
           CART MODAL - DESKTOP 
        ======================================== */
        @media (min-width: 1024px) {
            .cart-modal {
                position: fixed;
                top: 120px;
                right: 4rem;
                width: 450px;
                max-height: 80vh;
                background: white;
                border-radius: 24px;
                box-shadow: var(--shadow-lg);
                transform: translateX(500px);
                transition: transform 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
                z-index: 2000;
                overflow: hidden;
            }

            .cart-modal.active {
                transform: translateX(0);
            }
        }

        /* ========================================
           CART MODAL - MOBILE 
        ======================================== */
        @media (max-width: 1023px) {
            .cart-modal {
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;
                background: rgba(0,0,0,0.95);
                backdrop-filter: blur(20px);
                transform: translateY(100%);
                transition: transform 0.4s ease;
                z-index: 2000;
                border-radius: 0;
            }

            .cart-modal.active {
                transform: translateY(0);
            }

            .cart-modal-content {
                margin: 0;
                height: 100%;
                border-radius: 0;
                overflow-y: auto;
            }
        }

        .cart-header {
            padding: 2rem;
            border-bottom: 1px solid #eee;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .cart-item {
            display: flex;
            gap: 1rem;
            padding: 1.5rem 2rem;
            border-bottom: 1px solid #f0f0f0;
        }

        .cart-item img {
            width: 80px;
            height: 80px;
            border-radius: 12px;
            object-fit: cover;
        }

        .cart-total {
            padding: 2rem;
            font-size: 1.5rem;
            font-weight: 700;
            border-top: 2px solid #f0f0f0;
        }

        .checkout-btn {
            width: 100%;
            background: var(--secondary);
            color: white;
            border: none;
            padding: 1.5rem;
            border-radius: 12px;
            font-size: 1.2rem;
            font-weight: 700;
            cursor: pointer;
            margin-top: 1rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(40px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .animate {
            animation: fadeInUp 0.8s ease forwards;
        }

        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #f1f1f1;
        }

        ::-webkit-scrollbar-thumb {
            background: var(--secondary);
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <!-- DESKTOP/MOBILE HEADER -->
    <header class="header" id="header">
        <div class="nav-container">
            <!-- LOGO -->
            <a href="#" class="logo">URBANKINETIC</a>

            <!-- DESKTOP NAV -->
            <ul class="nav-menu" id="desktopNav">
                <li><a href="#home">Home</a></li>
                <li><a href="#products">Products</a></li>
                <li><a href="#collections">Collections</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

            <!-- MOBILE MENU BUTTON -->
            <div class="mobile-menu-btn" id="mobileMenuBtn">
                <span></span>
                <span></span>
                <span></span>
            </div>

            <!-- MOBILE MENU -->
            <div class="mobile-menu" id="mobileMenu">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#collections">Collections</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="mobile-actions">
                    <button>Login</button>
                    <button style="background: var(--secondary);">Cart (3)</button>
                </div>
            </div>

            <!-- DESKTOP ACTIONS -->
            <div class="header-actions" id="desktopActions">
                <i class="fas fa-search" style="font-size: 1.3rem; cursor: pointer; color: var(--text);"></i>
                <button>Cart (3)</button>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>URBANKINETIC</h1>
            <p>Streetwear Indonesia<br>Built for the Culture</p>
            <div class="hero-buttons">
                <a href="#products" class="cta-button">Shop Now</a>
                <a href="#collections" class="cta-button" style="background: transparent; border: 2px solid white;">View Collections</a>
            </div>
        </div>
    </section>

    <!-- PRODUCTS SECTION -->
    <section class="products-section" id="products">
        <div class="section-header">
            <h2 class="section-title">Featured Products</h2>
            <p class="section-subtitle">Latest drops you need to cop</p>
        </div>
        <div class="products-grid">
            <div class="product-card animate">
                <div class="product-image">
                    <div class="product-badge">New</div>
                    <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 350'><rect fill='%23ff6b35' x='10%' y='10%' width='80%' height='80%' rx='25'/><text x='50%' y='55%' font-family='Inter,sans-serif' font-size='28' fill='%23fff' text-anchor='middle' font-weight='700'>HOODIE</text></svg>" alt="Hoodie">
                </div>
                <div class="product-info">
                    <h3 class="product-name">Urban Kinetic Hoodie</h3>
                    <div class="product-price">Rp 899.000</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card animate">
                <div class="product-image">
                    <div class="product-badge">Hot</div>
                    <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 400 350'><rect fill='%231a1a1a' x='15%' y='15%' width='70%' height='70%' rx='20'/><circle cx='50%' cy='35%' r='20%' fill='%23ff6b35'/><text x='50%' y='75%' font-family='Inter,sans-serif' font-size='26' fill='%23fff' text-anchor='middle'>SNKR</text></svg>" alt="Sneakers">
                </div>
                <div class="product-info">
                    <h3 class="product-name">Kinetic Runners</h3>
                    <div class="product-price">Rp 1.299.000</div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <!-- Add more products... -->
        </div>
    </section>

    <!-- COLLECTIONS -->
    <section class="collections" id="collections">
        <div class="products-section">
            <div class="section-header">
                <h2 class="section-title">Collections</h2>
                <p class="section-subtitle">Discover our latest collections</p>
            </div>
            <div class="collections-grid">
                <div class="collection-card animate" style="background: linear-gradient(-45deg, #1a1a1a, #2d2d2d);">
                    <div class="collection-overlay">
                        <h3 class="collection-title">STREET</h3>
                        <p>Classic streetwear essentials for everyday</p>
                    </div>
                </div>
                <div class="collection-card animate" style="background: linear-gradient(-45deg, #ff6b35, #ff8e60);">
                    <div class="collection-overlay">
                        <h3 class="collection-title">LIMITED</h3>
                        <p>Exclusive drops - gone in seconds</p>
                    </div>
                </div>
                <div class="collection-card animate" style="background: linear-gradient(-45deg, #f8f9fa, #e9ecef);">
                    <div class="collection-overlay">
                        <h3 class="collection-title">ESSENTIALS</h3>
                        <p>Timeless pieces for every rotation</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer" id="contact">
        <div class="footer-content">
            <div>
                <h3 style="font-family: 'Bebas Neue'; font-size: 2rem; margin-bottom: 1rem;">URBANKINETIC</h3>
                <p>Streetwear brand from Indonesia, built for the streets.</p>
                <div style="margin-top: 1.5rem; display: flex; gap: 1rem;">
                    <a href="#" style="color: #ccc; font-size: 1.5rem;"><i class="fab fa-instagram"></i></a>
                    <a href="#" style="color: #ccc; font-size: 1.5rem;"><i class="fab fa-tiktok"></i></a>
                    <a href="#" style="color: #ccc; font-size: 1.5rem;"><i class="fab fa-twitter"></i></a>
                </div>
            </div>
            <div>
                <h3>Quick Links</h3>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">New Arrivals</a>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">Collections</a>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">Track Order</a>
            </div>
            <div>
                <h3>Support</h3>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">FAQ</a>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">Shipping</a>
                <a href="#" style="display: block; margin-bottom: 0.8rem; color: #ccc;">Returns</a>
            </div>
            <div class="newsletter-form">
                <h3>Stay Updated</h3>
                <input type="email" placeholder="Enter your email">
                <button>Subscribe</button>
            </div>
        </div>
        <div style="text-align: center; padding-top: 3rem; color: #999; border-top: 1px solid #333;">
            <p>&copy; 2024 Urbankinetic. Made in Indonesia 🇮🇩</p>
        </div>
    </footer>

    <!-- CART MODAL -->
    <div class="cart-modal" id="cartModal">
        <div class="cart-modal-content">
            <div class="cart-header">
                <h2 style="margin: 0;"><i class="fas fa-shopping-bag"></i> Shopping Cart</h2>
                <i class="fas fa-times" style="font-size: 1.5rem; cursor: pointer;" onclick="closeCart()"></i>
            </div>
            <div style="max-height: 400px; overflow-y: auto;">
                <div class="cart-item">
                    <img src="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' width='80' height='80' viewBox='0 0 80 80'><rect fill='%23ff6b35' rx='8' width='80' height='80'/></svg>" alt="Product">
                    <div style="flex: 1;">
                        <h4>Urban Kinetic Hoodie</h4>
                        <p style="color: var(--text-light);">Rp 899.000</p>
                        <div style="display: flex; align-items: center; gap: 1rem; margin-top: 0.5rem;">
                            <button style="width: 35px; height: 35px; border: 1px solid #ddd; border-radius: 50%; background: white;">-</button>
                            <span style="font-weight: 600;">1</span>
                            <button style="width: 35px; height: 35px; border: 1px solid #ddd; border-radius: 50%; background: white;">+</button>
                        </div>
                    </div>
                </div>
                <!-- More items -->
            </div>
            <div class="cart-total">
                <div style="display: flex; justify-content: space-between; margin-bottom: 1rem;">
                    <span>Total:</span>
                    <span>Rp 2.097.000</span>
                </div>
                <button class="checkout-btn">Proceed to Checkout</button>
            </div>
        </div>
    </div>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenuBtn.classList.toggle('active');
            mobileMenu.classList.toggle('active');
        });

        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth' });
                
                // Close mobile menu
                if (mobileMenu.classList.contains('active')) {
                    mobileMenuBtn.classList.remove('active');
                    mobileMenu.classList.remove('active');
                }
            });
        });

        // Cart Modal
        function openCart() {
            document.getElementById('cartModal').classList.add('active');
            document.body.style.overflow = 'hidden';
        }

        function closeCart() {
            document.getElementById('cartModal').classList.remove('active');
            document.body.style.overflow = 'auto';
        }

        // Add to Cart Buttons
        document.querySelectorAll('.add-to-cart').forEach(btn => {
            btn.addEventListener('click', () => {
                btn.textContent = 'Added!';
                btn.style.background = '#28a745';
                setTimeout(() => {
                    btn.textContent = 'Add to Cart';
                    btn.style.background = 'var(--secondary)';
                }, 1500);
            });
        });

        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255,255,255,0.98)';
                header.style.boxShadow = '0 4px 30px rgba(0,0,0,0.1)';
            } else {
                header.style.background = 'rgba(255,255,255,0.95)';
                header.style.boxShadow = '0 2px 20px rgba(0,0,0,0.08)';
            }
        });

        // Intersection Observer for Animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('animate');
                }
            });
        }, { threshold: 0.1 });

        document.querySelectorAll('.product-card, .collection-card').forEach(el => {
            observer.observe(el);
        });

        // Parallax Hero Effect (Desktop)
        if (window.innerWidth >= 1024) {
            window.addEventListener('scroll', () => {
                const scrolled = window.pageYOffset;
                const hero = document.querySelector('.hero');
                hero.style.transform = `translateY(${scrolled * 0.5}px)`;
            });
        }
    </script>
</body>
</html>
