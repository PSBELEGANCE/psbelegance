<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PSB Élégance Fashion - Mode & Style</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: bold;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 30px rgba(30, 144, 255, 0.5);
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            position: relative;
        }

        .nav-links a:hover {
            color: #1e90ff;
            transform: translateY(-2px);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, rgba(26,26,26,0.8), rgba(45,45,45,0.8)), 
                        url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><defs><pattern id="fashion" patternUnits="userSpaceOnUse" width="100" height="100"><circle cx="50" cy="50" r="20" fill="%23d4af37" opacity="0.1"/></pattern></defs><rect width="100%" height="100%" fill="url(%23fashion)"/></svg>');
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
            padding: 2rem;
            animation: fadeInUp 1s ease-out;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, #1e90ff, #87ceeb, #fff);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 0 50px rgba(30, 144, 255, 0.3);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
            color: white;
            padding: 1rem 2.5rem;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 30px rgba(30, 144, 255, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(30, 144, 255, 0.4);
        }

        /* Sections */
        .section {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #1a1a1a;
            position: relative;
        }

        .section h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
        }

        /* About Section */
        .about {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .about-image {
            height: 400px;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        /* Product Gallery */
        .product-gallery {
            margin-top: 4rem;
            padding: 3rem 0;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .product-item {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
        }

        .product-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0,0,0,0.15);
        }

        .product-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .product-item:hover .product-image {
            transform: scale(1.05);
        }

        .product-info {
            padding: 1.5rem;
            text-align: center;
        }

        .product-title {
            font-size: 1.2rem;
            font-weight: bold;
            color: #1a1a1a;
            margin-bottom: 0.5rem;
        }

        .product-brand {
            color: #1e90ff;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .product-description {
            color: #666;
            font-size: 0.9rem;
            line-height: 1.5;
        }

        /* Services Section */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .service-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0,0,0,0.15);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, #1e90ff, #87ceeb);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
            font-size: 2rem;
            color: white;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%);
            color: white;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-form {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #1e90ff;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 1rem;
            border: none;
            border-radius: 10px;
            background: rgba(255,255,255,0.1);
            color: white;
            backdrop-filter: blur(10px);
        }

        .form-group input::placeholder,
        .form-group textarea::placeholder {
            color: rgba(255,255,255,0.7);
        }

        .contact-info h3 {
            color: #1e90ff;
            margin-bottom: 1rem;
        }

        .contact-info p {
            margin-bottom: 1rem;
            opacity: 0.9;
        }

        /* Footer */
        footer {
            background: #1a1a1a;
            color: white;
            text-align: center;
            padding: 2rem;
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .contact-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <nav>
            <div class="logo">PSB Élégance</div>
            <ul class="nav-links">
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#apropos">À Propos</a></li>
                <li><a href="#services">Produits</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="accueil" class="hero">
        <div class="hero-content">
            <h1>PSB Élégance Fashion</h1>
            <p>Votre boutique de mode : vêtements, sacs, chaussures et accessoires</p>
            <a href="#services" class="cta-button">Découvrir nos Produits</a>
        </div>
        
        <!-- Product Gallery -->
        <div class="product-gallery">
            <h2>Nos Produits Vedettes</h2>
            <div class="gallery-grid">
                <div class="product-item">
                    <canvas id="canvas1" class="product-image"></canvas>
                    <div class="product-info">
                        <div class="product-brand">BALENCIAGA</div>
                        <div class="product-title">Speed Trainer</div>
                        <div class="product-description">Baskets montantes en textile stretch noir avec semelle sculptée rouge et blanche</div>
                    </div>
                </div>
                <div class="product-item">
                    <canvas id="canvas2" class="product-image"></canvas>
                    <div class="product-info">
                        <div class="product-brand">BALENCIAGA</div>
                        <div class="product-title">Speed 2.0</div>
                        <div class="product-description">Baskets montantes beige avec semelle technique et design futuriste</div>
                    </div>
                </div>
                <div class="product-item">
                    <canvas id="canvas3" class="product-image"></canvas>
                    <div class="product-info">
                        <div class="product-brand">GUCCI</div>
                        <div class="product-title">Mules Horsebit</div>
                        <div class="product-description">Mules en cuir noir avec détail mors doré, élégance italienne</div>
                    </div>
                </div>
                <div class="product-item">
                    <canvas id="canvas4" class="product-image"></canvas>
                    <div class="product-info">
                        <div class="product-brand">GUCCI</div>
                        <div class="product-title">Mules Premium</div>
                        <div class="product-description">Mules en cuir noir avec logo doré, confort et style intemporel</div>
                    </div>
                </div>
                <div class="product-item">
                    <canvas id="canvas5" class="product-image"></canvas>
                    <div class="product-info">
                        <div class="product-brand">BALENCIAGA</div>
                        <div class="product-title">Speed Trainer High</div>
                        <div class="product-description">Baskets hautes noires avec semelle épaisse rouge et blanche</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="apropos" class="section about">
        <h2>À Propos de Nous</h2>
        <div class="about-content">
            <div class="about-text">
                <p>PSB Élégance Fashion est une marque dédiée à l'excellence dans le domaine de la mode. Nous proposons des créations uniques qui allient sophistication, confort et style contemporain.</p>
                <p>Notre mission est de révéler la beauté naturelle de chaque personne à travers des vêtements soigneusement sélectionnés et des accessoires raffinés. Nous croyons que la mode est un moyen d'expression personnelle et de confiance en soi.</p>
                <p>Avec une attention particulière aux détails et un service client exceptionnel, PSB Élégance Fashion s'engage à offrir une expérience d'achat mémorable et des produits de qualité supérieure.</p>
            </div>
            <div class="about-image">
                Collection Exclusive
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section">
        <h2>Nos Produits</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">👗</div>
                <h3>Vêtements</h3>
                <p>Large collection de vêtements tendance pour homme et femme : robes, pantalons, chemises, t-shirts, vestes et bien plus encore.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">👜</div>
                <h3>Sacs</h3>
                <p>Sélection exclusive de sacs à main, sacs à dos, pochettes et sacs de voyage de qualité supérieure pour tous les styles.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">👠</div>
                <h3>Chaussures</h3>
                <p>Chaussures élégantes et confortables : escarpins, baskets, bottes, sandales et chaussures de sport pour toutes les occasions.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">💍</div>
                <h3>Accessoires</h3>
                <p>Complétez votre look avec nos accessoires : bijoux, montres, ceintures, écharpes, lunettes et petite maroquinerie.</p>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section contact">
        <h2>Contactez-Nous</h2>
        <div class="contact-content">
            <div class="contact-form">
                <h3>Envoyez-nous un message</h3>
                <form>
                    <div class="form-group">
                        <label for="nom">Nom complet</label>
                        <input type="text" id="nom" placeholder="Votre nom">
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" placeholder="votre@email.com">
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" rows="5" placeholder="Votre message..."></textarea>
                    </div>
                    <button type="submit" class="cta-button">Envoyer</button>
                </form>
            </div>
            <div class="contact-info">
                <h3>Informations de Contact</h3>
                <p><strong>Adresse :</strong><br>Carrefour 30000 Tivaouane</p>
                <p><strong>Téléphone :</strong><br>212 701819749</p>
                <p><strong>Email :</strong><br>Papasalioubarr@gmail.com</p>
                <p><strong>Horaires :</strong><br>24/24 - 7/7</p>
                <p><strong>Réseaux Sociaux :</strong><br>
                   TikTok : @psbofficiel<br>
                   Instagram : @psb_elegance_fashion<br>
                   Snapchat : @psb-elegance-fashion
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 PSB Élégance Fashion. Tous droits réservés.</p>
    </div>

    <script>
        // Image data - vos photos de produits
        const imageFiles = [
            'Image 1.jpg', 'Image 2.jpg', 'Image 3.jpg', 'Image 4.jpg', 'Image 5.jpg'
        ];
        
        // Function to load and display images
        async function loadProductImages() {
            try {
                for (let i = 0; i < 5; i++) {
                    const canvas = document.getElementById(canvas${i + 1});
                    const ctx = canvas.getContext('2d');
                    
                    // Set canvas size
                    canvas.width = 280;
                    canvas.height = 250;
                    
                    try {
                        const imageData = await window.fs.readFile(imageFiles[i]);
                        const blob = new Blob([imageData], { type: 'image/jpeg' });
                        const imageUrl = URL.createObjectURL(blob);
                        
                        const img = new Image();
                        img.onload = function() {
                            // Clear canvas
                            ctx.clearRect(0, 0, canvas.width, canvas.height);
                            
                            // Calculate dimensions to maintain aspect ratio
                            const aspectRatio = img.width / img.height;
                            let drawWidth = canvas.width;
                            let drawHeight = canvas.height;
                            let offsetX = 0;
                            let offsetY = 0;
                            
                            if (aspectRatio > 1) {
                                drawHeight = canvas.width / aspectRatio;
                                offsetY = (canvas.height - drawHeight) / 2;
                            } else {
                                drawWidth = canvas.height * aspectRatio;
                                offsetX = (canvas.width - drawWidth) / 2;
                            }
                            
                            // Draw image
                            ctx.drawImage(img, offsetX, offsetY, drawWidth, drawHeight);
                            
                            // Clean up
                            URL.revokeObjectURL(imageUrl);
                        };
                        img.src = imageUrl;
                    } catch (error) {
                        // If image loading fails, show placeholder
                        ctx.fillStyle = '#f0f0f0';
                        ctx.fillRect(0, 0, canvas.width, canvas.height);
                        ctx.fillStyle = '#666';
                        ctx.font = '16px Arial';
                        ctx.textAlign = 'center';
                        ctx.fillText('Image produit', canvas.width/2, canvas.height/2);
                    }
                }
            } catch (error) {
                console.log('Images will be loaded when available');
            }
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission
        document.querySelector('form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Merci pour votre message ! Nous vous répondrons dans les plus brefs délais.');
            this.reset();
        });

        // Add scroll effect to header
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(26, 26, 26, 0.95)';
            } else {
                header.style.background = 'linear-gradient(135deg, #1a1a1a 0%, #2d2d2d 100%)';
            }
        });

        // Load images when page loads
        window.addEventListener('load', loadProductImages);
    </script>
</body>
</html>
