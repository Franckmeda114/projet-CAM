<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projet CAM - Chaîne Alimentaire Moderne | Initiative sociale Burkina Faso</title>
    <meta name="description" content="Projet CAM : initiative sociale financée par Orange Burkina pour soutenir l'agriculture et l'élevage des femmes en région.">
    <meta name="keywords" content="projet CAM, agriculture, élevage, Burkina Faso, initiative sociale, Orange Burkina, femmes rurales">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@1;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --vert-olive: #6B911B;
            --marron-terre: #502814;
            --jaune-paille: #D9D40C;
            --blanc: #FFFFFF;
            --orange: #FF6600;
            --gris-fonce: #333333;
        }

        * { 
            margin:0; 
            padding:0; 
            box-sizing:border-box; 
        }
        
        body {
            font-family: 'Times New Roman', Times, serif;
            font-style: italic;
            background: linear-gradient(to bottom, #f9f9f9, #f1f1f1);
            color: var(--gris-fonce);
            line-height:1.6;
            overflow-x: hidden;
        }
        /* Signature personnalisée */
.creator-signature {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background: rgba(107, 145, 27, 0.9);
    color: white;
    padding: 12px 18px;
    border-radius: 10px;
    font-size: 14px;
    font-weight: 500;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    z-index: 1000;
    transition: all 0.3s ease;
    backdrop-filter: blur(5px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    max-width: 220px;
    transform: scale(0.95);
    animation: signature-appear 0.5s ease forwards;
}

.creator-signature:hover {
    transform: scale(1.05);
    background: rgba(80, 40, 20, 0.95);
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
}

.creator-name {
    font-weight: bold;
    color: #FFD700;
    font-style: italic;
}

.creator-signature .heart {
    color: #FFD700;
    display: inline-block;
    margin: 0 3px;
    animation: heartbeat 2s infinite;
}

@keyframes signature-appear {
    from { opacity: 0; transform: translateY(20px) scale(0.95); }
    to { opacity: 1; transform: translateY(0) scale(0.95); }
}

@keyframes heartbeat {
    0% { transform: scale(1); }
    5% { transform: scale(1.1); }
    10% { transform: scale(1); }
    15% { transform: scale(1.1); }
    20% { transform: scale(1); }
    100% { transform: scale(1); }
}

/* Responsive */
@media (max-width: 768px) {
    .creator-signature {
        bottom: 15px;
        right: 15px;
        font-size: 12px;
        padding: 10px 14px;
        max-width: 180px;
    }
}

        /* HEADER */
        header {
            background: var(--vert-olive);
            color: var(--blanc);
            padding: 20px 0;
            text-align: center;
            position: relative;
            z-index: 10;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            margin-bottom: 15px;
        }
        
        header img {
            width: 70px;
            height: 70px;
            object-fit: contain;
            animation: float 3s ease-in-out infinite;
        }
        
        .orange-logo {
            width: 100px !important;
            border-left: 1px solid rgba(255,255,255,0.3);
            padding-left: 20px;
        }
        
        header h1 {
            font-family: 'Georgia', 'Times New Roman', Times, serif;
            font-style: italic;
            font-weight: bold;
            font-size: 2.8rem;
            letter-spacing: 1.5px;
            color: var(--blanc);
            text-shadow: 2px 2px 8px rgba(0,0,0,0.2);
            margin: 10px 0;
        }
        
        header p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto;
            color: var(--blanc);
        }

        /* NAVIGATION */
        nav {
            background: var(--jaune-paille);
            text-align: center;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        
        nav a {
            margin: 0 15px; 
            color: var(--marron-terre); 
            text-decoration: none;
            font-size: 1.2rem; 
            padding: 10px 20px; 
            border-radius: 30px; 
            transition: all 0.3s ease;
            position: relative;
            font-weight: bold;
        }
        
        nav a:hover {
            background: var(--vert-olive);
            color: var(--blanc);
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
        }
        
        nav a.active {
            background: var(--marron-terre);
            color: var(--jaune-paille);
            box-shadow: 0 6px 15px rgba(0,0,0,0.2);
        }

        /* SECTIONS */
        section {
            padding: 60px 20px; 
            margin: 40px auto; 
            max-width: 1200px;
            background: var(--blanc);
            border-radius: 15px; 
            box-shadow: 0 8px 25px rgba(0,0,0,0.08);
            transform: translateY(30px); 
            opacity: 0; 
            transition: all 0.8s ease;
        }
        
        section.visible {
            opacity: 1; 
            transform: translateY(0);
        }
        
        section h2 {
            text-align: center; 
            color: var(--vert-olive); 
            font-size: 2.5rem; 
            margin-bottom: 30px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--jaune-paille);
            position: relative;
        }
        
        section h2:after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: var(--orange);
        }
        
        section p {
            font-size: 1.25rem; 
            margin-bottom: 25px;
            text-align: justify;
            line-height: 1.8;
        }
        
        .content-block {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: flex-start;
            gap: 30px;
            margin: 40px 0;
        }
        
        .text-content {
            flex: 1;
            min-width: 300px;
        }
        
        .image-content {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .image-content img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .image-content img:hover {
            transform: scale(1.03); 
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
        }
        
        /* BUTTONS */
        .btn {
            display: inline-block; 
            padding: 14px 30px; 
            background: var(--orange); 
            color: var(--blanc);
            border-radius: 30px; 
            text-decoration: none; 
            transition: all 0.3s ease;
            font-size: 1.2rem;
            font-weight: bold;
            border: none;
            cursor: pointer;
            margin: 10px 5px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        
        .btn:hover {
            transform: translateY(-3px); 
            background: var(--vert-olive); 
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
        }
        
        /* PARTENAIRES */
        .partners {
            text-align: center;
            padding: 30px;
            background: rgba(255, 102, 0, 0.05);
            border-radius: 10px;
            margin: 40px 0;
        }
        
        .partners h3 {
            color: var(--orange);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .partner-logos {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
            flex-wrap: wrap;
        }
        
        /* CONTACT */
        #contact {
            text-align: center;
        }
        
        .contact-info {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
        }
        
        .contact-method {
            flex: 1;
            min-width: 250px;
            padding: 25px;
            background: rgba(107, 145, 27, 0.1);
            border-radius: 10px;
            transition: transform 0.3s ease;
        }
        
        .contact-method:hover {
            transform: translateY(-5px);
            background: rgba(107, 145, 27, 0.15);
        }
        
        .contact-method h3 {
            color: var(--vert-olive);
            margin-bottom: 15px;
        }
        
        form {
            max-width: 600px;
            margin: 0 auto;
            text-align: left;
        }
        
        form label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: var(--marron-terre);
        }
        
        form input, form textarea {
            width: 100%;
            padding: 14px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1.1rem;
            font-family: 'Times New Roman', Times, serif;
        }
        
        form button {
            width: 100%;
            padding: 16px;
        }
        
        /* FOOTER */
        footer {
            background: var(--marron-terre); 
            color: var(--blanc); 
            text-align: center; 
            padding: 30px 20px; 
            margin-top: 60px;
        }
        
        .footer-content {
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin: 20px 0;
        }
        
        .footer-links a {
            color: var(--jaune-paille);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--blanc);
            text-decoration: underline;
        }
        
        .copyright {
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.2);
        }
        
        /* ANIMATIONS */
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            z-index: -1;
            overflow: hidden;
            pointer-events: none;
        }
        
        .animated-bg span {
            position: absolute;
            display: block;
            width: 20px;
            height: 20px;
            background: rgba(107, 145, 27, 0.15);
            border-radius: 50%;
            animation: bubble 15s linear infinite;
            bottom: -100px;
        }
        
        @keyframes bubble {
            0% { transform: translateY(0) scale(1); opacity: 0.7; }
            50% { opacity: 0.8; }
            100% { transform: translateY(-100vh) scale(1.2); opacity: 0; }
        }
        
        /* RESPONSIVE */
        @media (max-width: 768px) {
            header h1 {
                font-size: 2.2rem;
            }
            
            nav a {
                margin: 5px;
                padding: 8px 15px;
                font-size: 1.1rem;
            }
            
            section {
                padding: 40px 15px;
            }
            
            section h2 {
                font-size: 2rem;
            }
            
            .content-block {
                flex-direction: column;
            }
            
            .logo-container {
                flex-direction: column;
                gap: 10px;
            }
            
            .orange-logo {
                border-left: none;
                border-top: 1px solid rgba(255,255,255,0.3);
                padding-left: 0;
                padding-top: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="animated-bg"></div>
    
    <header>
        <div class="header-content">
            <div class="logo-container">
                <img src="WhatsApp Image 2025-08-21 à 23.46.22_d1f6f998.jpg" alt="Logo CAM">
                <img class="orange-logo" src="WhatsApp Image 2025-08-22 à 11.54.43_a4f8168a.jpg" alt="Logo Orange Burkina">
            </div>
            <h1>Projet CAM - Chaîne Alimentaire Moderne</h1>
            <p>Initiative sociale financée par Orange Burkina pour soutenir les femmes défavorisées du Centre Ouest</p>
        </div>
    </header>

    <nav>
        <a href="#about">À propos</a>
        <a href="#activities">Activités</a>
        <a href="#objectives">Objectifs</a>
        <a href="#contact">Contact</a>
    </nav>

    <main>
        <section id="about">
            <h2>À propos du projet CAM</h2>
            <div class="content-block">
                <div class="text-content">
                    <p>Le <strong>Projet CAM (Chaîne Alimentaire Moderne)</strong> est une initiative sociale financée par <strong>Orange Burkina</strong> visant à soutenir les femmes vulnérables de la région à travers l'agriculture et l'élevage durables.</p>
                    
                    <p>Notre mission est de créer des opportunités économiques pour les femmes démunies en leur fournissant les ressources, les formations et l'accompagnement nécessaires pour développer des activités agricoles et d'élevage viables.</p>
                    
                    <p>Le projet CAM ne propose pas d'emploi mais vise à autonomiser les femmes en leur donnant les moyens de générer leurs propres revenus grâce à des pratiques durables et modernes.</p>
                </div>
                <div class="image-content">
                    <img src="WhatsApp Image 2025-08-21 à 22.15.12_2e3dced5.jpg" alt="Femmes travaillant dans l'agriculture">
                    <img src="WhatsApp Image 2025-08-22 à 07.58.03_0dda3b89.jpg" alt="Projet social pour femmes">
                </div>
            </div>
            
            <div class="partners">
                <h3>Avec le soutien de</h3>
                <div class="partner-logos">
                    <img src="WhatsApp Image 2025-08-22 à 11.54.43_a4f8168a.jpg" alt="Orange Burkina" style="max-width: 200px;">
                </div>
            </div>
        </section>

        <section id="activities">
            <h2>Nos Activités</h2>
            <div class="content-block">
                <div class="text-content">
                    <p>Le projet CAM se concentre sur deux activités principales qui offrent des opportunités économiques durables aux femmes des régions rurales :</p>
                    
                    <h3>🌱 Agriculture Durable</h3>
                    <p>Nous accompagnons les femmes dans le développement de cultures adaptées aux conditions locales, en mettant l'accent sur des techniques durables et respectueuses de l'environnement.</p>
                    
                    <h3>🐓 Élevage Traditionnel Amélioré</h3>
                    <p>Nous soutenons l'élevage de volailles et de porcs avec des méthodes modernes qui préservent les savoirs traditionnels tout en améliorant la productivité.</p>
                    
                    <p><em>Ces activités sont menées par des femmes de la région que nous formons et accompagnons dans le démarrage de cette initiative.</em></p>
                </div>
                <div class="image-content">
                    <img src="WhatsApp Image 2025-08-22 à 08.25.16_bcabacd8.jpg" alt="Agriculture durable">
                    <img src="WhatsApp Image 2025-08-22 à 07.58.02_34d712d1.jpg" alt="Élevage traditionnel">
                    <img src="WhatsApp Image 2025-08-22 à 08.25.17_683d24f5.jpg" alt="Femmes rurales">
                </div>
            </div>
        </section>

        <section id="objectives">
            <h2>Objectifs du Projet</h2>
            <div class="content-block">
                <div class="text-content">
                    <p>Le projet CAM poursuit plusieurs objectifs sociaux et économiques :</p>
                    
                    <ul style="font-size: 1.2rem; margin-left: 20px; margin-bottom: 25px;">
                        <li>Autonomiser économiquement les femmes vulnérables de la région du Centre Ouest</li>
                        <li>Optimiser la transformation des produits Agro-pastoraux</li>
                        <li>Préserver et valoriser les savoirs traditionnels</li>
                        <li>Promouvoir des pratiques agricoles durables</li>
                        <li>Renforcer la sécurité alimentaire locale</li>
                        <li>Créer des modèles reproductibles dans d'autres régions</li>
                    </ul>
                    
                    <p>Notre vision est de développer un réseau de femmes entrepreneures dans le secteur agroalimentaire, capables de subvenir à leurs besoins et à ceux de leurs familles tout en contribuant au développement économique de leur région.</p>
                    
                    <p><strong>Le projet CAM</strong> est fier d'être financé par <strong>Orange Burkina</strong> qui partage notre vision d'un développement économique inclusif et durable.</p>
                </div>
                <div class="image-content">
                    <img src="WhatsApp Image 2025-08-22 à 12.19.29_e4d68432.jpg" alt="Autonomisation des femmes">
                    <img src="WhatsApp Image 2025-08-22 à 12.17.15_5580abf1.jpg" alt="Soutien Orange Burkina">
                </div>
            </div>
            
            <div style="text-align: center; margin-top: 40px;">
                <a href="#contact" class="btn">Soutenir notre initiative</a>
            </div>
        </section>

        <section id="contact">
            <h2>Contact & Soutien</h2>
            <p>Une question, une suggestion ou envie de rejoindre notre projet ? <br>
    Notre équipe est à votre écoute ! <br><br>
    <strong>Email :</strong> 
    <a href="mailto:keturabirba@gmail.com?subject=Projet%20CAM&body=Bonjour,%20je%20suis%20intéressé%20par%20votre%20projet."
       class="btn">keturabirba@gmail.com</a><br>
    
    <strong>WhatsApp :</strong> 
    <a href="https://wa.me/22657126768?text=Bonjour,%20je%20suis%20intéressé%20par%20le%20projet%20CAM" 
       target="_blank" class="btn">‪+226 57 12 67 68‬</a> / 
    <a href="https://wa.me/22665484993?text=Bonjour,%20je%20suis%20intéressé%20par%20le%20projet%20CAM" 
       target="_blank" class="btn">‪+226 65 48 49 93‬</a><br>
    
    <strong>Facebook :</strong> 
    <a href="https://m.me/ketuingridbirba" 
       target="_blank" class="btn">facebook.com/ketuingridbirba</a>
</p>
            
            <p><strong>Le projet CAM</strong> est à la recherche de partenaires et de soutiens pour amplifier son impact social. Toute forme de collaboration est la bienvenue.</p>
            
            <form id="contact-form">
                <div style="margin-bottom: 20px;">
                    <label for="name">Nom complet</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div style="margin-bottom: 20px;">
                    <label for="email">Adresse email</label>
                    <input type="email" id="email" name="email" required>
                </div>
                
                <div style="margin-bottom: 20px;">
                    <label for="message">Votre message</label>
                    <textarea id="message" name="message" rows="5" required></textarea>
                </div>
                
                <button type="submit" class="btn">Envoyer le message</button>
            </form>
        </section>
    </main>
    <div class="creator-signature">
    Conçu par <span class="creator-name">Franck Armel MEDA</span>
</div>

    <footer>
        <div class="footer-content">
            <div class="partner-logos">
                <img src="WhatsApp Image 2025-08-21 à 23.46.22_d1f6f998.jpg" alt="Logo CAM" style="max-width: 150px;">
                <img src="WhatsApp Image 2025-08-22 à 11.54.43_a4f8168a.jpg" alt="Logo Orange Burkina" style="max-width: 150px;">
            </div>
            
            <div class="footer-links">
                <a href="#about">À propos</a>
                <a href="#activities">Activités</a>
                <a href="#objectives">Objectifs</a>
                <a href="#contact">Contact</a>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 Projet CAM - Chaîne Alimentaire Moderne. Initiative sociale financée par Orange Burkina.</p>
                <p>Email: keturabirba@gmail.com | Tél: +226 57 12 67 68 / +226 65 48 49 93</p>
            </div>
        </div>
    </footer>

    <script>
        // Animation des sections au défilement
        const sections = document.querySelectorAll('section');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        sections.forEach(section => {
            observer.observe(section);
        });

        // Animation des images
        const images = document.querySelectorAll('.image-content img');
        const imgObserver = new IntersectionObserver((entries, obs) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                    obs.unobserve(entry.target);
                }
            });
        }, { threshold: 0.2 });

        images.forEach(img => {
            img.style.opacity = '0';
            img.style.transform = 'translateY(20px)';
            img.style.transition = 'opacity 0.8s ease, transform 0.8s ease';
            imgObserver.observe(img);
        });

        // Création des bulles pour l'arrière-plan animé
        const bg = document.querySelector('.animated-bg');
        for (let i = 1; i <= 15; i++) {
            const span = document.createElement('span');
            span.style.left = Math.random() * 100 + '%';
            span.style.animationDelay = Math.random() * 15 + 's';
            span.style.animationDuration = (15 + Math.random() * 15) + 's';
            span.style.width = (10 + Math.random() * 20) + 'px';
            span.style.height = span.style.width;
            bg.appendChild(span);
        }

        // Gestion du formulaire de contact
        const contactForm = document.getElementById('contact-form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Merci pour votre message! Nous vous contacterons très bientôt.');
                contactForm.reset();
            });
        }

        // Navigation active
        const navLinks = document.querySelectorAll('nav a');
        const sectionsIds = Array.from(sections).map(section => section.id);
        
        window.addEventListener('scroll', function() {
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (pageYOffset >= (sectionTop - 200)) {
                    current = section.getAttribute('id');
                }
            });
            
            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html